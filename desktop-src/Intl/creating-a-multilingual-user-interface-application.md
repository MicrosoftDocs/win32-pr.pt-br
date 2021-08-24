---
description: Este tutorial demonstra como usar um aplicativo monolíngue e torná-lo pronto para o mundo. Esse aplicativo está na forma de uma solução completa criada em Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: Adicionando Interface de Usuário Multilíngue suporte a um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5ca1ddba2574610cde1f375f7fab2b07461008665f2092c9c8e88ae9b51f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147689"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>Adicionando Interface de Usuário Multilíngue suporte a um aplicativo

Este tutorial demonstra como usar um aplicativo monolíngue e torná-lo pronto para o mundo. Esse aplicativo está na forma de uma solução completa criada em Microsoft Visual Studio.

-   [Visão geral](#splitting-the-various-language-resource-modules-an-overview)
    -   [A ideia por trás do Hello MUI](#the-idea-behind-hello-mui)
-   [Configurando a solução Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Requisitos da plataforma](#platform-requirements)
    -   [Pré-requisitos](#prerequisites)
-   [Etapa 0: Criando o Hello MUI codificado](#step-0-creating-the-hard-coded-hello-mui)
-   [Etapa 1: implementando o módulo de recurso básico](#step-1-implementing-the-basic-resource-module)
-   [Etapa 2: Criando o módulo de recurso básico](#step-2-building-the-basic-resource-module)
    -   [Dividindo os vários módulos de recursos de linguagem: uma visão geral](#splitting-the-various-language-resource-modules-an-overview)
    -   [Dividindo os vários módulos de recurso de linguagem: criando os arquivos](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Etapa 3: Criando um Resource-Savvy "Hello MUI"](#step-3-creating-a-resource-savvy-hello-mui)
-   [Etapa 4: Globalizando "Hello MUI"](#step-4-globalizing-hello-mui)
-   [Etapa 5: Personalização de "Hello MUI"](#step-5-customizing-hello-mui)
-   [Considerações adicionais sobre a MUI](#additional-considerations-for-mui)
    -   [Suporte para aplicativos de console](#support-for-console-applications)
    -   [Determinação de idiomas para dar suporte em tempo de executar](#determination-of-languages-to-support-at-run-time)
    -   [Suporte a script complexo em versões anteriores ao Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Resumo](#summary)

## <a name="overview"></a>Visão geral

A partir do Windows Vista, o próprio sistema operacional Windows foi criado desde o início para ser uma plataforma multilíngue, com suporte adicional que permite criar aplicativos multilíngues que usam o modelo de recurso Windows MUI.

Este tutorial ilustra esse novo suporte para aplicativos multilíngues abordando os seguintes aspectos:

-   Usa o suporte aprimorado da plataforma MUI para habilitar facilmente aplicativos multilíngues.
-   Estende aplicativos multilíngues para executar em versões do Windows antes do Windows Vista.
-   Aborda as considerações adicionais envolvidas no desenvolvimento de aplicativos multilíngues especializados, como aplicativos de console.

Esses links ajudam a fornecer uma atualização rápida sobre os conceitos sobre internacionalização e MUI:

-   [Visão geral rápida da internacionalização.](understanding-internationalization.md)
-   [Conceitos da MUI.](understanding-mui.md)
-   [Usando a MUI para desenvolver aplicativos Win32.](using-multilingual-user-interface.md)

### <a name="the-idea-behind-hello-mui"></a>A ideia por trás do Hello MUI

Você provavelmente está familiarizado com o aplicativo de Olá, Mundo clássico, que ilustra os conceitos básicos de programação. Este tutorial usa uma abordagem semelhante para ilustrar como usar o modelo de recurso da MUI para atualizar um aplicativo monolíngue para criar uma versão multilíngue chamada Hello MUI.

> [!Note]  
> As tarefas neste tutorial são descritas em etapas detalhadas devido à precisão com que essas atividades devem ser executadas e à necessidade de explicar os detalhes aos desenvolvedores que têm pouca experiência com essas tarefas.

 

## <a name="setting-up-the-hello-mui-solution"></a>Configurando a solução Hello MUI

Estas etapas descreve como se preparar para criar a solução Hello MUI.

### <a name="platform-requirements"></a>Requisitos de plataforma

Você deve compilar os exemplos de código neste tutorial usando o SDK (Software Development Kit) do Windows para Windows 7 e Visual Studio 2008. O SDK Windows 7 será instalado no Windows XP, Windows Vista e Windows 7, e a solução de exemplo pode ser criada em qualquer uma dessas versões do sistema operacional.

Todos os exemplos de código neste tutorial foram projetados para serem executados em versões x86 e x64 do Windows XP, Windows Vista e Windows 7. Partes específicas que não funcionarão no Windows XP são destacadas quando apropriado.

### <a name="prerequisites"></a>Pré-requisitos

1.  Instale Visual Studio 2008.

    Para obter mais informações, consulte o [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).

2.  Instale o Windows SDK do Windows 7.

    Você pode instalá-lo na página Windows SDK do [Windows Developer Center.](https://msdn.microsoft.com/windowsserver/bb980924.aspx) O SDK inclui utilitários para desenvolver aplicativos para versões do sistema operacional desde o Windows XP até o mais recente.

    > [!Note]  
    > Se você não estiver instalando o pacote no local padrão ou se não estiver instalando na unidade do sistema, que geralmente é a unidade C, anote o caminho de instalação.

     

3.  Configure os parâmetros Visual Studio linha de comando.

    1.  Abra uma Visual Studio de comando.
    2.  Caminho do **conjunto de tipos**.
    3.  Confirme se a variável de caminho inclui o caminho da pasta bin do SDK Windows 7: ... SDKs da Microsoft \\ Windows \\ compartimento v7.0 \\

4.  Instale o pacote de complemento de APIs de nível de baixo do Microsoft NLS.
    > [!Note]  
    > No contexto deste tutorial, esse pacote só será necessário se você estiver personalização do aplicativo para ser executado em versões Windows antes do Windows Vista. Consulte [Etapa 5: Personalização do Hello MUI.](#step-5-customizing-hello-mui)

     

    1.  Baixe e instale o pacote de seu [site de download](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).
    2.  Assim como acontece com o SDK do Windows, se você não estiver instalando o pacote no local padrão ou se não estiver instalando na unidade do sistema, que geralmente é a unidade C, anote o caminho de instalação.
    3.  Se sua plataforma de desenvolvimento Windows XP ou Windows Server 2003, confirme se Nlsdl.dll está instalado e registrado corretamente.

        1.  Navegue até a pasta "redist" no local do caminho de instalação.
        2.  Execute o Nlsdl redistribuível apropriado. \*.exe, como nlsdl.x86.exe. Esta etapa instala e registra Nlsdl.dll.

    > [!Note]  
    > Se você desenvolver um aplicativo que usa a MUI e que deve ser executado em versões Windows anteriores ao Windows Vista, o Nlsdl.dll deverá estar presente na plataforma Windows destino. Na maioria dos casos, isso significa que o aplicativo precisa carregar e instalar o instalador de Nlsdl redistribuível (e não simplesmente copiar Nlsdl.dll si mesmo).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Etapa 0: Criando o Hello MUI codificado

Este tutorial começa com a versão monolíngue do aplicativo Hello MUI. O aplicativo assume o uso da linguagem de programação C++, das cadeias de caracteres largos e da [**função MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) para saída.

Comece criando o aplicativo GuiStep 0 inicial, bem como a solução HelloMUI, que contém todos os \_ aplicativos neste tutorial.

1.  No Visual Studio 2008, crie um novo projeto. Use as seguintes configurações e valores:

    1.  Project tipo: em Visual C++ selecione Win32 e, em Visual Studio modelos instalados, selecione Win32 Project.
    2.  Nome: GuiStep \_ 0.
    3.  Local: *ProjectRootDirectory* (etapas posteriores referenciam este diretório).
    4.  Nome da solução: HelloMUI.
    5.  Selecione Criar diretório para a solução.
    6.  No Assistente de Aplicativo Win32, selecione o tipo de aplicativo padrão: Windows aplicativo.

2.  Configure o modelo de threading do projeto:

    1.  No Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep \_ 0 e selecione Propriedades.
    2.  Na caixa de diálogo Páginas de Propriedades do projeto:

        1.  Na lista de opções superior esquerda, de definir Configuração como Todas as Configurações.
        2.  Em Propriedades de Configuração, expanda C/C++, selecione Geração de Código e depure Biblioteca de Runtime: Depuração multi-threaded (/MTd).

3.  Substitua o conteúdo de GuiStep \_ 0.cpp pelo seguinte código:
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  Compile e execute o aplicativo.

O código-fonte simples acima faz a escolha de design simplista de codificação ou incorporação, toda a saída que o usuário verá– nesse caso, o texto "Hello MUI". Essa opção limita o utilitário do aplicativo para usuários que não reconhecem a palavra em inglês "Hello". Como a MUI é um acrônimo em inglês baseado em tecnologia, supõe-se neste tutorial que a cadeia de caracteres permaneça "MUI" para todos os idiomas.

## <a name="step-1-implementing-the-basic-resource-module"></a>Etapa 1: implementando o módulo de recurso básico

O Microsoft Win32 já expôs há muito tempo a capacidade de os desenvolvedores de aplicativos separarem seus dados de recurso de interface do usuário do código-fonte do aplicativo. Essa separação vem na forma do modelo de recurso Win32, no qual cadeias de caracteres, bitmaps, ícones, mensagens e outros itens normalmente exibidos para um usuário são empacotados em uma seção distinta do executável, separada do código executável.

Para ilustrar essa separação entre o código executável e o empacotamento de dados de recursos, nesta etapa, o tutorial coloca a cadeia de caracteres "Hello" codificada anteriormente (o recurso "en-US" ) na seção de recursos de um módulo DLL no projeto HelloModule \_ en \_ us.

Essa DLL do Win32 também pode conter a funcionalidade executável de tipo de biblioteca (como qualquer outra DLL pode. Mas, para ajudar a se concentrar nos aspectos relacionados a recursos do Win32, deixam o código DLL em tempo de run-time em dllmain.cpp. As seções subsequentes deste tutorial usam os dados de recurso HelloModule que estão sendo construídos aqui e também apresentam o código de runtime apropriado.

Para construir um módulo de recurso do Win32, comece criando uma DLL com um dllmain desalocado:

1.  Adicione um novo projeto à solução HelloMUI:

    1.  No menu Arquivo, selecione Adicionar e, em seguida, Novo Project.
    2.  Project tipo: Win32 Project.
    3.  Nome: HelloModule \_ en \_ US.
    4.  Local: *ProjectRootDirectory* \\ HelloMUI.
    5.  No assistente de aplicativo Win32, selecione tipo de aplicativo: DLL.

2.  Configure o modelo de Threading deste projeto:

    1.  Na Gerenciador de Soluções, clique com o botão direito do mouse no projeto HelloModule \_ en \_ US e selecione Propriedades.
    2.  Na caixa de diálogo páginas de propriedades do projeto:

        1.  Na lista suspensa superior esquerda, defina configuração para todas as configurações.
        2.  Em Propriedades de configuração, expanda C/C++, selecione geração de código e defina biblioteca de tempo de execução: depuração multi-threaded (/MTd).

3.  Examine DllMain. cpp. (Talvez você queira adicionar a referência não referenciada \_ Macros de parâmetro para o código gerado, como temos aqui, para permitir que ele seja compilado no nível de aviso 4.)
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  Adicione um arquivo de definição de recurso HelloModule. rc ao projeto:

    1.  No projeto HelloModule \_ \_ , clique com o botão direito do mouse na pasta arquivos de recursos e selecione Adicionar e, em seguida, selecione novo item.
    2.  Na caixa de diálogo Adicionar novo item, escolha o seguinte:

        1.  categorias: em Visual C++ selecione recurso e, em seguida, em "modelos Visual Studio instalados", selecione arquivo de recursos (. rc).
        2.  Nome: HelloModule.
        3.  Local: aceite o padrão.
        4.  Clique em Adicionar.

    3.  Especifique que o novo arquivo HelloModule. rc deve ser salvo como Unicode:

        1.  Na Gerenciador de Soluções, clique com o botão direito do mouse em HelloModule. rc e selecione Exibir código.
        2.  Se você vir uma mensagem informando que o arquivo já está aberto e perguntará se deseja fechá-lo, clique em Sim.
        3.  Com o arquivo exibido como texto, faça o arquivo de seleção de menu e as opções avançadas de salvamento.
        4.  Em codificação, especifique Unicode-CodePage 1200.
        5.  Clique em OK.
        6.  Salve e feche o HelloModule. rc.

    4.  Adicione uma tabela de cadeia de caracteres que contém a cadeia de caracteres "Olá":

        1.  Na Modo de Exibição de Recursos, clique com o botão direito do mouse em HelloModule. rc e selecione Adicionar recurso.
        2.  Selecione a tabela de cadeia de caracteres.
        3.  Clique em Novo.
        4.  Adicione uma cadeia de caracteres à tabela de cadeia de caracteres:

            1.  ID: Olá \_ MUI \_ Str \_ 0.
            2.  Valor: 0.
            3.  Legenda: Olá.

        Se você exibir HelloModule. rc como texto agora, verá várias partes do código-fonte específico do recurso. O maior interesse é a seção que descreve a cadeia de caracteres "Olá":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        Essa cadeia de caracteres "Olá" é o recurso que precisa ser localizado (ou seja, traduzido) em todas as linguagens que o aplicativo espera oferecer suporte. Por exemplo, o HelloModule \_ ta \_ no projeto (que você criará na próxima etapa) conterá sua própria versão localizada de HelloModule. rc para "ta-in":

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  Crie o \_ projeto HelloModule en \_ US para ter certeza de que não há erros.

5.  Crie mais seis projetos na solução HelloMUI (ou quantos quiser) para criar mais seis DLLs de recurso para idiomas adicionais. Use os valores nesta tabela:

    | Nome do projeto        | Nome do arquivo. rc | ID da Cadeia de Caracteres          | Valor da cadeia de caracteres | Legenda da cadeia de caracteres |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ de | HelloModule      | Olá \_ MUI \_ Str \_ 0 | 0            | Hallo          |
    | HelloModule \_ es \_ es | HelloModule      | Olá \_ MUI \_ Str \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | Olá \_ MUI \_ Str \_ 0 | 0            | Bonjour        |
    | HelloModule \_ Hi \_ | HelloModule      | Olá \_ MUI \_ Str \_ 0 | 0            | नमस्           |
    | HelloModule \_ ru \_ ru | HelloModule      | Olá \_ MUI \_ Str \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ ta \_ | HelloModule      | Olá \_ MUI \_ Str \_ 0 | 0            | வணக்கம்        |

    

     

Para obter mais informações sobre a estrutura e a sintaxe do arquivo. rc, consulte [About Resource files](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Etapa 2: criando o módulo de recurso básico

Usando modelos de recursos anteriores, a criação de qualquer um dos sete projetos HelloModule resultaria em sete DLLs separadas. Cada DLL contém uma seção de recursos com uma única cadeia de caracteres localizada no idioma apropriado. Embora apropriado para o modelo de recurso do Win32 histórico, esse design não aproveita o MUI.

no SDK do Windows Vista e posterior, o MUI fornece a capacidade de dividir os executáveis no código-fonte e nos módulos de conteúdo localizáveis. com a personalização adicional que é abordada posteriormente na etapa 5, os aplicativos podem ser habilitados para suporte multilíngue para execução em versões anteriores ao Windows Vista.

os principais mecanismos disponíveis para dividir os recursos do código executável, começando com o Windows Vista, são:

-   Usando rc.exe (o compilador RC) com opções específicas ou
-   Usando uma ferramenta de divisão de estilo de pós-compilação chamada muirct.exe.

Consulte [utilitários de recursos](resource-utilities.md) para obter mais informações.

Para simplificar, este tutorial usa muirct.exe para dividir o executável "Hello MUI".

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Dividindo os vários módulos de recursos de linguagem: uma visão geral

Um processo de várias partes é envolvido na divisão de DLLs em um executável HelloModule.dll, além de um HelloModule.dll. mui para cada um dos sete idiomas com suporte neste tutorial. Esta visão geral descreve as etapas necessárias; a próxima seção apresenta um arquivo de comando que executa essas etapas.

Primeiro, divida o módulo HelloModule.dll somente em inglês usando o comando:


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



A linha de comando acima usa o arquivo de configuração DoReverseMuiLoc. rcconfig. Esse tipo de arquivo de configuração normalmente é usado pelo muirct.exe para dividir os recursos entre a DLL do LN (linguagem neutra) e os arquivos. mui dependentes do idioma. Nesse caso, o arquivo XML DoReverseMuiLoc. rcconfig (listado na próxima seção) indica muitos tipos de recursos, mas todos eles se encaixam na categoria de arquivo "localizedResources" ou. mui, e não há recursos na categoria idioma neutro. Para obter mais informações sobre como preparar um arquivo de configuração de recurso, consulte [preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md).

Além de criar um arquivo HelloModule.dll. mui que contém a cadeia de caracteres em inglês "Olá", muirct.exe também insere um recurso MUI no módulo HelloModule.dll durante a divisão. Para carregar corretamente em tempo de execução os recursos apropriados dos módulos HelloModule.dll. mui específicos do idioma, cada arquivo. mui deve ter suas somas de verificação fixas para corresponder às somas de verificação no módulo LN da linguagem de linha de base neutro. Isso é feito por um comando como:


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



Da mesma forma, muirct.exe é invocado para criar um arquivo HelloModule.dll. mui para cada um dos outros idiomas. No entanto, nesses casos, a DLL neutra de idioma é descartada, pois apenas a primeira criada será necessária. Os comandos que processam os recursos em espanhol e francês têm a seguinte aparência:


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



Uma das coisas mais importantes a observar nas muirct.exe comando acima é que o sinalizador -x é usado para especificar uma ID de idioma de destino. O valor fornecido para muirct.exe é diferente para cada módulo específico HelloModule.dll idioma. Esse valor de linguagem é central e é usado por muirct.exe para marcar adequadamente o arquivo .mui durante a divisão. Um valor incorreto produz falhas de carregamento de recursos para esse arquivo .mui específico em tempo de executar. Consulte [Constantes e cadeias de caracteres](language-identifier-constants-and-strings.md) do identificador de idioma para obter mais detalhes sobre como mapear o nome do idioma para lCID.

Cada arquivo .mui dividido acaba sendo colocado em um diretório correspondente ao nome do idioma, imediatamente abaixo do diretório no qual o idioma neutro HelloModule.dll residirá. Para obter mais informações sobre o posicionamento do arquivo .mui, consulte [Implantação de aplicativo.](application-deployment.md)

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Dividindo os vários módulos de recurso de linguagem: criando os arquivos

Para este tutorial, você cria um arquivo de comando que contém os comandos para dividir as várias DLLs e o invoca manualmente. Observe que, no trabalho de desenvolvimento real, você pode reduzir o potencial de erros de build incluindo esses comandos como eventos de pré-build ou pós-build na solução HelloMUI, mas isso está além do escopo deste tutorial.

Crie os arquivos para o build de depuração:

1.  Crie um arquivo de comando DoReverseMuiLoc.cmd contendo os seguintes comandos:
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  Crie um arquivo xml DoReverseMuiLoc.rcconfig contendo as seguintes linhas:
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  Copie DoReverseMuiLoc.cmd e DoReverseMuiLoc.rcconfig para *ProjectRootDirectory* \\ HelloMUI \\ Debug.
4.  Abra o prompt Visual Studio 2008 e navegue até o diretório Depurar.
5.  Execute DoReverseMuiLoc.cmd.

Ao criar um build de versão, copie os mesmos arquivos DoReverseMuiLoc.cmd e DoReverseMuiLoc.rcconfig para o diretório Release e execute o arquivo de comando lá.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Etapa 3: Criando um Resource-Savvy "Hello MUI"

Com base no exemplo inicial codificado do GuiStep0.exe acima, você pode estender o alcance do aplicativo para vários usuários de linguagem escolhendo incorporar o modelo de recurso \_ win32. O novo código em tempo de run time apresentado nesta etapa inclui o carregamento do módulo ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) e a lógica de recuperação de cadeia de caracteres ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  Adicione um novo projeto à solução HelloMUI (usando a seleção de menu Arquivo, Adicionar e Novo Project) com as seguintes configurações e valores:

    1.  Project tipo: Win32 Project.
    2.  Nome: GuiStep \_ 1.
    3.  Local: aceite o padrão.
    4.  No Assistente de Aplicativo Win32, selecione o tipo de aplicativo padrão: Windows aplicativo.

2.  De definir este projeto para ser executado de dentro Visual Studio e configurar seu modelo de threading:

    1.  No Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep 1 e \_ selecione Definir como Iniciar Project.
    2.  Clique com o botão direito do mouse nele novamente e selecione Propriedades.
    3.  Na caixa de diálogo Páginas de Propriedades do projeto:

        1.  Na lista de opções superior esquerda, de definir Configuração como Todas as Configurações.
        2.  Em Propriedades de Configuração, expanda C/C++, selecione Geração de Código e depure Biblioteca de Runtime: Depuração multi-threaded (/MTd).

3.  Substitua o conteúdo de GuiStep \_ 1.cpp pelo seguinte código:
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  Compile e execute o aplicativo. A saída será exibida no idioma atualmente definido como o idioma de exibição do computador (desde que seja um dos sete idiomas que criarmos).

## <a name="step-4-globalizing-hello-mui"></a>Etapa 4: Globalizando "Hello MUI"

Embora o exemplo anterior seja capaz de exibir sua saída em idiomas diferentes, ele fica aquém em várias áreas. Talvez o mais perceptível seja que o aplicativo só esteja disponível em um pequeno subconjunto de idiomas quando comparado ao sistema operacional Windows em si. Se, por exemplo, o aplicativo GuiStep 1 da etapa anterior tiver sido instalado em um build japonês do Windows, as falhas de local do recurso \_ provavelmente serão.

Para resolver essa situação, você tem duas opções principais:

-   Verifique se os recursos em uma linguagem de fallback final predeterminada estão incluídos.
-   Forneça uma maneira para o usuário final configurar suas preferências de idioma entre o subconjunto de idiomas especificamente com suporte pelo aplicativo.

Entre essas opções, a que fornece uma linguagem de fallback final é altamente aconselhável e é implementada neste tutorial passando o sinalizador -g para muirct.exe, conforme visto acima. Esse sinalizador muirct.exe para tornar um idioma específico (de-DE/0x0407) o idioma de fallback final associado ao módulo DLL neutro em idioma (HelloModule.dll). Em tempo de executar, esse parâmetro é usado como último recurso para gerar texto a ser exibido para o usuário. Caso um idioma de fallback final não seja encontrado e nenhum recurso apropriado está disponível no binário com neutralidade de idioma, o carregamento do recurso falha. Portanto, você deve determinar cuidadosamente os cenários que seu aplicativo pode encontrar e planejar o idioma de fallback final de acordo.

A outra opção de permitir preferências de idioma configuráveis e carregar recursos com base nessa hierarquia definida pelo usuário pode aumentar muito a satisfação do cliente. Infelizmente, isso também complica a funcionalidade necessária no aplicativo.

Esta etapa do tutorial usa um mecanismo de arquivo de texto simplificado para habilitar a configuração de idioma do usuário personalizada. O arquivo de texto é analisado em tempo de executar pelo aplicativo e a lista de idiomas analisados e validados é usada para estabelecer uma lista de fallback personalizada. Depois que a lista de fallback personalizada for estabelecida, as APIs de Windows carregarão recursos de acordo com a precedência de idioma definida nesta lista. O restante do código é semelhante ao encontrado na etapa anterior.

1.  Adicione um novo projeto à solução HelloMUI (usando a seleção de menu Arquivo, Adicionar e Novo Project) com as seguintes configurações e valores:

    1.  Project tipo: Win32 Project.
    2.  Nome: GuiStep \_ 2.
    3.  Local: aceite o padrão.
    4.  No Assistente de Aplicativo Win32, selecione o tipo de aplicativo padrão: Windows aplicativo.

2.  De definir este projeto para ser executado de dentro Visual Studio e configurar seu modelo de threading:

    1.  No Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep 2 e \_ selecione Definir como Iniciar Project.
    2.  Clique com o botão direito do mouse nele novamente e selecione Propriedades.
    3.  Na caixa de diálogo Páginas de Propriedades do projeto:

        1.  Na lista de opções superior esquerda, de definir Configuração como Todas as Configurações.
        2.  Em Propriedades de Configuração, expanda C/C++, selecione Geração de Código e depure Biblioteca de Runtime: Depuração multi-threaded (/MTd).

3.  Substitua o conteúdo de GuiStep \_ 2.cpp pelo seguinte código:
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Crie um arquivo de texto Unicode langs.txt que contém a seguinte linha:

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Salve o arquivo como Unicode.

     

    Copie langs.txt para o diretório do qual o programa será executado:

    -   Se estiver executando de dentro Visual Studio, copie-o para *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   Se estiver executando Windows Explorer, copie-o para o mesmo diretório que GuiStep \_2.exe.

5.  Compile e execute o projeto. Tente editar langs.txt para que idiomas diferentes apareçam na frente da lista.

## <a name="step-5-customizing-hello-mui"></a>Etapa 5: Personalização de "Hello MUI"

Vários recursos de tempo de run time mencionados até agora neste tutorial estão disponíveis somente no Windows Vista e posterior. Talvez você queira usar o esforço aplicado na localização e na divisão de recursos fazendo com que o aplicativo funcione em versões de sistema operacional de nível Windows, como Windows XP. Esse processo envolve ajustar o exemplo anterior em duas áreas principais:

-   As funções de carregamento de recursos Windows Vista pré-Windows (como [**LoadString,**](/windows/win32/api/winuser/nf-winuser-loadstringa) [**LoadIcon,**](/windows/win32/api/winuser/nf-winuser-loadicona) [**LoadBitmap,**](/windows/win32/api/winuser/nf-winuser-loadbitmapa) [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)e outras) não têm conhecimento da MUI. Os aplicativos que são fornecidas com recursos divididos (arquivos LN e .mui) devem carregar módulos de recurso usando uma destas duas funções:

    -   Se o aplicativo deve ser executado somente no Windows Vista e posterior, ele deve carregar módulos de recurso com [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).
    -   Se o aplicativo deve ser executado em versões anteriores ao Windows Vista, bem como no vista do Windows ou posterior, ele deve usar [**LoadMUILibrary,**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)que é uma função de nível downlevel específica fornecida no SDK do Windows 7.

-   O gerenciamento de linguagem e o suporte à ordem de fallback de idioma oferecidos em versões anteriores do Windows Vista do sistema operacional Windows diferem significativamente do que no Windows Vista e posterior. Por esse motivo, os aplicativos que permitem o fallback de idioma configurado pelo usuário devem ajustar suas práticas de gerenciamento de idioma:

    -   Se o aplicativo deve ser executado somente no Windows Vista e posterior, definir a lista de idiomas usando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) é suficiente.
    -   Se o aplicativo deve ser executado em todas as versões Windows, o código deve ser construído que será executado em plataformas de nível baixo para iterar por meio da lista de idiomas configurada pelo usuário e da investigação do módulo de recurso desejado. Isso pode ser visto nas seções 1c e 2 do código fornecido posteriormente nesta etapa.

Crie um projeto que possa usar os módulos de recursos localizados em qualquer versão do Windows:

1.  Adicione um novo projeto à solução HelloMUI (usando a seleção de menu Arquivo, Adicionar e Novo Project) com as seguintes configurações e valores:

    1.  Project tipo: Win32 Project.
    2.  Nome: GuiStep \_ 3.
    3.  Local: aceite o padrão.
    4.  No Assistente de Aplicativo Win32, selecione o tipo de aplicativo padrão: Windows aplicativo.

2.  De definir esse projeto para ser executado de dentro Visual Studio e configurar seu modelo de threading. Além disso, configure-o para adicionar os bibliotecas e os headers necessários.

    > [!Note]  
    > Os caminhos usados neste tutorial supõem que o SDK do Windows 7 e o pacote de APIs de nível de baixo do Microsoft NLS foram instalados em seus diretórios padrão. Se esse não for o caso, modifique os caminhos adequadamente.

     

    1.  No Gerenciador de Soluções, clique com o botão direito do mouse no projeto GuiStep 3 e \_ selecione Definir como Iniciar Project.
    2.  Clique com o botão direito do mouse nele novamente e selecione Propriedades.
    3.  Na caixa de diálogo Páginas de Propriedades do projeto:

        1.  Na lista de opções superior esquerda, de definir Configuração como Todas as Configurações.
        2.  Em Propriedades de Configuração, expanda C/C++, selecione Geração de Código e depure Biblioteca de Runtime: Depuração multi-threaded (/MTd).
        3.  Selecione Geral e adicione a Diretórios de Inclusão Adicionais:

            -   "C: as \\ APIs de nível inferior do Microsoft NLS \\ incluem".

        4.  Selecione idioma e defina tratar WCHAR \_ t como tipo interno: não (/Zc: WCHAR \_ t-).
        5.  Selecione avançado e defina a Convenção de chamada: \_ stdcall (/gz).
        6.  Em Propriedades de configuração, expanda vinculador, selecione entrada e adicionar a dependências adicionais:

            -   "C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Lib \\ MUILoad. lib".
            -   "C: \\ APIs de nível inferior da Microsoft NLS \\ \\ x86 \\ nlsdl. lib".

3.  Substitua o conteúdo de GuiStep \_ 3. cpp pelo código a seguir:
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Crie ou copie langs.txt para o diretório apropriado, conforme descrito anteriormente na [etapa 4: Globalizando "Hello mui"](#step-4-globalizing-hello-mui).
5.  Compile e execute o projeto.

> [!Note]  
> se o aplicativo deve ser executado em versões do Windows anteriores ao Windows Vista, leia os documentos que vieram com o pacote de [APIs de nível inferior do Microsoft NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) sobre como redistribuir Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Considerações adicionais sobre o MUI

### <a name="support-for-console-applications"></a>Suporte para aplicativos de console

As técnicas abordadas neste tutorial também podem ser usadas em aplicativos de console. no entanto, ao contrário da maioria dos controles de GUI padrão, a Windows janela de comando não pode exibir caracteres para todos os idiomas. Por esse motivo, os aplicativos de console multilíngües exigem atenção especial.

Chamar as APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) ou [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) com sinalizadores de filtragem específicos faz com que as funções de carregamento de recursos removam as investigações de recursos de idioma para linguagens específicas que normalmente não são exibidas em uma janela de comando. Quando esses sinalizadores são definidos, os algoritmos de configuração de idioma permitem apenas os idiomas que serão exibidos corretamente na janela de comando para que fiquem na lista de fallback.

Para obter mais informações sobre como usar essas APIs para criar um aplicativo de console multilíngüe, consulte as seções comentários de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) e [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Determinação de idiomas para suporte em Run-Time

Você pode adotar uma das seguintes sugestões de design para determinar em quais idiomas seu aplicativo deve dar suporte em tempo de execução:

-   **Durante a instalação, habilite o usuário final para selecionar o idioma preferencial em uma lista de idiomas com suporte**

-   **Ler uma lista de idiomas de um arquivo de configuração**

    Alguns dos projetos neste tutorial contêm uma função usada para analisar um arquivo de configuração langs.txt, que contém uma lista de idiomas.

    Como essa função usa entrada externa, valide os idiomas que são fornecidos como entrada. Consulte as funções [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) ou [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) para obter mais detalhes sobre como executar essa validação.

-   **Consultar o sistema operacional para determinar quais idiomas estão instalados**

    Essa abordagem ajuda o aplicativo a usar o mesmo idioma que o sistema operacional. Embora isso não exija a solicitação do usuário, se você escolher essa opção, lembre-se de que os idiomas do sistema operacional podem ser adicionados ou removidos a qualquer momento e podem ser alterados após o usuário instalar o aplicativo. Além disso, lembre-se de que, em alguns casos, o sistema operacional é instalado com suporte a idiomas limitados e o aplicativo oferece mais valor se oferecer suporte a idiomas para os quais o sistema operacional não oferece suporte.

    Para obter mais informações sobre como determinar os idiomas atualmente instalados no sistema operacional, consulte a função [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>suporte a scripts complexos em versões anteriores ao Windows Vista

quando um aplicativo que dá suporte a determinados scripts complexos é executado em uma versão do Windows antes do Windows Vista, o texto nesse script pode não ser exibido corretamente em componentes de GUI. Por exemplo, no projeto de nível inferior neste tutorial, os scripts de hi-IN e ta-IN podem não ser exibidos na caixa de mensagem devido a problemas com o processamento de scripts complexos e a falta de fontes relacionadas. Normalmente, os problemas dessa natureza se apresentam como caixas quadradas no componente da GUI.

Mais informações sobre como habilitar o processamento de script complexo podem ser encontradas em [suporte a scripts e fontes no Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Resumo

Este tutorial globalizava um aplicativo multilíngue e demonstrou as práticas recomendadas a seguir.

-   Projete o aplicativo para aproveitar o modelo de recurso do Win32.
-   Utilize a divisão de recursos do MUI em binários satélite (arquivos. mui).
-   Verifique se o processo de localização atualiza os recursos nos arquivos. mui para que sejam apropriados para o idioma de destino.
-   Certifique-se de que o empacotamento e a implantação do aplicativo, arquivos. mui associados e conteúdo de configuração seja feito corretamente para permitir que as APIs de carregamento de recursos localizem o conteúdo localizado.
-   Forneça ao usuário final um mecanismo para ajustar a configuração de idioma do aplicativo.
-   Ajuste o código de tempo de execução para aproveitar a configuração da linguagem, para tornar o aplicativo mais responsivo às necessidades dos usuários finais.

 

 
