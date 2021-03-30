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
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="d729e-103">Chamando em BITS do .NET e do C# usando DLLs de referência</span><span class="sxs-lookup"><span data-stu-id="d729e-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="d729e-104">Uma maneira de chamar as classes COM de um programa .NET é criar um arquivo DLL de referência começando com os arquivos de [IDL](/windows/desktop/Midl/midl-start-page) do bits (linguagem de definição de interface) no SDK do Windows, usando as ferramentas [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) e [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) .</span><span class="sxs-lookup"><span data-stu-id="d729e-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="d729e-105">A DLL de referência é um conjunto de wrappers de classe para as classes COM de BITS; Você pode usar as classes de wrapper diretamente do .NET.</span><span class="sxs-lookup"><span data-stu-id="d729e-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="d729e-106">Uma alternativa ao uso de DLLs de referência criadas automaticamente é usar um wrapper de BITS .NET de terceiros do [GitHub](https://github.com/) e do [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="d729e-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="d729e-107">Esses wrappers geralmente têm um estilo de programação .NET mais natural, mas podem atrasar por trás das alterações e atualizações nas interfaces do BITS.</span><span class="sxs-lookup"><span data-stu-id="d729e-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="d729e-108">Criando DLLs de referência</span><span class="sxs-lookup"><span data-stu-id="d729e-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="d729e-109">Arquivos IDL de BITS</span><span class="sxs-lookup"><span data-stu-id="d729e-109">BITS IDL files</span></span>

<span data-ttu-id="d729e-110">Você começará com o conjunto de arquivos IDL do BITS.</span><span class="sxs-lookup"><span data-stu-id="d729e-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="d729e-111">Esses são arquivos que definem totalmente a interface COM do BITS.</span><span class="sxs-lookup"><span data-stu-id="d729e-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="d729e-112">Os arquivos estão localizados no diretório de **kits do Windows** e são chamados bits *version*. idl (por exemplo, bits10_2. idl), exceto para o arquivo da versão 1,0, que é apenas bits. idl.</span><span class="sxs-lookup"><span data-stu-id="d729e-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="d729e-113">À medida que novas versões de BITS são criadas, novos arquivos IDL de BITS também são criados.</span><span class="sxs-lookup"><span data-stu-id="d729e-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="d729e-114">Talvez você também queira modificar uma cópia dos arquivos IDL do BITS do SDK para usar os recursos do BITS que não são convertidos automaticamente em equivalentes do .NET.</span><span class="sxs-lookup"><span data-stu-id="d729e-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="d729e-115">As alterações de arquivo IDL possíveis serão discutidas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="d729e-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="d729e-116">Os arquivos IDL do BITS incluem vários outros arquivos IDL por referência.</span><span class="sxs-lookup"><span data-stu-id="d729e-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="d729e-117">Elas também se aninham, de modo que, se você usar uma versão, ela incluirá todas as versões mais baixas.</span><span class="sxs-lookup"><span data-stu-id="d729e-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="d729e-118">Para cada versão do BITS que você deseja direcionar em seu programa, você precisará de uma DLL de referência para essa versão.</span><span class="sxs-lookup"><span data-stu-id="d729e-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="d729e-119">Por exemplo, se você quiser escrever um programa que funcione em BITS 1,5 e superior, mas tenha recursos adicionais quando o BITS 10,2 estiver presente, será necessário converter os arquivos bits1_5. idl e bits10_2. idl.</span><span class="sxs-lookup"><span data-stu-id="d729e-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="d729e-120">Utilitários MIDL e TLBIMP</span><span class="sxs-lookup"><span data-stu-id="d729e-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="d729e-121">O utilitário [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (linguagem IDL da Microsoft) converte os arquivos IDL que descrevem a interface com do bits em um arquivo TLB (biblioteca de tipos).</span><span class="sxs-lookup"><span data-stu-id="d729e-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="d729e-122">A ferramenta MIDL depende do utilitário CL (pré-processador de C) para ler corretamente o arquivo de idioma IDL.</span><span class="sxs-lookup"><span data-stu-id="d729e-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="d729e-123">O utilitário CL faz parte do Visual Studio e é instalado quando você inclui recursos do C/C++ na instalação do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d729e-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="d729e-124">Normalmente, o utilitário MIDL criará um conjunto de arquivos C e H (código de linguagem C e cabeçalho de linguagem C).</span><span class="sxs-lookup"><span data-stu-id="d729e-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="d729e-125">Você pode suprimir esses arquivos extras enviando a saída para o dispositivo NUL:.</span><span class="sxs-lookup"><span data-stu-id="d729e-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="d729e-126">Por exemplo, definir o/dlldata nomedearquivo NUL: switch irá suprimir a criação de um arquivo dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="d729e-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="d729e-127">Os comandos de exemplo abaixo mostram quais opções devem ser definidas como NUL:.</span><span class="sxs-lookup"><span data-stu-id="d729e-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="d729e-128">O utilitário [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (tipo de importador de biblioteca de tipos) lê em um arquivo tlb e cria o arquivo DLL de referência correspondente.</span><span class="sxs-lookup"><span data-stu-id="d729e-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="d729e-129">Comandos de exemplo para MIDL e TLBIMP</span><span class="sxs-lookup"><span data-stu-id="d729e-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="d729e-130">Este é um exemplo do conjunto completo de comandos para gerar um conjunto de arquivos de referência.</span><span class="sxs-lookup"><span data-stu-id="d729e-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="d729e-131">Talvez seja necessário modificar os comandos com base em seu Visual Studio e SDK do Windows instalação e com base nos recursos do BITS e nas versões do sistema operacional que você está direcionando.</span><span class="sxs-lookup"><span data-stu-id="d729e-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="d729e-132">O exemplo cria um diretório para posicionar os arquivos DLL de referência e cria uma variável de ambiente BITSTEMP para apontar para esse diretório.</span><span class="sxs-lookup"><span data-stu-id="d729e-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="d729e-133">Os comandos de exemplo executam o arquivo vsdevcmd.bat que é criado pelo instalador do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d729e-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="d729e-134">Esse arquivo BAT irá configurar seus caminhos e algumas variáveis de ambiente para que os comandos MIDL e TLBIMP sejam executados.</span><span class="sxs-lookup"><span data-stu-id="d729e-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="d729e-135">Ele também configura as variáveis WindowsSdkDir e WindowsSDKLibVersion para apontar para os diretórios de SDK do Windows mais recentes.</span><span class="sxs-lookup"><span data-stu-id="d729e-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

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
<span data-ttu-id="d729e-136">Depois que esses comandos forem executados, você terá um conjunto de DLLs de referência no diretório BITSTEMP.</span><span class="sxs-lookup"><span data-stu-id="d729e-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="d729e-137">Adicionando as DLLs de referência ao seu projeto</span><span class="sxs-lookup"><span data-stu-id="d729e-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="d729e-138">Para usar uma DLL de referência em um projeto C#, abra seu projeto C# no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d729e-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="d729e-139">Na Gerenciador de Soluções, clique com o botão direito do mouse nas referências e clique em Adicionar referência.</span><span class="sxs-lookup"><span data-stu-id="d729e-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="d729e-140">Em seguida, clique no botão procurar e, em seguida, no botão Adicionar.</span><span class="sxs-lookup"><span data-stu-id="d729e-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="d729e-141">Navegue até o diretório com as DLLs de referência, selecione-as e clique em Adicionar.</span><span class="sxs-lookup"><span data-stu-id="d729e-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="d729e-142">Na janela Gerenciador de referências, as DLLs de referência serão verificadas.</span><span class="sxs-lookup"><span data-stu-id="d729e-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="d729e-143">Em seguida, clique em OK.</span><span class="sxs-lookup"><span data-stu-id="d729e-143">Then click OK.</span></span>

<span data-ttu-id="d729e-144">As DLLs de referência do BITS agora são adicionadas ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="d729e-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="d729e-145">As informações nos arquivos DLL de referência serão inseridas em seu programa final.</span><span class="sxs-lookup"><span data-stu-id="d729e-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="d729e-146">Você não precisa enviar os arquivos DLL de referência com seu programa; Você só precisa enviar o. EXE.</span><span class="sxs-lookup"><span data-stu-id="d729e-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="d729e-147">Você pode alterar se as DLLs de referência estão incorporadas ao EXE final.</span><span class="sxs-lookup"><span data-stu-id="d729e-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="d729e-148">Use a propriedade [inserir tipos de interoperabilidade](/dotnet/framework/interop/how-to-add-references-to-type-libraries) para definir se as DLLs de referência serão inseridas ou não.</span><span class="sxs-lookup"><span data-stu-id="d729e-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="d729e-149">Isso pode ser feito de acordo com a referência.</span><span class="sxs-lookup"><span data-stu-id="d729e-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="d729e-150">O padrão é true para inserir as DLLs.</span><span class="sxs-lookup"><span data-stu-id="d729e-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="d729e-151">Modificando arquivos IDL para obter um código .NET mais completo</span><span class="sxs-lookup"><span data-stu-id="d729e-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="d729e-152">Os arquivos IDL (linguagem IDL da Microsoft) BITS podem ser usados inalterados para criar o arquivo DLL BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="d729e-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="d729e-153">No entanto, a DLL de referência .NET resultante não terá algumas uniões irtraduzidas e terá nomes difíceis de usar para algumas estruturas e enumerações.</span><span class="sxs-lookup"><span data-stu-id="d729e-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="d729e-154">Esta seção descreve algumas das alterações que você pode fazer para tornar a DLL do .NET mais completa e mais fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="d729e-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="d729e-155">Nomes de enumeração mais simples</span><span class="sxs-lookup"><span data-stu-id="d729e-155">Simpler ENUM names</span></span>

<span data-ttu-id="d729e-156">Os arquivos IDL do BITS geralmente definem valores de enumeração como este:</span><span class="sxs-lookup"><span data-stu-id="d729e-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="d729e-157">O BG_AUTH_TARGET é o nome do typedef; o enum real não é nomeado.</span><span class="sxs-lookup"><span data-stu-id="d729e-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="d729e-158">Isso normalmente não causa problemas com o código C, mas não se traduz bem para uso com um programa .NET.</span><span class="sxs-lookup"><span data-stu-id="d729e-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="d729e-159">Um novo nome será criado automaticamente, mas poderá ser algo parecido com _MIDL___MIDL_itf_bits4_0_0005_0001_0001 em vez de um valor legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="d729e-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="d729e-160">Você pode corrigir esse problema atualizando os arquivos MIDL para incluir um nome de enumeração.</span><span class="sxs-lookup"><span data-stu-id="d729e-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="d729e-161">O nome de enumeração pode ser igual ao nome do typedef.</span><span class="sxs-lookup"><span data-stu-id="d729e-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="d729e-162">Alguns programadores têm uma Convenção de nomenclatura onde são mantidos diferentes (por exemplo, colocando um sublinhado antes do nome da enumeração), mas isso apenas confundirá as traduções do .NET.</span><span class="sxs-lookup"><span data-stu-id="d729e-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="d729e-163">Tipos de cadeia de caracteres em uniões</span><span class="sxs-lookup"><span data-stu-id="d729e-163">String types in unions</span></span>

<span data-ttu-id="d729e-164">Os arquivos IDL BITS passam cadeias de caracteres usando a Convenção LPWSTR (ponteiro longo para cadeia de caracteres largos).</span><span class="sxs-lookup"><span data-stu-id="d729e-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="d729e-165">Embora isso funcione ao passar parâmetros de função (como o método Job. GetDisplayName ([out] LPWSTR \* pVal), ele não funciona quando as cadeias de caracteres fazem parte de uniões.</span><span class="sxs-lookup"><span data-stu-id="d729e-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="d729e-166">Por exemplo, o arquivo bits5_0. idl inclui a União de BITS_FILE_PROPERTY_VALUE:</span><span class="sxs-lookup"><span data-stu-id="d729e-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="d729e-167">O campo LPWSTR não será incluído na versão .NET da União.</span><span class="sxs-lookup"><span data-stu-id="d729e-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="d729e-168">Para corrigir isso, altere o LPWSTR para um WCHAR \*.</span><span class="sxs-lookup"><span data-stu-id="d729e-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="d729e-169">O campo resultante (chamado de String) será passado como um IntPtr.</span><span class="sxs-lookup"><span data-stu-id="d729e-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="d729e-170">Converta-o em uma cadeia de caracteres usando System. Runtime. InteropServices. Marshal. PtrToStringAuto (valor. Cadeia de caracteres); forma.</span><span class="sxs-lookup"><span data-stu-id="d729e-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="d729e-171">Uniões em estruturas</span><span class="sxs-lookup"><span data-stu-id="d729e-171">Unions in structures</span></span>

<span data-ttu-id="d729e-172">Às vezes, as uniões inseridas em estruturas não serão incluídas na estrutura.</span><span class="sxs-lookup"><span data-stu-id="d729e-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="d729e-173">Por exemplo, no Bits1_5. idl, o BG_AUTH_CREDENTIALS é definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d729e-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="d729e-174">O BG_AUTH_CREDENTIALS_UNION é definido para ser uma União da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d729e-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="d729e-175">O campo de credenciais na BG_AUTH_CREDENTIALS não será incluído na definição de classe do .NET.</span><span class="sxs-lookup"><span data-stu-id="d729e-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="d729e-176">Observe que a União é definida para sempre ser uma BG_BASIC_CREDENTIALS independentemente da BG_AUTH_SCHEME.</span><span class="sxs-lookup"><span data-stu-id="d729e-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="d729e-177">Como a União não é usada como uma União, podemos apenas passar um BG_BASIC_CREDENTIALS assim:</span><span class="sxs-lookup"><span data-stu-id="d729e-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="d729e-178">Usando BITS de C #</span><span class="sxs-lookup"><span data-stu-id="d729e-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="d729e-179">Instrução using recomendada</span><span class="sxs-lookup"><span data-stu-id="d729e-179">Recommended using statement</span></span>

<span data-ttu-id="d729e-180">A configuração de algumas instruções using em C# reduzirá o número de caracteres que você precisa digitar para usar as diferentes versões de BITS.</span><span class="sxs-lookup"><span data-stu-id="d729e-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="d729e-181">O nome "BITSReference" vem do nome da DLL de referência.</span><span class="sxs-lookup"><span data-stu-id="d729e-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="d729e-182">Exemplo rápido: baixar um arquivo</span><span class="sxs-lookup"><span data-stu-id="d729e-182">Quick Sample: download a file</span></span>

<span data-ttu-id="d729e-183">Um trecho de código C# curto, mas completo, para baixar um arquivo de uma URL é fornecido abaixo.</span><span class="sxs-lookup"><span data-stu-id="d729e-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

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

<span data-ttu-id="d729e-184">Neste código de exemplo, um Gerenciador de BITS chamado Mgr é criado.</span><span class="sxs-lookup"><span data-stu-id="d729e-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="d729e-185">Ele corresponde diretamente à interface [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="d729e-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="d729e-186">No Gerenciador, um novo trabalho é criado.</span><span class="sxs-lookup"><span data-stu-id="d729e-186">From the manager a new job is created.</span></span> <span data-ttu-id="d729e-187">O trabalho é um parâmetro de saída no método CreateJob.</span><span class="sxs-lookup"><span data-stu-id="d729e-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="d729e-188">Também passado é o nome do trabalho (que não precisa ser exclusivo) e o tipo de download, que é um trabalho de download.</span><span class="sxs-lookup"><span data-stu-id="d729e-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="d729e-189">Um GUID BITS para o identificador de trabalho também é preenchido.</span><span class="sxs-lookup"><span data-stu-id="d729e-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="d729e-190">Depois que o trabalho é criado, você adiciona um novo arquivo de download ao trabalho com o método AddFile.</span><span class="sxs-lookup"><span data-stu-id="d729e-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="d729e-191">Você precisa passar duas cadeias de caracteres, uma para o arquivo remoto (a URL ou compartilhamento de arquivos) e outra para o arquivo local.</span><span class="sxs-lookup"><span data-stu-id="d729e-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="d729e-192">Depois de adicionar o arquivo, chame resume no trabalho para iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="d729e-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="d729e-193">Em seguida, o código aguarda até que o trabalho esteja em um estado final (erro ou transferido) e, em seguida, é concluído.</span><span class="sxs-lookup"><span data-stu-id="d729e-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="d729e-194">Versões do BITS, conversão e QueryInterface</span><span class="sxs-lookup"><span data-stu-id="d729e-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="d729e-195">Você descobrirá que geralmente precisa usar uma versão anterior de um objeto BITS e uma versão mais recente em seu programa.</span><span class="sxs-lookup"><span data-stu-id="d729e-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="d729e-196">Por exemplo, ao criar um objeto de trabalho, você obterá um método ibackgroundcopyjob (parte do BITS versão 1,0) mesmo quando estiver fazendo isso usando um objeto de gerente mais recente e um objeto método ibackgroundcopyjob mais recente estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="d729e-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="d729e-197">Como o método CreateJob não aceita uma interface para a versão mais recente, você não pode fazer a versão mais recente diretamente.</span><span class="sxs-lookup"><span data-stu-id="d729e-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="d729e-198">Use uma conversão .NET para converter de um objeto de tipo mais antigo em um objeto de tipo mais recente.</span><span class="sxs-lookup"><span data-stu-id="d729e-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="d729e-199">A conversão chamará automaticamente um COM QueryInterface conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="d729e-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="d729e-200">Neste exemplo, há um objeto método ibackgroundcopyjob do BITS chamado "Job" e queremos convertê-lo em um objeto IBackgroundCopyJob5 chamado "Job5" para que possamos chamar o método GetProperty do BITS 5,0.</span><span class="sxs-lookup"><span data-stu-id="d729e-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="d729e-201">Acabamos de converter para o tipo IBackgroundCopyJob5 como este:</span><span class="sxs-lookup"><span data-stu-id="d729e-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="d729e-202">A variável Job5 será inicializada pelo .NET usando o QueryInterface correto.</span><span class="sxs-lookup"><span data-stu-id="d729e-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="d729e-203">Se seu código pode ser executado em um sistema que não dá suporte a uma versão específica do BITS, você pode tentar a conversão e capturar a System. InvalidCastException.</span><span class="sxs-lookup"><span data-stu-id="d729e-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

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

<span data-ttu-id="d729e-204">Um problema comum é quando você tenta converter no tipo errado de objeto.</span><span class="sxs-lookup"><span data-stu-id="d729e-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="d729e-205">O sistema .NET não conhece a relação real entre as interfaces do BITS.</span><span class="sxs-lookup"><span data-stu-id="d729e-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="d729e-206">Se você solicitar o tipo errado de interface, o .NET tentará fazê-lo para você e irá falhar com uma InvalidCastException e HResult 0x80004002 (E_NOINTERFACE).</span><span class="sxs-lookup"><span data-stu-id="d729e-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="d729e-207">Trabalhando com as versões do BITS 10_1 e 10_2</span><span class="sxs-lookup"><span data-stu-id="d729e-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="d729e-208">Em algumas versões do Windows 10, você não pode criar diretamente um objeto BITS IBackgroundCopyManager usando as interfaces 10,1 ou 10,2.</span><span class="sxs-lookup"><span data-stu-id="d729e-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="d729e-209">Em vez disso, você precisará usar várias versões dos arquivos de referência da DLL do BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="d729e-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="d729e-210">Por exemplo, você pode usar a versão 1,5 para criar um objeto IBackgroundCopyManager e, em seguida, converter o trabalho ou os objetos de arquivo resultantes usando as versões 10,1 ou 10,2.</span><span class="sxs-lookup"><span data-stu-id="d729e-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

