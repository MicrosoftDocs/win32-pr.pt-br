---
title: Usando BITS do .NET usando DLLs de referência
description: Os exemplos a seguir mostram como chamar a interface COM do BITS a partir de um programa .NET
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103638929"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Chamando em BITS do .NET e do C# usando DLLs de referência

Uma maneira de chamar as classes COM de um programa .NET é criar um arquivo DLL de referência começando com os arquivos de [IDL](/windows/desktop/Midl/midl-start-page) do bits (linguagem de definição de interface) no SDK do Windows, usando as ferramentas [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) e [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) . A DLL de referência é um conjunto de wrappers de classe para as classes COM de BITS; Você pode usar as classes de wrapper diretamente do .NET.

Uma alternativa ao uso de DLLs de referência criadas automaticamente é usar um wrapper de BITS .NET de terceiros do [GitHub](https://github.com/) e do [NuGet](https://www.nuget.org/). Esses wrappers geralmente têm um estilo de programação .NET mais natural, mas podem atrasar por trás das alterações e atualizações nas interfaces do BITS.

## <a name="creating-the-reference-dlls"></a>Criando DLLs de referência
### <a name="bits-idl-files"></a>Arquivos IDL de BITS

Você começará com o conjunto de arquivos IDL do BITS. Esses são arquivos que definem totalmente a interface COM do BITS. Os arquivos estão localizados no diretório de **kits do Windows** e são chamados bits *version*. idl (por exemplo, bits10_2. idl), exceto para o arquivo da versão 1,0, que é apenas bits. idl. À medida que novas versões de BITS são criadas, novos arquivos IDL de BITS também são criados.

Talvez você também queira modificar uma cópia dos arquivos IDL do BITS do SDK para usar os recursos do BITS que não são convertidos automaticamente em equivalentes do .NET. As alterações de arquivo IDL possíveis serão discutidas posteriormente.

Os arquivos IDL do BITS incluem vários outros arquivos IDL por referência. Elas também se aninham, de modo que, se você usar uma versão, ela incluirá todas as versões mais baixas.

Para cada versão do BITS que você deseja direcionar em seu programa, você precisará de uma DLL de referência para essa versão. Por exemplo, se você quiser escrever um programa que funcione em BITS 1,5 e superior, mas tenha recursos adicionais quando o BITS 10,2 estiver presente, será necessário converter os arquivos bits1_5. idl e bits10_2. idl.


### <a name="midl-and-tlbimp-utilities"></a>Utilitários MIDL e TLBIMP

O utilitário [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (linguagem IDL da Microsoft) converte os arquivos IDL que descrevem a interface com do bits em um arquivo TLB (biblioteca de tipos). A ferramenta MIDL depende do utilitário CL (pré-processador de C) para ler corretamente o arquivo de idioma IDL. O utilitário CL faz parte do Visual Studio e é instalado quando você inclui recursos do C/C++ na instalação do Visual Studio.

Normalmente, o utilitário MIDL criará um conjunto de arquivos C e H (código de linguagem C e cabeçalho de linguagem C). Você pode suprimir esses arquivos extras enviando a saída para o dispositivo NUL:. Por exemplo, definir o/dlldata nomedearquivo NUL: switch irá suprimir a criação de um arquivo dlldata. c. Os comandos de exemplo abaixo mostram quais opções devem ser definidas como NUL:.

O utilitário [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (tipo de importador de biblioteca de tipos) lê em um arquivo tlb e cria o arquivo DLL de referência correspondente. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Comandos de exemplo para MIDL e TLBIMP

Este é um exemplo do conjunto completo de comandos para gerar um conjunto de arquivos de referência. Talvez seja necessário modificar os comandos com base em seu Visual Studio e SDK do Windows instalação e com base nos recursos do BITS e nas versões do sistema operacional que você está direcionando. 

O exemplo cria um diretório para posicionar os arquivos DLL de referência e cria uma variável de ambiente BITSTEMP para apontar para esse diretório. 

Os comandos de exemplo executam o arquivo vsdevcmd.bat que é criado pelo instalador do Visual Studio. Esse arquivo BAT irá configurar seus caminhos e algumas variáveis de ambiente para que os comandos MIDL e TLBIMP sejam executados. Ele também configura as variáveis WindowsSdkDir e WindowsSDKLibVersion para apontar para os diretórios de SDK do Windows mais recentes.

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
Depois que esses comandos forem executados, você terá um conjunto de DLLs de referência no diretório BITSTEMP.

### <a name="adding-the-reference-dlls-to-your-project"></a>Adicionando as DLLs de referência ao seu projeto

Para usar uma DLL de referência em um projeto C#, abra seu projeto C# no Visual Studio. Na Gerenciador de Soluções, clique com o botão direito do mouse nas referências e clique em Adicionar referência. Em seguida, clique no botão procurar e, em seguida, no botão Adicionar. Navegue até o diretório com as DLLs de referência, selecione-as e clique em Adicionar. Na janela Gerenciador de referências, as DLLs de referência serão verificadas. Em seguida, clique em OK.

As DLLs de referência do BITS agora são adicionadas ao seu projeto.

As informações nos arquivos DLL de referência serão inseridas em seu programa final. Você não precisa enviar os arquivos DLL de referência com seu programa; Você só precisa enviar o. EXE. 

Você pode alterar se as DLLs de referência estão incorporadas ao EXE final. Use a propriedade [inserir tipos de interoperabilidade](/dotnet/framework/interop/how-to-add-references-to-type-libraries) para definir se as DLLs de referência serão inseridas ou não. Isso pode ser feito de acordo com a referência. O padrão é true para inserir as DLLs.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Modificando arquivos IDL para obter um código .NET mais completo

Os arquivos IDL (linguagem IDL da Microsoft) BITS podem ser usados inalterados para criar o arquivo DLL BackgroundCopyManager. No entanto, a DLL de referência .NET resultante não terá algumas uniões irtraduzidas e terá nomes difíceis de usar para algumas estruturas e enumerações. Esta seção descreve algumas das alterações que você pode fazer para tornar a DLL do .NET mais completa e mais fácil de usar.

### <a name="simpler-enum-names"></a>Nomes de enumeração mais simples

Os arquivos IDL do BITS geralmente definem valores de enumeração como este:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
O BG_AUTH_TARGET é o nome do typedef; o enum real não é nomeado. Isso normalmente não causa problemas com o código C, mas não se traduz bem para uso com um programa .NET. Um novo nome será criado automaticamente, mas poderá ser algo parecido com _MIDL___MIDL_itf_bits4_0_0005_0001_0001 em vez de um valor legível por humanos. Você pode corrigir esse problema atualizando os arquivos MIDL para incluir um nome de enumeração.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

O nome de enumeração pode ser igual ao nome do typedef. Alguns programadores têm uma Convenção de nomenclatura onde são mantidos diferentes (por exemplo, colocando um sublinhado antes do nome da enumeração), mas isso apenas confundirá as traduções do .NET. 

### <a name="string-types-in-unions"></a>Tipos de cadeia de caracteres em uniões

Os arquivos IDL BITS passam cadeias de caracteres usando a Convenção LPWSTR (ponteiro longo para cadeia de caracteres largos). Embora isso funcione ao passar parâmetros de função (como o método Job. GetDisplayName ([out] LPWSTR * pVal), ele não funciona quando as cadeias de caracteres fazem parte de uniões. Por exemplo, o arquivo bits5_0. idl inclui a União de BITS_FILE_PROPERTY_VALUE:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

O campo LPWSTR não será incluído na versão .NET da União. Para corrigir isso, altere o LPWSTR para um WCHAR *. O campo resultante (chamado de String) será passado como um IntPtr. Converta-o em uma cadeia de caracteres usando System. Runtime. InteropServices. Marshal. PtrToStringAuto (valor. Cadeia de caracteres); forma.

### <a name="unions-in-structures"></a>Uniões em estruturas

Às vezes, as uniões inseridas em estruturas não serão incluídas na estrutura. Por exemplo, no Bits1_5. idl, o BG_AUTH_CREDENTIALS é definido da seguinte maneira:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

O BG_AUTH_CREDENTIALS_UNION é definido para ser uma União da seguinte maneira:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
O campo de credenciais na BG_AUTH_CREDENTIALS não será incluído na definição de classe do .NET.

Observe que a União é definida para sempre ser uma BG_BASIC_CREDENTIALS independentemente da BG_AUTH_SCHEME. Como a União não é usada como uma União, podemos apenas passar um BG_BASIC_CREDENTIALS assim:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Usando BITS de C #

### <a name="recommended-using-statement"></a>Instrução using recomendada

A configuração de algumas instruções using em C# reduzirá o número de caracteres que você precisa digitar para usar as diferentes versões de BITS. O nome "BITSReference" vem do nome da DLL de referência.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Exemplo rápido: baixar um arquivo

Um trecho de código C# curto, mas completo, para baixar um arquivo de uma URL é fornecido abaixo. 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

Neste código de exemplo, um Gerenciador de BITS chamado Mgr é criado. Ele corresponde diretamente à interface [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) . 

No Gerenciador, um novo trabalho é criado. O trabalho é um parâmetro de saída no método CreateJob. Também passado é o nome do trabalho (que não precisa ser exclusivo) e o tipo de download, que é um trabalho de download. Um GUID BITS para o identificador de trabalho também é preenchido.

Depois que o trabalho é criado, você adiciona um novo arquivo de download ao trabalho com o método AddFile. Você precisa passar duas cadeias de caracteres, uma para o arquivo remoto (a URL ou compartilhamento de arquivos) e outra para o arquivo local. 

Depois de adicionar o arquivo, chame resume no trabalho para iniciá-lo. Em seguida, o código aguarda até que o trabalho esteja em um estado final (erro ou transferido) e, em seguida, é concluído.

### <a name="bits-versions-casting-and-queryinterface"></a>Versões do BITS, conversão e QueryInterface

Você descobrirá que geralmente precisa usar uma versão anterior de um objeto BITS e uma versão mais recente em seu programa.  

Por exemplo, ao criar um objeto de trabalho, você obterá um método ibackgroundcopyjob (parte do BITS versão 1,0) mesmo quando estiver fazendo isso usando um objeto de gerente mais recente e um objeto método ibackgroundcopyjob mais recente estiver disponível. Como o método CreateJob não aceita uma interface para a versão mais recente, você não pode fazer a versão mais recente diretamente.

Use uma conversão .NET para converter de um objeto de tipo mais antigo em um objeto de tipo mais recente. A conversão chamará automaticamente um COM QueryInterface conforme apropriado. 

Neste exemplo, há um objeto método ibackgroundcopyjob do BITS chamado "Job" e queremos convertê-lo em um objeto IBackgroundCopyJob5 chamado "Job5" para que possamos chamar o método GetProperty do BITS 5,0. Acabamos de converter para o tipo IBackgroundCopyJob5 como este:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

A variável Job5 será inicializada pelo .NET usando o QueryInterface correto. 

Se seu código pode ser executado em um sistema que não dá suporte a uma versão específica do BITS, você pode tentar a conversão e capturar a System. InvalidCastException. 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

Um problema comum é quando você tenta converter no tipo errado de objeto. O sistema .NET não conhece a relação real entre as interfaces do BITS. Se você solicitar o tipo errado de interface, o .NET tentará fazê-lo para você e irá falhar com uma InvalidCastException e HResult 0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Trabalhando com as versões do BITS 10_1 e 10_2

Em algumas versões do Windows 10, você não pode criar diretamente um objeto BITS IBackgroundCopyManager usando as interfaces 10,1 ou 10,2. Em vez disso, você precisará usar várias versões dos arquivos de referência da DLL do BackgroundCopyManager. Por exemplo, você pode usar a versão 1,5 para criar um objeto IBackgroundCopyManager e, em seguida, converter o trabalho ou os objetos de arquivo resultantes usando as versões 10,1 ou 10,2.

