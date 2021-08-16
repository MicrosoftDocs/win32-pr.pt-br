---
description: Os gerenciadores de visualização são chamados quando um item é selecionado para mostrar uma visualização leve, rica e somente leitura do conteúdo do arquivo no painel de leitura do modo de exibição. Isso é feito sem iniciar o aplicativo associado do arquivo.
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: Gerenciadores de visualização e host de visualização do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ccc6c2a519b4f9646e76a0a0ef4d0d26348e08d114eb9a080aaee09a75b9f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858758"
---
# <a name="preview-handlers-and-shell-preview-host"></a>Gerenciadores de visualização e host de visualização do Shell

Os gerenciadores de visualização são chamados quando um item é selecionado para mostrar uma visualização leve, rica e *somente leitura* do conteúdo do arquivo no painel de leitura do modo de exibição. Isso é feito sem iniciar o aplicativo associado do arquivo.

Este tópico aborda os seguintes tópicos:

-   [Arquitetura do Gerenciador de visualização](#preview-handler-architecture)
-   [Opções de modelo de servidor](#server-model-options)
-   [Inicialização](#initialization)
-   [Flow de dados do Gerenciador de visualização](#preview-handler-data-flow)
-   [Depurando um Gerenciador de visualização](#debugging-a-preview-handler)
-   [Fornecendo seu próprio processo para um Gerenciador de visualização](#providing-your-own-process-for-a-preview-handler)
-   [Tópicos relacionados](#related-topics)

## <a name="preview-handler-architecture"></a>Arquitetura do Gerenciador de visualização

Um Gerenciador de visualização é um aplicativo hospedado. os hosts incluem o Windows Explorer no Windows Vista ou no Microsoft Outlook 2007. Os hosts implementam [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) como um método de comunicação entre o Gerenciador de visualização e o host.

O próprio Gerenciador de visualização implementa essas interfaces:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (opcional)

Seu manipulador é chamado por meio de seu [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), que retorna um ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) por meio do qual você solicita um objeto [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) para interagir com o host.

## <a name="server-model-options"></a>Opções de modelo de servidor

Os gerenciadores de visualização sempre ficam fora do processo. Há dois métodos para implementar isso:

1.  Um Gerenciador de visualização pode ser criado como um servidor em processo, mas executado por meio de um host alternativo fora do processo. Este é o método preferencial. O sistema fornece um host alternativo para isso no arquivo de Prevhost.exe. os gerenciadores de visualização criados por esse método não são compatíveis com Outlook 2007 no Windows XP. no entanto, esses mesmos manipuladores funcionarão no Windows Explorer e no Outlook 2007 em execução no Windows Vista.
2.  Um Gerenciador de visualização pode ser criado como um servidor local Component Object Model (COM). Isso não é recomendado por vários motivos. Primeiro, a implementação de um servidor em processo é mais fácil. O mais importante é que a implementação como um servidor em processo fornece maior controle sobre o tempo de vida do objeto do manipulador, o que permite melhor limpeza e eficiência.

Por padrão, os gerenciadores de visualização são executados em um processo de nível de integridade baixo (IL) por motivos de segurança. Opcionalmente, você pode desabilitar a execução como um processo de IL baixo definindo o seguinte valor no registro. No entanto, não é recomendável fazer isso. Os sistemas podem eventualmente ser configurados para rejeitar qualquer processo que não seja de IL baixo.

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

Os diferentes gerenciadores de visualização compartilham o mesmo processo por padrão. Duas instâncias do Prevhost.exe podem ser executadas simultaneamente; um para os manipuladores executados como processos de IL baixo, um para manipuladores que tenham optado por esse comportamento.

## <a name="initialization"></a>Inicialização

Assim como com os manipuladores de miniatura e propriedade, é altamente recomendável que você Inicialize seu manipulador com um fluxo. Você pode inicializar por meio de um arquivo ou item, se necessário, mas os fluxos fornecem a maneira mais segura de implementar um manipulador. A inicialização por meio de um fluxo garante a integridade do arquivo e os benefícios de estabilidade para o sistema de executar o manipulador como um processo de IL baixo, como proteger o sistema contra estouros de buffer, limitando onde um manipulador pode gravar informações e limitando a comunicação com outras janelas.

Se você precisar inicializar com um item de arquivo ou de Shell, armazene o caminho do arquivo ou uma referência ao [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem). Não leia dados dessas fontes até que [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) seja chamado.

Em geral, a inicialização não deve fazer nenhum trabalho pesado, como compor e armazenar uma imagem de visualização. Para uma eficiência ideal, esse tipo de processamento não deve ser feito até que a versão prévia seja chamada para.

## <a name="preview-handler-data-flow"></a>Flow de dados do Gerenciador de visualização

O fluxo de dados no processo de visualização segue o caminho geral mostrado aqui. o host pode ser considerado como Windows Explorer no Windows Vista ou Outlook 2007.

1.  O Gerenciador de visualização é inicializado, preferencialmente com um fluxo.
2.  A janela de exibição é passada do host para o manipulador por meio de [**IPreviewHandler:: SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow).
3.  Neste ponto, o manipulador não deve fazer nada mais até que [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) seja chamado.
4.  A visualização é exibida no painel de leitura por meio de uma chamada para [**IPreviewHandler::D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview).
5.  O tamanho da janela é definido por meio de [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
6.  A janela é redimensionada quando necessário por meio de [**IPreviewHandler:: SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect).
7.  A visualização é descarregada e seus recursos são liberados quando não são mais necessários, por meio de uma chamada para [**IPreviewHandler:: Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload).

## <a name="debugging-a-preview-handler"></a>Depurando um Gerenciador de visualização

Se você seguiu as recomendações para implementar o Gerenciador de visualização como um servidor em processo, para depurar o Gerenciador de visualização, você pode anexar ao Prevhost.exe. Como mencionado anteriormente, lembre-se de que pode haver duas instâncias do Prevhost.exe, uma para processos normais de IL baixo e outra para os manipuladores que tenham optado por ser executado como um processo de IL baixo.

Se você não encontrar Prevhost.exe na sua lista de processos disponíveis, provavelmente ele não foi carregado nesse ponto. Clicar em um arquivo para uma visualização carrega o substituto e, em seguida, ele deve aparecer como um processo anexável.

## <a name="providing-your-own-process-for-a-preview-handler"></a>Fornecendo seu próprio processo para um Gerenciador de visualização

Se você quiser forçar a criação de um novo processo para seu manipulador em vez de executar sob o processo padrão, crie uma nova subchave para o manipulador em **AppID** e defina sua entrada DllSurrogate como "Prevhost.exe". Use essa subchave **AppID** em vez do padrão Prevhost.exe **AppID**.

Ao fornecer um novo processo, o manipulador pode evitar a execução em um processo compartilhado como faria por padrão. Isso pode permitir, por exemplo, garantir a versão específica do Common Language Runtime (CLR) no processo. Isso será necessário se você estiver criando uma implementação gerenciada de um Gerenciador de visualização.

> [!Note]  
> os gerenciadores de visualização de 32 bits devem usar **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} quando instalados em sistemas operacionais de 64 bits.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando gerenciadores de visualização](building-preview-handlers.md)
</dt> <dt>

[Como registrar um Gerenciador de visualização](how-to-register-a-preview-handler.md)
</dt> <dt>

[Diretrizes do Gerenciador de visualização](preview-handler-guidelines.md)
</dt> </dl>

 

 
