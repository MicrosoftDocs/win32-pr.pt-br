---
title: Sobre ícones
description: Este tópico discute os ícones.
ms.assetid: 67867460-07f6-460f-9263-05bbf3474744
keywords:
- recursos, ícones
- ícones, pontos de acesso
- ícones, padrão
- ícones padrão
- ícones, personalizado
- ícones personalizados
- ícones, tamanhos
- criando ícones
- ícones, exibindo
- ícones, destruindo
- ícones, duplicando
- ícones, criando
- exibindo ícones
- destruindo ícones
- duplicando ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a56f049999ab4c5a00953db552e4977cc26366af669141d15fa1fc53c4cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870743"
---
# <a name="about-icons"></a>Sobre ícones

O sistema usa ícones em toda a interface do usuário para representar objetos como arquivos, pastas, atalhos, aplicativos e documentos. As funções de ícone permitem que os aplicativos criem, carreguem, exibam, organizem, animem e destruam ícones. Para obter informações sobre como especificar ícones para tipos de arquivo, consulte [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona).

Esta visão geral fornece informações sobre os seguintes tópicos:

-   [Ponto de acesso de ícone](#icon-hot-spot)
-   [Tipos de ícone](#icon-types)
-   [Tamanhos de ícone](#icon-sizes)
    -   [Para alterar o tamanho do ícone pequeno do sistema](#to-change-the-size-of-the-system-small-icon)
    -   [Para recuperar o tamanho do ícone pequeno do sistema](#to-retrieve-the-size-of-the-system-small-icon)
    -   [Para recuperar o tamanho do ícone grande do sistema](#to-retrieve-the-size-of-the-system-large-icon)
    -   [Para recuperar o tamanho do ícone pequeno do Shell](#to-retrieve-the-size-of-the-shell-small-icon)
    -   [Para alterar o tamanho do ícone grande](#to-change-the-size-of-the-large-icon)
    -   [Para recuperar o tamanho do ícone grande do Shell](#to-retrieve-the-size-of-the-shell-large-icon)
-   [Criação de ícone](#icon-creation)
-   [Exibição de ícone](#icon-display)
-   [Destruição de ícone](#icon-destruction)
-   [Duplicação de ícone](#icon-duplication)

## <a name="icon-hot-spot"></a>Ponto de acesso de ícone

Um dos pixels em um ícone é designado como ponto de [acesso](#icon-hot-spot), que é o ponto que o sistema acompanha e reconhece como a posição do ícone. O ponto de acesso de um ícone é normalmente o pixel localizado no centro do ícone. Se você usar a função [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) para criar um ícone, poderá especificar qualquer pixel para ser o ponto de acesso.

## <a name="icon-types"></a>Tipos de ícone

O sistema operacional fornece um conjunto de *ícones padrão* que estão disponíveis para qualquer aplicativo a ser usado a qualquer momento. Os arquivos de cabeçalho Software Development Kit (SDK) contêm identificadores para os ícones padrão — os identificadores começam com o prefixo **IDI \_** .

Cada ícone padrão tem uma imagem padrão correspondente associada a ele. O usuário pode substituir a imagem padrão associada a qualquer cursor padrão a qualquer momento.

Os *ícones personalizados* são projetados para uso em um aplicativo específico e podem ser qualquer design. A seguir estão vários ícones personalizados.

![vários ícones personalizados](images/csicn-02.png)

## <a name="icon-sizes"></a>Tamanhos de ícone

O sistema usa quatro tamanhos de ícone:

-   Sistema pequeno
-   Sistema grande
-   Shell pequeno
-   Shell grande

O *ícone pequeno do sistema* é exibido na legenda da janela.

### <a name="to-change-the-size-of-the-system-small-icon"></a>Para alterar o tamanho do ícone pequeno do sistema

1.  No painel de controle, clique em **Exibir** e, em seguida, clique na guia **aparência** .
2.  Selecione os **botões de legenda** na lista **Item** e, em seguida, defina o campo **tamanho** .

### <a name="to-retrieve-the-size-of-the-system-small-icon"></a>Para recuperar o tamanho do ícone pequeno do sistema

-   Chame a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) com **SM \_ CXSMICON** e **SM \_ CYSMICON**.

O *ícone grande do sistema* é usado principalmente por aplicativos, mas também é exibido na caixa de diálogo Alt + Tab. As funções [**CreateIconFromResource**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresource), [**DrawIcon**](/windows/desktop/api/Winuser/nf-winuser-drawicon), [**ExtractAssociatedIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extractassociatedicona), [**ExtractIcon**](/windows/desktop/api/Shellapi/nf-shellapi-extracticona), [**ExtractIconEx**](/windows/desktop/api/Shellapi/nf-shellapi-extracticonexa)e [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) usam ícones grandes do sistema. O tamanho do ícone grande do sistema é definido pelo driver de vídeo, portanto, não pode ser alterado.

### <a name="to-retrieve-the-size-of-the-system-large-icon"></a>Para recuperar o tamanho do ícone grande do sistema

-   Chame [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) com **SM \_ CXICON** e **SM \_ CYICON**.

As funções [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon), [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex), [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect)e [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) podem ser usadas para trabalhar com ícones em tamanhos diferentes do sistema grande.

o *ícone pequeno do shell* é usado no Windows Explorer e nas caixas de diálogo comuns. Atualmente, esse padrão é o tamanho pequeno do sistema.

### <a name="to-retrieve-the-size-of-the-shell-small-icon"></a>Para recuperar o tamanho do ícone pequeno do Shell

1.  Use a função [SHGetFileInfo](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) com `SHGFI_SHELLICONSIZE | SHGFI_SMALLICON` para recuperar um identificador para a lista de imagens do sistema.
2.  Em seguida, chame a função [**ImageList \_ geticonize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) para obter o tamanho do ícone.

O ícone grande do Shell é usado na área de trabalho.

### <a name="to-change-the-size-of-the-large-icon"></a>Para alterar o tamanho do ícone grande

1.  No painel de controle, clique em **Exibir** e, em seguida, clique na guia **aparência** ,
2.  Selecione o **ícone** na lista de **itens** e, em seguida, defina o campo **tamanho** (esse tamanho é armazenado no registro, em **HKEY \_ atual \_ \\ painel de controle do usuário, \\ WindowMetrics do ícone do \\ shell do desktop**).
3.  Clique no **Plus!** e, em seguida, marque a caixa de seleção **usar ícones grandes** .

### <a name="to-retrieve-the-size-of-the-shell-large-icon"></a>Para recuperar o tamanho do ícone grande do Shell

1.  Use a função [**SHGetFileInfo**](/windows/win32/api/shellapi/nf-shellapi-shgetfileinfoa) com **SHGFI \_ SHELLICONSIZE** para recuperar um identificador para a lista de imagens do sistema.
2.  Em seguida, chame a função [**ImageList \_ geticonize**](/windows/win32/api/commctrl/nf-commctrl-imagelist_geticonsize) para obter o tamanho do ícone.

o menu Iniciar usa ícones pequenos do shell ou ícones grandes do shell, dependendo se a caixa de seleção **usar ícones grandes** está marcada.

Seu aplicativo deve fornecer grupos de imagens de ícone nos seguintes tamanhos:

-   48x48, cor de 256
-   32x32, 16 cores
-   16x16 pixels, 16 cores

Ao preencher a estrutura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) a ser usada no registro da classe de janela, defina o membro **HICON** como o ícone 32x32 e o membro **hIconSm** para o ícone 16x16. Para obter mais informações sobre ícones de classe, consulte [ícones de classe](/windows/desktop/winmsg/about-window-classes).

## <a name="icon-creation"></a>Criação de ícone

Os ícones padrão são predefinidos, portanto, não é necessário criá-los. Para usar um ícone padrão, um aplicativo pode obter seu identificador usando a função [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) . Um *identificador de ícone* é um valor exclusivo do tipo **HICON** que identifica um ícone padrão ou personalizado.

Para criar um ícone personalizado para um aplicativo, você normalmente usaria um aplicativo de gráficos e incluiria o [recurso de ícone](./icon-resource.md) no arquivo de definição de recurso do aplicativo. Em tempo de execução, você pode chamar [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) para recuperar um identificador para o ícone. Um recurso de ícone pode conter um grupo de imagens para vários dispositivos de vídeo diferentes. **LoadIcon** e **LoadImage** selecionam automaticamente o ícone mais apropriado do grupo para o dispositivo de vídeo atual.

Um aplicativo também pode criar um ícone personalizado em tempo de execução usando a função [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , que cria um ícone com base no conteúdo de uma estrutura [**ICONINFO**](/windows/desktop/api/Winuser/ns-winuser-iconinfo) . A função [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) preenche a estrutura com as coordenadas do ponto de acesso e as informações sobre o bitmap de bitmask e bitmap de cor para o ícone.

Os aplicativos devem implementar ícones personalizados como recursos e devem usar [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea), em vez de criar o ícone em tempo de execução. O uso de recursos de ícone evita a dependência de dispositivos, simplifica a localização e permite que os aplicativos compartilhem formas de ícones.

A função [**CreateIconFromResourceEx**](/windows/desktop/api/Winuser/nf-winuser-createiconfromresourceex) permite que um aplicativo Navegue pelos recursos do sistema e crie ícones e cursores com base nos dados do recurso. **CreateIconFromResourceEx** cria um ícone baseado em dados de recursos binários de outros arquivos ou DLLs executáveis. Um aplicativo deve preceder essa função com chamadas para a função [**LookupIconIdFromDirectoryEx**](/windows/desktop/api/Winuser/nf-winuser-lookupiconidfromdirectoryex) e várias funções de recurso. **LookupIconIdFromDirectoryEx** retorna o identificador dos dados de ícone mais apropriados para o dispositivo de vídeo atual.

## <a name="icon-display"></a>Exibição de ícone

Você pode recuperar a imagem para um ícone usando a função [**GetIconInfo**](/windows/desktop/api/Winuser/nf-winuser-geticoninfo) e pode desenhá-la usando a função [**DrawIconEx**](/windows/desktop/api/Winuser/nf-winuser-drawiconex) . Para desenhar a imagem padrão para um ícone, especifique o sinalizador de **\_ compatibilidade de di** na chamada para **DrawIconEx**. Se você não especificar o sinalizador **\_ compatível com di** , **DrawIconEx** desenhará o ícone usando a imagem especificada pelo usuário.

Quando o sistema exibe um ícone, ele deve extrair a imagem de ícone apropriada do arquivo .exe ou .dll. O sistema usa as seguintes etapas para selecionar a imagem do ícone:

1.  Selecione o recurso de **\_ \_ ícone de grupo RT** . Se houver mais de um recurso, o sistema usará o primeiro recurso listado no recurso cript.
2.  Selecione a imagem **de \_ ícone de RT** apropriada do recurso de **\_ \_ ícone de grupo RT** . Se houver mais de uma imagem, o sistema usará os seguintes critérios para escolher uma imagem:
    -   -   A imagem mais próxima de tamanho para o tamanho solicitado é escolhida.
        -   Se duas ou mais imagens desse tamanho estiverem presentes, a que corresponder à intensidade de cor da exibição será escolhida.
        -   Se nenhuma imagem corresponder exatamente à intensidade de cor da exibição, a imagem com a maior profundidade de cor que não exceda a intensidade de cor da exibição será escolhida. Se todos excederem a profundidade de cor, aquele com a menor intensidade de cor será escolhido.

> [!Note]  
> O sistema trata todas as profundidades de cor de 8 ou mais bpp como iguais. Portanto, não há nenhuma vantagem de incluir uma imagem de 16 a 256 cores e uma imagem de dezesseis cores de 16x16 no mesmo recurso – o sistema simplesmente escolherá a primeira que encontrar. Quando a exibição estiver no modo de 8-bpp, o sistema escolherá um ícone de 16 cores em um ícone de cor de 256 e exibirá todos os ícones usando a paleta padrão do sistema.

 

Para exibir um ícone animado, use um controle estático, conforme mostrado no fragmento de código a seguir.


```
hIcon = LoadImage(NULL, "ico.ani", IMAGE_ICON, 0, 0, LR_LOADFROMFILE);
SendMessage( hStatic, STM_SETIMAGE, IMAGE_ICON, (LPARAM)(UINT)hIcon);
```



## <a name="icon-destruction"></a>Destruição de ícone

Quando um aplicativo não precisar mais de um ícone criado usando a função [**CreateIconIndirect**](/windows/desktop/api/Winuser/nf-winuser-createiconindirect) , ele deverá destruir o ícone. A função [**DestroyIcon**](/windows/desktop/api/Winuser/nf-winuser-destroyicon) destrói a alça do ícone e libera qualquer memória usada pelo ícone. Os aplicativos devem usar essa função somente para ícones criados com **CreateIconIndirect**; Não é necessário destruir outros ícones.

## <a name="icon-duplication"></a>Duplicação de ícone

A função [**CopyIcon**](/windows/desktop/api/Winuser/nf-winuser-copyicon) copia um identificador de ícone. Isso permite que um aplicativo ou uma DLL Obtenha seu próprio identificador para um ícone de propriedade de outro módulo. Em seguida, se o outro módulo for liberado, o aplicativo que copiou o ícone ainda será capaz de usar o ícone.

A função [**CopyImage**](/windows/desktop/api/Winuser/nf-winuser-copyimage) cria um novo ícone com base no ícone de origem especificado. O novo ícone pode ser maior ou menor do que o ícone de origem.

Para obter informações sobre como adicionar, remover ou substituir os recursos de ícone em arquivos executáveis (.exe), consulte [recursos](resources.md).

A função [**DuplicateIcon**](/windows/desktop/api/Shellapi/nf-shellapi-duplicateicon) faz uma cópia real do ícone.

 

 