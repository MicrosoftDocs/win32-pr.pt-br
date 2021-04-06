---
title: Habilitar estilos visuais
description: Este tópico explica como configurar seu aplicativo para garantir que os controles comuns sejam exibidos no estilo visual preferencial do usuário.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39339c0535767011a59730534486604389f62468
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917743"
---
# <a name="enabling-visual-styles"></a>Habilitar estilos visuais

Este tópico explica como configurar seu aplicativo para garantir que os controles comuns sejam exibidos no estilo visual preferencial do usuário.

Este tópico inclui as seções a seguir.

-   [Usando manifestos ou diretivas para garantir que os estilos visuais possam ser aplicados a aplicativos](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Usando ComCtl32.dll versão 6 em um aplicativo que usa apenas extensões padrão](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [Usando o ComCtl32 versão 6 no painel de controle ou uma DLL que é executada pelo RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Adicionando suporte ao estilo visual a uma extensão, plug-in, snap-in do MMC ou uma DLL que é colocada em um processo](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Desativando estilos visuais](#turning-off-visual-styles)
-   [Usando estilos visuais com conteúdo HTML](#using-visual-styles-with-html-content)
-   [Quando os estilos visuais não são aplicados](#when-visual-styles-are-not-applied)
-   [Tornando seu aplicativo compatível com versões anteriores do Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Tópicos relacionados](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Usando manifestos ou diretivas para garantir que os estilos visuais possam ser aplicados a aplicativos

Para habilitar seu aplicativo a usar estilos visuais, você deve usar ComCtl32.dll versão 6 ou posterior. Como a versão 6 não é redistribuível, ela estará disponível somente quando o aplicativo estiver em execução em uma versão do Windows que a contém. O Windows é fornecido com a versão 5 e a versão 6. ComCtl32.dll versão 6 contém os controles de usuário e os controles comuns. Por padrão, os aplicativos usam os controles de usuário definidos em User32.dll e os controles comuns definidos no ComCtl32.dll versão 5. Para obter uma lista de versões de DLL e suas plataformas de distribuição, consulte [versões de controle comuns](common-control-versions.md).

Se você quiser que seu aplicativo use estilos visuais, você deve adicionar um manifesto de aplicativo ou uma diretiva de compilador que indica que ComCtl32.dll versão 6 deve ser usada se estiver disponível.

Um manifesto de aplicativo permite que um aplicativo especifique quais versões de um assembly ele exige. No Microsoft Win32, um assembly é um conjunto de DLLs e uma lista de objetos com versão que estão contidos nessas DLLs.

Os manifestos são gravados em XML. O nome do arquivo de manifesto do aplicativo é o nome do seu executável seguido pela extensão de nome de arquivo. manifest; por exemplo, MyApp.exe. manifest. O manifesto de exemplo a seguir mostra que a primeira seção descreve o próprio manifesto. A tabela a seguir mostra os atributos definidos pelo elemento **AssemblyIdentity** na seção de descrição do manifesto.



| Atributo             | Descrição                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Versão do manifesto. A versão deve estar no formato Major. Minor. Revision. Build (ou seja, n. n. n. n, em que n <= 65535). |
| processorArchitecture | Processador para o qual seu aplicativo é desenvolvido.                                                                          |
| name                  | Inclui o nome da empresa, o nome do produto e o nome do aplicativo.                                                                   |
| tipo                  | Tipo de seu aplicativo, como Win32.                                                                                    |



 

O manifesto de exemplo também fornece uma descrição do seu aplicativo e especifica as dependências do aplicativo. A tabela a seguir mostra os atributos definidos pelo elemento **AssemblyIdentity** na seção de dependência.



| Atributo             | Descrição                                      |
|-----------------------|--------------------------------------------------|
| type                  | Tipo do componente de dependência, como Win32. |
| name                  | Nome do componente.                           |
| version               | A versão do componente.                        |
| processorArchitecture | Processador para o qual o componente foi projetado.    |
| publicKeyToken        | Token de chave usado com este componente.              |
| Linguagem              | Idioma do componente.                       |



 

Veja a seguir um exemplo de um arquivo de manifesto.

> [!IMPORTANT]
> Defina a entrada **ProcessorArchitecture** como **"x86"** se seu aplicativo for direcionado para a plataforma Windows de 32 bits ou para **"amd64"** se seu aplicativo for direcionado para a plataforma de 64 bits do Windows. Você também pode especificar **" \* "**, que garante que todas as plataformas sejam direcionadas, conforme mostrado nos exemplos a seguir.

 


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



Se você estiver usando o Microsoft Visual C++ 2005 ou posterior, poderá adicionar a seguinte diretiva de compilador ao código-fonte em vez de criar um manifesto manualmente. Para facilitar a leitura, a diretiva é dividida em várias linhas aqui.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



Os tópicos a seguir descrevem as etapas para aplicar estilos visuais a diferentes tipos de aplicativos. Observe que o formato do manifesto é o mesmo em cada caso.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Usando ComCtl32.dll versão 6 em um aplicativo que usa apenas extensões padrão

Veja a seguir exemplos de aplicativos que não usam extensões de terceiros.

-   Calculator
-   FreeCell
-   Campo
-   Bloco de notas
-   Paciência

**Para criar um manifesto e habilitar seu aplicativo para usar estilos visuais.**

1.  Link para ComCtl32. lib e chame [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Adicione um arquivo chamado YourApp.exe. manifest à sua árvore de origem que tem o formato de manifesto XML.
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

    

3.  Adicione o manifesto ao arquivo de recurso do aplicativo da seguinte maneira:
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Ao adicionar a entrada anterior ao recurso, você deve formatá-la em uma linha. Como alternativa, você pode posicionar o arquivo de manifesto XML no mesmo diretório que o arquivo executável do seu aplicativo. O sistema operacional carregará o manifesto do sistema de arquivos primeiro e, em seguida, verificará a seção de recursos do executável. A versão do sistema de arquivos tem precedência.

     

Quando você criar seu aplicativo, o manifesto será adicionado como um recurso binário.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>Usando o ComCtl32 versão 6 no painel de controle ou uma DLL que é executada pelo RunDll32.exe

**Para criar um manifesto e habilitar seu aplicativo para usar estilos visuais.**

1.  Link para ComCtl32. lib e chame [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Adicione um arquivo chamado YourApp.cpl. manifest à sua árvore de origem que tem o formato de manifesto XML.
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
> Ao criar um aplicativo do painel de controle, coloque-o na categoria apropriada. O painel de controle agora dá suporte à categorização de aplicativos do painel de controle. Isso significa que os aplicativos do painel de controle podem ser atribuídos a identificadores e separados em áreas de tarefas, como adicionar ou remover programas, aparência e temas ou data, hora, idioma e opções regionais.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Adicionando suporte ao estilo visual a uma extensão, plug-in, snap-in do MMC ou uma DLL que é colocada em um processo

O suporte para estilos visuais pode ser adicionado a uma extensão, plug-in, snap-in do MMC ou uma DLL que é colocada em um processo. Por exemplo, use as etapas a seguir para adicionar suporte a estilos visuais para um snap-in do MMC (console de gerenciamento Microsoft).

1.  Compile seu snap-in com o sinalizador habilitado para reconhecimento de-DISOLATION \_ \_ ou insira a instrução a seguir antes da \# inclusão da instrução "Windows. h".

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Para obter mais informações sobre o reconhecimento de isolamento \_ \_ habilitado, consulte [isolando componentes](/windows/desktop/SbsCs/isolating-components).

2.  Inclua o arquivo de cabeçalho de controle comum em sua fonte de snap-in.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Adicione um arquivo chamado YourApp. manifest à sua árvore de origem que usa o formato de manifesto XML.
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

    

4.  Adicione o manifesto ao arquivo de recurso do snap-in. Consulte [usando o comctl32 versão 6 em um aplicativo que usa extensões, plug-ins ou uma DLL que é colocada em um processo](/previous-versions//ms649781(v=vs.85)) para obter detalhes sobre como adicionar um manifesto a um arquivo de recurso.

## <a name="turning-off-visual-styles"></a>Desativando estilos visuais

Você pode desativar os estilos visuais de um controle ou de todos os controles em uma janela chamando a função [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) da seguinte maneira:


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



No exemplo anterior, *HWND* é o identificador da janela na qual os estilos visuais serão desabilitados. Após a chamada, o controle é renderizado sem estilos visuais.

## <a name="using-visual-styles-with-html-content"></a>Usando estilos visuais com conteúdo HTML

As páginas HTML que modificam as propriedades de folhas de estilos em cascata (CSS), como plano de fundo ou borda, não têm estilos visuais aplicados a elas. Eles exibem o atributo CSS especificado. Quando especificado como parte do conteúdo, a maioria das propriedades de CSS se aplica a elementos que têm estilos visuais aplicados.

Por padrão, os estilos visuais são aplicados aos controles HTML intrínsecos nas páginas exibidas no Microsoft Internet Explorer 6 e versões posteriores. Para desativar os estilos visuais de uma página HTML, adicione uma marca META ao <head> seção. Essa técnica também se aplica ao conteúdo empacotado como aplicativos HTML (HTAs). Para desativar os estilos visuais, a marca META deve ser a seguinte:


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Se a configuração do navegador e a configuração de marca não forem aceitas, a página não aplicará estilos visuais. Por exemplo, se a marca META for definida como "não" e o navegador estiver definido para Habilitar estilos visuais, os estilos visuais não serão aplicados à página. No entanto, se o navegador ou a marca META for definido como "Yes" e o outro item não for especificado, os estilos visuais serão aplicados.

 

Estilos visuais podem alterar o layout do seu conteúdo. Além disso, se você definir determinados atributos em controles HTML intrínsecos, como a largura de um botão, poderá descobrir que o rótulo no botão está ilegível em determinados estilos visuais.

Você deve testar exaustivamente seu conteúdo usando estilos visuais para determinar se a aplicação de estilos visuais tem um efeito adverso no seu conteúdo e layout.

## <a name="when-visual-styles-are-not-applied"></a>Quando os estilos visuais não são aplicados

Para evitar a aplicação de estilos visuais a uma janela de nível superior, dê à janela uma região não nula (**SetWindowRgn**). O sistema pressupõe que uma janela com uma região não nula é uma janela especializada que não usa estilos visuais. Uma janela filho associada a uma janela de nível superior de estilos não visuais ainda pode aplicar estilos visuais, mesmo que a janela pai não tenha.

Se você quiser desabilitar o uso de estilos visuais para todas as janelas em seu aplicativo, chame [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) e não passe o sinalizador STAP \_ Allow \_ unclient. Se um aplicativo não chamar **SetThemeAppProperties**, os valores de sinalizador presumidos serão STAP permitir que não \_ \_ clientes \| STAP \_ permitir \_ controles \| STAP \_ permitir \_ webcontent. Os valores presumidos fazem com que a área não cliente, os controles e o conteúdo da Web tenham um estilo visual aplicado.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Tornando seu aplicativo compatível com versões anteriores do Windows

Grande parte da arquitetura de estilo visual foi projetada para simplificar a entrega de seu produto em versões anteriores do Windows que não dão suporte à alteração da aparência dos controles. Ao enviar um aplicativo para mais de um sistema operacional, lembre-se do seguinte:

-   Em versões do Windows anteriores ao Windows 8, os estilos visuais ficam desativados quando o alto contraste está ativado. Para dar suporte a alto contraste, um aplicativo herdado que dá suporte a estilos visuais precisa fornecer um caminho de código separado para desenhar corretamente elementos de interface do usuário em alto contraste. No Windows 8, o alto contraste é uma parte dos estilos visuais; no entanto, um aplicativo do Windows 8 (que inclui o GUID do Windows 8 na seção de compatibilidade de seu manifesto do aplicativo) ainda precisa fornecer um caminho de código separado para ser renderizado corretamente em alto contraste no Windows 7 anteriormente.
-   Se você usar os recursos do ComCtl32.dll versão 6, como o modo de exibição de bloco ou de link, deverá lidar com o caso em que esses controles não estão disponíveis no computador do usuário. ComCtl32.dll versão 6 não é redistribuível.
-   Teste seu aplicativo para certificar-se de que você não está contando com os recursos do ComCtl32.dll versão 6 sem primeiro verificar a versão atual.
-   Não vincule a UxTheme. lib.
-   Grave o código de tratamento de erros para instâncias quando os estilos visuais não funcionarem conforme o esperado.
-   Instalar o manifesto do aplicativo em versões anteriores não afetará a renderização de controles.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estilos visuais](themes-overview.md)
</dt> </dl>

 

 