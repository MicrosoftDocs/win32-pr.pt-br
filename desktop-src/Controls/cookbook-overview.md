---
title: Habilitar estilos visuais
description: Este tópico explica como configurar seu aplicativo para garantir que controles comuns sejam exibidos no estilo visual preferido do usuário.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f259be6165bd3a4f9f5a655aaecf0fe6837de3dce057848ba92ac737e608fbc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413362"
---
# <a name="enabling-visual-styles"></a>Habilitar estilos visuais

Este tópico explica como configurar seu aplicativo para garantir que controles comuns sejam exibidos no estilo visual preferido do usuário.

Este tópico inclui as seções a seguir.

-   [Usando manifestos ou diretivas para garantir que estilos visuais possam ser aplicados a aplicativos](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Usando ComCtl32.dll versão 6 em um aplicativo que usa apenas extensões padrão](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Usando o ComCtl32 versão 6 Painel de Controle ou uma DLL que é executado por RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Adicionando suporte de estilo visual a uma extensão, plug-in, snap-in do MMC ou uma DLL que é levada para um processo](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Como desligar estilos visuais](#turning-off-visual-styles)
-   [Usando estilos visuais com conteúdo HTML](#using-visual-styles-with-html-content)
-   [Quando estilos visuais não são aplicados](#when-visual-styles-are-not-applied)
-   [Tornando seu aplicativo compatível com versões anteriores do Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Tópicos relacionados](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Usando manifestos ou diretivas para garantir que estilos visuais possam ser aplicados a aplicativos

Para permitir que seu aplicativo use estilos visuais, você deve usar ComCtl32.dll versão 6 ou posterior. Como a versão 6 não é redistribuível, ela está disponível somente quando seu aplicativo está em execução em uma versão do Windows que o contém. Windows vem com as versões 5 e 6. ComCtl32.dll versão 6 contém os controles de usuário e os controles comuns. Por padrão, os aplicativos usam os controles de usuário definidos User32.dll e os controles comuns definidos ComCtl32.dll versão 5. Para ver uma lista de versões de DLL e suas plataformas de distribuição, consulte [Versões de Controle Comum](common-control-versions.md).

Se você quiser que seu aplicativo use estilos visuais, adicione um manifesto do aplicativo ou uma diretiva do compilador que indique que ComCtl32.dll versão 6 deve ser usada se estiver disponível.

Um manifesto do aplicativo permite que um aplicativo especifique quais versões de um assembly ele requer. No Microsoft Win32, um assembly é um conjunto de DLLs e uma lista de objetos com controle de versão contidos nessas DLLs.

Os manifestos são gravados em XML. O nome do arquivo de manifesto do aplicativo é o nome do executável seguido pela extensão de nome de arquivo .manifest; por exemplo, MyApp.exe.manifest. O manifesto de exemplo a seguir mostra que a primeira seção descreve o manifesto em si. A tabela a seguir mostra os atributos definidos pelo **elemento assemblyIdentity** na seção de descrição do manifesto.



| Atributo             | Descrição                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Versão do manifesto. A versão deve estar no formato major.minor.revision.build (ou seja, n.n.n.n.n, em que n <=65535). |
| processorArchitecture | Processador para o qual seu aplicativo é desenvolvido.                                                                          |
| name                  | Inclui nome da empresa, nome do produto e nome do aplicativo.                                                                   |
| tipo                  | Tipo de aplicativo, como Win32.                                                                                    |



 

O manifesto de exemplo também fornece uma descrição do aplicativo e especifica as dependências do aplicativo. A tabela a seguir mostra os atributos definidos pelo **elemento assemblyIdentity** na seção de dependência.



| Atributo             | Descrição                                      |
|-----------------------|--------------------------------------------------|
| type                  | Tipo do componente de dependência, como Win32. |
| name                  | Nome do componente.                           |
| version               | A versão do componente.                        |
| processorArchitecture | Processador para o que o componente foi projetado.    |
| Publickeytoken        | Token de chave usado com esse componente.              |
| Linguagem              | Idioma do componente.                       |



 

A seguir está um exemplo de um arquivo de manifesto.

> [!IMPORTANT]
> De definir a entrada **processorArchitecture** como **"X86"** se o aplicativo for destinado à plataforma Windows de 32 bits ou como **"amd64"** se o aplicativo tiver como destino a plataforma de Windows de 64 bits. Você também pode especificar **" \* "**, que garante que todas as plataformas sejam direcionadas, conforme mostrado nos exemplos a seguir.

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



Se você estiver usando o Microsoft Visual C++ 2005 ou posterior, poderá adicionar a seguinte diretiva do compilador ao código-fonte em vez de criar manualmente um manifesto. Para a capacidade de leitura, a diretiva é dividida em várias linhas aqui.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



Os tópicos a seguir descrevem as etapas para aplicar estilos visuais a diferentes tipos de aplicativos. Observe que o formato de manifesto é o mesmo em cada caso.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Usando ComCtl32.dll versão 6 em um aplicativo que usa apenas extensões padrão

A seguir estão exemplos de aplicativos que não usam extensões de terceiros.

-   Calculadora
-   FreeCell (no Windows Vista e Windows 7)
-   OMsweeper (no Windows Vista e Windows 7)
-   Bloco de notas
-   Solitaire (no Windows Vista e Windows 7)

**Para criar um manifesto e permitir que seu aplicativo use estilos visuais.**

1.  Vincule a ComCtl32.lib e [**chame InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
2.  Adicione um arquivo chamado YourApp.exe.manifest à árvore de origem que tem o formato de manifesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Adicione o manifesto ao arquivo de recurso do aplicativo da seguinte forma:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Ao adicionar a entrada anterior ao recurso, você deve formatá-la em uma linha. Como alternativa, você pode colocar o arquivo de manifesto XML no mesmo diretório que o arquivo executável do aplicativo. O sistema operacional carregará o manifesto do sistema de arquivos primeiro e, em seguida, verificará a seção de recursos do executável. A versão do sistema de arquivos tem precedência.

     

Quando você criar seu aplicativo, o manifesto será adicionado como um recurso binário.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Usando o ComCtl32 versão 6 Painel de Controle ou uma DLL que é executado por RunDll32.exe

**Para criar um manifesto e permitir que seu aplicativo use estilos visuais.**

1.  Vincule a ComCtl32.lib e [**chame InitCommonControls.**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
2.  Adicione um arquivo chamado YourApp.cpl.manifest à árvore de origem que tem o formato de manifesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Adicione o manifesto ao arquivo de recurso do aplicativo como ID de recurso 123.

> [!Note]  
> Quando você autor de um Painel de Controle, coloque-o na categoria apropriada. Painel de Controle agora dá suporte à categorização de Painel de Controle aplicativos. Isso significa que Painel de Controle aplicativos podem ser atribuídos a identificadores e separados em áreas de tarefa, como Adicionar ou Remover Programas, Aparência e Temas ou Data, Hora, Idioma e Opções Regionais.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Adicionando suporte de estilo visual a uma extensão, plug-in, snap-in do MMC ou uma DLL que é levada para um processo

O suporte para estilos visuais pode ser adicionado a uma extensão, plug-in, snap-in do MMC ou uma DLL que é levada para um processo. Por exemplo, use as etapas a seguir para adicionar suporte a estilos visuais para um snap-in Console de Gerenciamento Microsoft (MMC).

1.  Compile o snap-in com o sinalizador -DISOLATION AWARE ENABLED ou insira a instrução a seguir antes da instrução \_ \_ include \# "windows.h".

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Para obter mais informações sobre ISOLATION \_ AWARE \_ ENABLED, consulte [Isolating Components](/windows/desktop/SbsCs/isolating-components).

2.  Inclua o arquivo de header de controle comum na origem do snap-in.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Adicione um arquivo chamado YourApp.manifest à árvore de origem que usa o formato de manifesto XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  Adicione o manifesto ao arquivo de recurso do snap-in. Consulte [Usando o ComCtl32 versão 6](/previous-versions//ms649781(v=vs.85)) em um aplicativo que usa extensões, plug-ins ou uma DLL que é trazido em um processo para obter detalhes sobre como adicionar um manifesto a um arquivo de recurso.

## <a name="turning-off-visual-styles"></a>Como desligar estilos visuais

Você pode desativar estilos visuais para um controle ou para todos os controles em uma janela chamando a [**função SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) da seguinte forma:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



No exemplo anterior, *hwnd é* o handle da janela na qual desabilitar estilos visuais. Após a chamada, o controle renderiza sem estilos visuais.

## <a name="using-visual-styles-with-html-content"></a>Usando estilos visuais com conteúdo HTML

As páginas HTML que modificam as folhas de estilos em cascata (CSS), como plano de fundo ou borda, não têm estilos visuais aplicados a elas. Eles exibem o atributo CSS especificado. Quando especificado como parte do conteúdo, a maioria das propriedades CSS se aplica a elementos que têm estilos visuais aplicados.

Por padrão, os estilos visuais são aplicados a controles HTML intrínsecos em páginas exibidas no Microsoft Internet Explorer 6 e versões posteriores. Para desativar estilos visuais para uma página HTML, adicione uma marca META ao <head> seção. Essa técnica também se aplica ao conteúdo empacotado como HTAs (aplicativos HTML). Para desativar estilos visuais, a marca META deve ser a seguinte:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Se a configuração do navegador e a configuração de marca não concordarem, a página não aplicará estilos visuais. Por exemplo, se a marca META estiver definida como "não" e o navegador estiver definido para habilitar estilos visuais, os estilos visuais não serão aplicados à página. No entanto, se o navegador ou a marca META estiver definido como "sim" e o outro item não for especificado, os estilos visuais serão aplicados.

 

Os estilos visuais podem alterar o layout do conteúdo. Além disso, se você definir determinados atributos em controles HTML intrínsecos, como a largura de um botão, poderá descobrir que o rótulo no botão é ilegível em determinados estilos visuais.

Você deve testar completamente seu conteúdo usando estilos visuais para determinar se a aplicação de estilos visuais tem um efeito adverso em seu conteúdo e layout.

## <a name="when-visual-styles-are-not-applied"></a>Quando estilos visuais não são aplicados

Para evitar a aplicação de estilos visuais a uma janela de nível superior, dê à janela uma região não nula (**SetWindowRgn**). O sistema presume que uma janela com uma região não NULL é uma janela especializada que não usa estilos visuais. Uma janela filho associada a uma janela de nível superior não visual-styles ainda pode aplicar estilos visuais, mesmo que a janela pai não aplique.

Se você quiser desabilitar o uso de estilos visuais para todas as janelas em seu aplicativo, chame [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) e não passe o sinalizador STAP \_ ALLOW \_ NONCLIENT. Se um aplicativo não chamar **SetThemeAppProperties**, os valores de sinalizador assumidos serão STAP \_ ALLOW \_ NONCLIENT \| STAP \_ ALLOW CONTROLS \_ \| STAP ALLOW \_ \_ WEBCONTENT. Os valores assumidos faz com que a área não dependente, os controles e o conteúdo da Web tenham um estilo visual aplicado.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Tornando seu aplicativo compatível com versões anteriores do Windows

Grande parte da arquitetura de estilo visual foi projetada para tornar mais simples continuar a enviar seu produto em versões anteriores do Windows que não suportam alterar a aparência dos controles. Ao enviar um aplicativo para mais de um sistema operacional, esteja ciente do seguinte:

-   Em versões do Windows anteriores Windows 8, os estilos visuais estão desligados quando o alto contraste está em. Para dar suporte a alto contraste, um aplicativo herdada que dá suporte a estilos visuais precisa fornecer um caminho de código separado para desenhar corretamente os elementos da interface do usuário em alto contraste. Em Windows 8, alto contraste faz parte dos estilos visuais; No entanto, um aplicativo Windows 8 (um que inclui o GUID do Windows 8 na seção de compatibilidade do manifesto do aplicativo) ainda precisa fornecer um caminho de código separado para renderizar corretamente em alto contraste no Windows 7 anteriormente.
-   Se você usar os recursos na ComCtl32.dll versão 6, como o controle de exibição de tile ou link, deverá lidar com o caso em que esses controles não estão disponíveis no computador do usuário. ComCtl32.dll versão 6 não é redistribuível.
-   Teste seu aplicativo para verificar se você não está contando com recursos do ComCtl32.dll versão 6 sem primeiro verificar a versão atual.
-   Não vincule a UxTheme.lib.
-   Escreva o código de tratamento de erros para instâncias quando os estilos visuais não funcionarem conforme o esperado.
-   Instalar o manifesto do aplicativo em versões anteriores não afetará a renderização de controles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 
