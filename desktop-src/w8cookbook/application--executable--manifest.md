---
title: Manifesto do aplicativo (executável)
description: Manifesto do aplicativo (executável)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008493"
---
# <a name="app-executable-manifest"></a>Manifesto do aplicativo (executável)

## <a name="platforms"></a>Plataformas

**Clientes** – Windows 8  
**Servidores** – Windows Server 2012  


## <a name="description"></a>Descrição

A seção de compatibilidade do manifesto do aplicativo (executável) introduzido no Windows ajuda o sistema operacional a determinar as versões do Windows que um aplicativo foi projetado para direcionar. Além disso, o manifesto do aplicativo permite que o Windows forneça o comportamento que o aplicativo espera com base na versão do Windows de destino do aplicativo.

A seção de compatibilidade do manifesto permite que o Windows forneça um novo comportamento ao software recém-criado, mantendo a compatibilidade com o software existente. Esta seção ajuda o Windows a fornecer maior compatibilidade em versões futuras do Windows também. Por exemplo, um aplicativo que declara suporte somente para o Windows 8 na seção de compatibilidade continuará a receber o comportamento do Windows 8 em versões futuras do Windows.

## <a name="manifestation"></a>Manifestação

Aplicativos sem uma seção de compatibilidade em seu manifesto terão o comportamento do Windows Vista por padrão no Windows 7 e no Windows 8 e em versões futuras do Windows. Lembre-se de que o Windows XP e o Windows Vista ignoram essa seção de manifesto e não têm nenhum impacto sobre elas.

Esses componentes do Windows fornecem comportamento divergente com base na seção de compatibilidade:

**Pool de threads padrão RPC (chamada de procedimento remoto)**

-   Windows 8 e Windows 7: para melhorar a escalabilidade e reduzir as contagens de threads, o RPC alternou para o pool de threads do NT (pool padrão). Para o Windows Vista, o RPC usou um pool de threads privado:

    -   Para binários compilados para o Windows 7 e versões posteriores do Windows, o pool padrão é usado.
    -   Se I \_ RpcMgmtEnableDedicatedThreadPool for chamado antes de qualquer API RPC ser chamada, o pool de threads privado será usado (comportamento do vista).
    -   Se eu \_ RpcMgmtEnableDedicatedThreadPool for chamado depois de uma chamada RPC, o pool padrão será usado, I \_ RpcMgmtEnableDedicatedThreadPool retornará o erro 1764 e não haverá suporte para a operação solicitada.

-   Windows Vista (padrão): para binários compilados para o Windows Vista e versões anteriores do Windows, o pool privado é usado.

**Bloqueio do DirectDraw**

-   Windows 8 e Windows 7: os aplicativos manifestados para o Windows 7 e versões posteriores do sistema operacional não podem chamar a API de bloqueio em DDRAW para bloquear o buffer de vídeo da área de trabalho principal; Isso resultará em um erro e será retornado um ponteiro nulo para o primário. Esse comportamento é imposto mesmo se Gerenciador de Janelas da Área de Trabalho composição não estiver ativada. Aplicativos com compatibilidade declarada para o Windows 7 e posterior não devem bloquear o buffer de vídeo primário para renderização.
-   Windows Vista (padrão): os aplicativos podem adquirir um bloqueio no buffer de vídeo primário, pois os aplicativos herdados dependem desse comportamento; a execução do aplicativo é desativada Gerenciador de Janelas da Área de Trabalho.

**BitBlt (transferência de bloco de bits) do DirectDraw para primário sem janela de recorte**

-   Windows 8 e Windows 7: os aplicativos manifestados para o Windows 7 e versões posteriores do Windows são impedidos de executar um BitBlt para o buffer de vídeo da área de trabalho principal sem uma janela de recorte; Isso resulta em um erro e a área de BitBlt não será renderizada. O Windows impõe esse comportamento mesmo se você não ativar Gerenciador de Janelas da Área de Trabalho composição. Aplicativos com compatibilidade declarada para o Windows 7 e posterior devem executar um BitBlt em uma janela de recorte.
-   Windows Vista (padrão): os aplicativos devem ser capazes de executar um BitBlt para o primário sem uma janela de recorte, pois os aplicativos herdados dependem desse comportamento; a execução desse aplicativo desativa o Gerenciador de Janelas da Área de Trabalho.

**API GetOverlappedResult**

-   Windows 8 e Windows 7: resolve uma condição de corrida em que um aplicativo multithread usando **GetOverlappedResult** pode retornar sem redefinir o evento na estrutura sobreposta, fazendo com que a próxima chamada para essa função seja retornada prematuramente.
-   Windows Vista (padrão): fornece o comportamento com a condição de corrida na qual os aplicativos podem ter uma dependência. Os aplicativos que devem evitar essa corrida antes do comportamento do Windows 7 devem aguardar no evento sobreposto e, quando sinalizado, chamar GetOverlappedResult com bWait = = FALSE.

**Status de temas do Shell no modo de alto contraste**

-   Windows 8: retorna o status real de ti para quando estiver no modo de alto contraste.
-   Windows 7: retorna-os como indisponíveis no modo de alto contraste porque o DWM ainda está ativado.
-   Windows Vista (padrão): retorna-os como indisponíveis no modo de alto contraste, pois o DWM ainda está ativado.

**Método Shell iPersistFile:: Save**

-   Windows 8: CShellLink:: Save agora determina se o manipulador IPersistFile é chamado com um argumento de caminho relativo e falha na chamada, se for.

    A [documentação pública](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) que descreve esse comportamento indica que o argumento de caminho deve ser um caminho absoluto:

-   Windows 7 e anterior (padrão): CShellLink:: Save não determina se o manipulador iPersistFile envia uma verificação de caminho relativa e permite que os aplicativos continuem trabalhando com caminhos absolutos ou relativos.

**PCA (Assistente de compatibilidade do programa)**

-   Windows 8: os aplicativos com a seção de compatibilidade não obtêm a mitigação do PCA.
-   Windows 7: os aplicativos com a seção de compatibilidade são acompanhados para possíveis problemas de compatibilidade com as alterações do Windows 8 (descritas neste documento).
-   Windows Vista (padrão): aplicativos que não são instalados corretamente ou falham durante o tempo de execução em algumas circunstâncias específicas obtêm a mitigação do PCA. Para obter mais informações, consulte a seção recursos.

## <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

Atualize o manifesto do aplicativo com as informações de compatibilidade mais recentes para o suporte do sistema operacional. Esta seção descreve as adições ao manifesto:

**Namespace:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)

**Nome da seção:** Compatibilidade (nova seção)

**SupportedOS:** GUID do sistema operacional com suporte-os GUIDs que mapeiam para os sistemas operacionais com suporte são:

-   {e2011457-1546-43c5-a5fe-008deee3d3f0}

    para o **Windows Vista**: esse é o valor padrão para o contexto Switchback

-   {35138b9a-5d96-4fbd-8e2d-a2440225f93a}

    para o **Windows 7**: os aplicativos que definem esse valor no manifesto do aplicativo obtêm o comportamento do Windows 7

-   {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}

    para o **Windows 8**: os aplicativos que definem esse valor no manifesto do aplicativo obtêm o comportamento do Windows 8

A Microsoft irá gerar e lançar GUIDs para versões futuras do Windows, conforme necessário.

Um exemplo de XML de um manifesto atualizado:

> [!Note]  
> O atributo e os nomes de marca no manifesto do aplicativo diferenciam maiúsculas de minúsculas.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



Os GUIDs para todos os sistemas operacionais no exemplo anterior fornecem suporte de nível inferior. Os aplicativos que dão suporte a várias plataformas não precisam de manifestos separados para cada plataforma.

## <a name="tests"></a>Testes

Um aplicativo pode especificar várias IDs de sistema operacional com suporte. Você deve adicionar uma ID do sistema operacional com suporte se tiver testado ou estiver no processo de teste, o aplicativo nesse sistema operacional. O Windows Vista e versões anteriores do sistema operacional não preste atenção a essas entradas. A partir do Windows 7, o Windows escolherá o GUID de versão mais alto no manifesto até a versão do Windows em execução e dará ao aplicativo o suporte nesse nível. Para verificar se o aplicativo funciona com a nova seção de compatibilidade de manifesto de aplicativo:

1.  Teste o aplicativo com a nova seção de compatibilidade e SupportedOS ID = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} para garantir que o aplicativo funcione corretamente usando o comportamento mais recente do Windows 8.
2.  Teste o aplicativo com a nova seção de compatibilidade e SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para garantir que o aplicativo funcione corretamente usando o comportamento do Windows 7.
3.  Teste o aplicativo com a nova seção de compatibilidade e SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} para garantir que o aplicativo funcione corretamente usando o comportamento do Windows Vista.

## <a name="resources"></a>Recursos

-   [Função QueryActCtxW](../sbscs/application-manifests.md)
-   [Manifesto do UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifestos de aplicativo para aplicativos do Windows](../sbscs/application-manifests.md)
-   [Gerenciador de Janelas da Área de Trabalho (DWM)](../dwm/dwm-overview.md)
-   [Atualização de incompatibilidade de contexto](https://support.microsoft.com/kb/978637)
-   [Assistente de compatibilidade de programa](/previous-versions/bb756937(v=msdn.10))

 

 