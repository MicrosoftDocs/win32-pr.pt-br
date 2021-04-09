---
title: Análise de despejo de memória
description: Este artigo técnico fornece informações sobre como escrever e usar um minidespejo.
ms.assetid: 575c4716-18c2-7b11-7308-aa2e3d8efac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7558e47d08cb0183b8d9cefa5f22f0750fd1c598
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007801"
---
# <a name="crash-dump-analysis"></a><span data-ttu-id="622d1-103">Análise de despejo de memória</span><span class="sxs-lookup"><span data-stu-id="622d1-103">Crash Dump Analysis</span></span>

<span data-ttu-id="622d1-104">Nem todos os bugs podem ser encontrados antes do lançamento, o que significa que nem todos os bugs que geram exceções podem ser encontrados antes do lançamento.</span><span class="sxs-lookup"><span data-stu-id="622d1-104">Not all bugs can be found prior to release, which means not all bugs that throw exceptions can be found before release.</span></span> <span data-ttu-id="622d1-105">Felizmente, a Microsoft incluiu o SDK da plataforma uma função para ajudar os desenvolvedores a coletar informações sobre exceções descobertas pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="622d1-105">Fortunately, Microsoft has included in the Platform SDK a function to help developers collect information on exceptions that are discovered by users.</span></span> <span data-ttu-id="622d1-106">A função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) grava as informações de despejo de memória necessárias em um arquivo sem salvar todo o espaço do processo.</span><span class="sxs-lookup"><span data-stu-id="622d1-106">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function writes the necessary crash dump information to a file without saving the whole process space.</span></span> <span data-ttu-id="622d1-107">Esse arquivo de informações de despejo de memória é chamado de minidespejo.</span><span class="sxs-lookup"><span data-stu-id="622d1-107">This crash dump information file is called a minidump.</span></span> <span data-ttu-id="622d1-108">Este artigo técnico fornece informações sobre como escrever e usar um minidespejo.</span><span class="sxs-lookup"><span data-stu-id="622d1-108">This technical article provides info about how to write and use a minidump.</span></span>

-   [<span data-ttu-id="622d1-109">Escrevendo um minidespejo</span><span class="sxs-lookup"><span data-stu-id="622d1-109">Writing a Minidump</span></span>](#writing-a-minidump)
-   [<span data-ttu-id="622d1-110">Segurança de thread</span><span class="sxs-lookup"><span data-stu-id="622d1-110">Thread safety</span></span>](#thread-safety)
-   [<span data-ttu-id="622d1-111">Escrevendo um minidespejo com código</span><span class="sxs-lookup"><span data-stu-id="622d1-111">Writing a Minidump with Code</span></span>](#writing-a-minidump-with-code)
-   [<span data-ttu-id="622d1-112">Usando Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="622d1-112">Using Dumpchk.exe</span></span>](#using-dumpchkexe)
-   [<span data-ttu-id="622d1-113">Analisando um minidespejo</span><span class="sxs-lookup"><span data-stu-id="622d1-113">Analyzing a Minidump</span></span>](#analyzing-a-minidump)
    -   [<span data-ttu-id="622d1-114">Usando o servidor de símbolos público da Microsoft</span><span class="sxs-lookup"><span data-stu-id="622d1-114">Using the Microsoft Public Symbol Server</span></span>](#using-the-microsoft-public-symbol-server)
    -   [<span data-ttu-id="622d1-115">Depurando um minidespejo com o WinDbg</span><span class="sxs-lookup"><span data-stu-id="622d1-115">Debugging a Minidump with WinDbg</span></span>](#debugging-a-minidump-with-windbg)
    -   [<span data-ttu-id="622d1-116">Usando ferramentas de Copy-Protection com minidespejos</span><span class="sxs-lookup"><span data-stu-id="622d1-116">Using Copy-Protection Tools with Minidumps</span></span>](#using-copy-protection-tools-with-minidumps)
-   [<span data-ttu-id="622d1-117">Resumo</span><span class="sxs-lookup"><span data-stu-id="622d1-117">Summary</span></span>](#summary)

## <a name="writing-a-minidump"></a><span data-ttu-id="622d1-118">Escrevendo um minidespejo</span><span class="sxs-lookup"><span data-stu-id="622d1-118">Writing a Minidump</span></span>

<span data-ttu-id="622d1-119">As opções básicas para escrever um minidespejo são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="622d1-119">The basic options for writing a minidump are as follows:</span></span>

-   <span data-ttu-id="622d1-120">Não fazer nada.</span><span class="sxs-lookup"><span data-stu-id="622d1-120">Do nothing.</span></span> <span data-ttu-id="622d1-121">O Windows gera automaticamente um minidespejo sempre que um programa gera uma exceção sem tratamento.</span><span class="sxs-lookup"><span data-stu-id="622d1-121">Windows automatically generates a minidump whenever a program throws an unhandled exception.</span></span> <span data-ttu-id="622d1-122">A geração automática de um minidespejo está disponível desde o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="622d1-122">Automatic generation of a minidump is available since Windows XP.</span></span> <span data-ttu-id="622d1-123">Se o usuário permitir, o minidespejo será enviado à Microsoft, e não ao desenvolvedor, por meio de Relatório de Erros do Windows (WER).</span><span class="sxs-lookup"><span data-stu-id="622d1-123">If the user allows it, the minidump will be sent to Microsoft, and not to the developer, through Windows Error Reporting (WER).</span></span> <span data-ttu-id="622d1-124">Os desenvolvedores podem obter acesso a esses minidespejos por meio do [programa de aplicativos da área de trabalho do Windows](../appxpkg/windows-desktop-application-program.md).</span><span class="sxs-lookup"><span data-stu-id="622d1-124">Developers can gain access to these minidumps through the [Windows Desktop Application Program](../appxpkg/windows-desktop-application-program.md).</span></span>

    <span data-ttu-id="622d1-125">O uso do WER requer:</span><span class="sxs-lookup"><span data-stu-id="622d1-125">Use of WER requires:</span></span>

    -   <span data-ttu-id="622d1-126">Desenvolvedores para assinar seus aplicativos usando Authenticode</span><span class="sxs-lookup"><span data-stu-id="622d1-126">Developers to sign their applications using Authenticode</span></span>
    -   <span data-ttu-id="622d1-127">Os aplicativos têm um recurso VERSIONINFO válido em todos os executáveis e DLL</span><span class="sxs-lookup"><span data-stu-id="622d1-127">Applications have valid VERSIONINFO resource in every executable and DLL</span></span>

    <span data-ttu-id="622d1-128">Se você implementar uma rotina personalizada para exceções sem tratamento, será altamente recomendável usar a função [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) no manipulador de exceção para também enviar um minidespejo automatizado para o wer.</span><span class="sxs-lookup"><span data-stu-id="622d1-128">If you implement a custom routine for unhandled exceptions, you are strongly urged to use the [**ReportFault**](/windows/desktop/api/errorrep/nf-errorrep-reportfault) function in the exception handler to also send an automated minidump to WER.</span></span> <span data-ttu-id="622d1-129">A função **ReportFault** lida com todos os problemas de conexão e envio do minidespejo para o wer.</span><span class="sxs-lookup"><span data-stu-id="622d1-129">The **ReportFault** function handles all of the issues of connecting to and sending the minidump to WER.</span></span> <span data-ttu-id="622d1-130">Não enviar minidespejos para o WER viola os requisitos de jogos para o Windows.</span><span class="sxs-lookup"><span data-stu-id="622d1-130">Not sending minidumps to WER violates the requirements of Games for Windows.</span></span>

    <span data-ttu-id="622d1-131">Para obter mais informações sobre como o WER funciona, consulte [como relatório de erros do Windows funciona](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span><span class="sxs-lookup"><span data-stu-id="622d1-131">For more information on how WER works, see [How Windows Error Reporting Works](https://www.microsoft.com/whdc/maintain/WER/WERWorks.mspx).</span></span> <span data-ttu-id="622d1-132">Para obter uma explicação dos detalhes do registro, consulte [introdução ao relatório de erros do Windows](https://msdn.microsoft.com/) na [zona ISV](https://msdn.microsoft.com/)do MSDN.</span><span class="sxs-lookup"><span data-stu-id="622d1-132">For an explanation of registration details, see [Introducing Windows Error Reporting](https://msdn.microsoft.com/) on MSDN's [ISV Zone](https://msdn.microsoft.com/).</span></span>

-   <span data-ttu-id="622d1-133">Use um produto do Microsoft Visual Studio Team System.</span><span class="sxs-lookup"><span data-stu-id="622d1-133">Use a product from the Microsoft Visual Studio Team System.</span></span> <span data-ttu-id="622d1-134">No menu **depurar** , clique em **Salvar despejo como** para salvar uma cópia de um despejo.</span><span class="sxs-lookup"><span data-stu-id="622d1-134">On the **Debug** menu, click **Save Dump As** to save a copy of a dump.</span></span> <span data-ttu-id="622d1-135">O uso de um despejo salvo localmente é apenas uma opção para teste interno e depuração.</span><span class="sxs-lookup"><span data-stu-id="622d1-135">Use of a locally saved dump is only an option for in-house testing and debugging.</span></span>
-   <span data-ttu-id="622d1-136">Adicione código ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="622d1-136">Add code to your project.</span></span> <span data-ttu-id="622d1-137">Adicione a função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e o código de manipulação de exceção apropriado para salvar e enviar um minidespejo diretamente para o desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="622d1-137">Add the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function and the appropriate exception handling code to save and send a minidump directly to the developer.</span></span> <span data-ttu-id="622d1-138">Este artigo demonstra como implementar essa opção.</span><span class="sxs-lookup"><span data-stu-id="622d1-138">This article demonstrates how to implement this option.</span></span> <span data-ttu-id="622d1-139">No entanto, observe que o **MiniDumpWriteDump** atualmente não funciona com código gerenciado e só está disponível no Windows XP, no Windows Vista e no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="622d1-139">However, note that **MiniDumpWriteDump** does not currently work with managed code and is only available on Windows XP, Windows Vista, Windows 7.</span></span>

## <a name="thread-safety"></a><span data-ttu-id="622d1-140">Acesso thread-safe</span><span class="sxs-lookup"><span data-stu-id="622d1-140">Thread safety</span></span>

<span data-ttu-id="622d1-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) faz parte da biblioteca dbghelp.</span><span class="sxs-lookup"><span data-stu-id="622d1-141">[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) is part of the DBGHELP library.</span></span> <span data-ttu-id="622d1-142">Essa biblioteca não é thread-safe, portanto, qualquer programa que usa **MiniDumpWriteDump** deve sincronizar todos os threads antes de tentar chamar **MiniDumpWriteDump**.</span><span class="sxs-lookup"><span data-stu-id="622d1-142">This library is not thread-safe, so any program that uses **MiniDumpWriteDump** should synchronize all threads before attempting to call **MiniDumpWriteDump**.</span></span>

## <a name="writing-a-minidump-with-code"></a><span data-ttu-id="622d1-143">Escrevendo um minidespejo com código</span><span class="sxs-lookup"><span data-stu-id="622d1-143">Writing a Minidump with Code</span></span>

<span data-ttu-id="622d1-144">A implementação real é simples.</span><span class="sxs-lookup"><span data-stu-id="622d1-144">The actual implementation is straightforward.</span></span> <span data-ttu-id="622d1-145">Veja a seguir um exemplo simples de como usar o [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="622d1-145">The following is a simple example of how to use [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>


```C++
#include <dbghelp.h>
#include <shellapi.h>
#include <shlobj.h>

int GenerateDump(EXCEPTION_POINTERS* pExceptionPointers)
{
    BOOL bMiniDumpSuccessful;
    WCHAR szPath[MAX_PATH]; 
    WCHAR szFileName[MAX_PATH]; 
    WCHAR* szAppName = L"AppName";
    WCHAR* szVersion = L"v1.0";
    DWORD dwBufferSize = MAX_PATH;
    HANDLE hDumpFile;
    SYSTEMTIME stLocalTime;
    MINIDUMP_EXCEPTION_INFORMATION ExpParam;

    GetLocalTime( &stLocalTime );
    GetTempPath( dwBufferSize, szPath );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s", szPath, szAppName );
    CreateDirectory( szFileName, NULL );

    StringCchPrintf( szFileName, MAX_PATH, L"%s%s\\%s-%04d%02d%02d-%02d%02d%02d-%ld-%ld.dmp", 
               szPath, szAppName, szVersion, 
               stLocalTime.wYear, stLocalTime.wMonth, stLocalTime.wDay, 
               stLocalTime.wHour, stLocalTime.wMinute, stLocalTime.wSecond, 
               GetCurrentProcessId(), GetCurrentThreadId());
    hDumpFile = CreateFile(szFileName, GENERIC_READ|GENERIC_WRITE, 
                FILE_SHARE_WRITE|FILE_SHARE_READ, 0, CREATE_ALWAYS, 0, 0);

    ExpParam.ThreadId = GetCurrentThreadId();
    ExpParam.ExceptionPointers = pExceptionPointers;
    ExpParam.ClientPointers = TRUE;

    bMiniDumpSuccessful = MiniDumpWriteDump(GetCurrentProcess(), GetCurrentProcessId(), 
                    hDumpFile, MiniDumpWithDataSegs, &ExpParam, NULL, NULL);

    return EXCEPTION_EXECUTE_HANDLER;
}


void SomeFunction()
{
    __try
    {
        int *pBadPtr = NULL;
        *pBadPtr = 0;
    }
    __except(GenerateDump(GetExceptionInformation()))
    {
    }
}
```



<span data-ttu-id="622d1-146">Este exemplo demonstra o uso básico de [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) e as informações mínimas necessárias para chamá-lo.</span><span class="sxs-lookup"><span data-stu-id="622d1-146">This example demonstrates the basic usage of [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) and the minimum information necessary to call it.</span></span> <span data-ttu-id="622d1-147">O nome do arquivo de despejo é para o desenvolvedor; no entanto, para evitar colisões de nome de arquivo, é aconselhável gerar o nome do arquivo a partir do nome do aplicativo e do número de versão, das IDs do processo e do thread, e da data e hora.</span><span class="sxs-lookup"><span data-stu-id="622d1-147">The name of the dump file is up to the developer; however, to avoid file name collisions, it is advisable to generate the file name from the application's name and version number, the process and thread IDs, and the date and time.</span></span> <span data-ttu-id="622d1-148">Isso também ajudará a manter os minidespejos agrupados por aplicativo e versão.</span><span class="sxs-lookup"><span data-stu-id="622d1-148">This will also help to keep the minidumps grouped by application and version.</span></span> <span data-ttu-id="622d1-149">Cabe ao desenvolvedor decidir quantas informações são usadas para diferenciar nomes de arquivos de minidespejo.</span><span class="sxs-lookup"><span data-stu-id="622d1-149">It is up to the developer to decide how much information is used to differentiate minidump file names.</span></span>

<span data-ttu-id="622d1-150">Deve-se observar que o nome do caminho no exemplo anterior foi gerado chamando a função [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) para recuperar o caminho do diretório designado para arquivos temporários.</span><span class="sxs-lookup"><span data-stu-id="622d1-150">It should be noted that the path name in the preceding example was generated by calling the [**GetTempPath**](/windows/desktop/api/fileapi/nf-fileapi-gettemppatha) function to retrieve the path of the directory designated for temporary files.</span></span> <span data-ttu-id="622d1-151">O uso desse diretório funciona mesmo com contas de usuário com privilégios mínimos e também impede que o minidespejo libere espaço no disco rígido depois que ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="622d1-151">Use of this directory works even with least-privileged user accounts, and it also prevents the minidump from taking up hard drive space after it is no longer needed.</span></span>

<span data-ttu-id="622d1-152">Se você arquivar o produto durante seu processo de compilação diário, também não se esqueça de incluir símbolos para a compilação para que você possa depurar uma versão antiga do produto, se necessário.</span><span class="sxs-lookup"><span data-stu-id="622d1-152">If you archive the product during your daily build process, also be sure to include symbols for the build so that you can debug an old version of the product, if necessary.</span></span> <span data-ttu-id="622d1-153">Você também precisa tomar medidas para manter as otimizações completas do compilador ao gerar símbolos.</span><span class="sxs-lookup"><span data-stu-id="622d1-153">You also need to take steps to maintain full compiler optimizations while generating symbols.</span></span> <span data-ttu-id="622d1-154">Isso pode ser feito abrindo as propriedades do projeto no ambiente de desenvolvimento e, para a configuração de versão, fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="622d1-154">This can be done by opening your project's properties in the development environment and, for the release configuration, doing the following:</span></span>

1.  <span data-ttu-id="622d1-155">No lado esquerdo da página de propriedades do projeto, clique em C/C++.</span><span class="sxs-lookup"><span data-stu-id="622d1-155">On the left side of the project's property page, click C/C++.</span></span> <span data-ttu-id="622d1-156">Por padrão, isso exibe as configurações **gerais** .</span><span class="sxs-lookup"><span data-stu-id="622d1-156">By default, this displays **General** settings.</span></span> <span data-ttu-id="622d1-157">No lado direito da página de propriedades do projeto, defina o **formato de informações de depuração** como **banco de dados do programa (/Zi)**.</span><span class="sxs-lookup"><span data-stu-id="622d1-157">On the right side of the project's property page, set **Debug Information Format** to **Program Database (/Zi)**.</span></span>
2.  <span data-ttu-id="622d1-158">No lado esquerdo da página de propriedades, expanda **vinculador** e clique em **depuração**.</span><span class="sxs-lookup"><span data-stu-id="622d1-158">On the left side of the property page, expand **Linker**, and then click **Debugging**.</span></span> <span data-ttu-id="622d1-159">No lado direito da página de propriedades, defina **gerar informações de depuração** como **Sim (/debug)**.</span><span class="sxs-lookup"><span data-stu-id="622d1-159">On the right side of the property page, set **Generate Debug Info** to **Yes (/DEBUG)**.</span></span>
3.  <span data-ttu-id="622d1-160">Clique em **otimização** e defina **referências** para e **Liminate dados não referenciados (/OPT: REF)**.</span><span class="sxs-lookup"><span data-stu-id="622d1-160">Click **Optimization**, and set **References** to E **liminate Unreferenced Data (/OPT:REF)**.</span></span>
4.  <span data-ttu-id="622d1-161">Defina **habilitar dobramento COMDAT** para **remover COMDATs redundantes (/OPT: ICF)**.</span><span class="sxs-lookup"><span data-stu-id="622d1-161">Set **Enable COMDAT Folding** to **Remove Redundant COMDATs (/OPT:ICF)**.</span></span>

<span data-ttu-id="622d1-162">O MSDN tem informações mais detalhadas sobre a estrutura de [**\_ \_ informações de exceção de minidespejo**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) e a função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) .</span><span class="sxs-lookup"><span data-stu-id="622d1-162">MSDN has more detailed information on the [**MINIDUMP\_EXCEPTION\_INFORMATION**](/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_exception_information) structure and the [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function.</span></span>

## <a name="using-dumpchkexe"></a><span data-ttu-id="622d1-163">Usando Dumpchk.exe</span><span class="sxs-lookup"><span data-stu-id="622d1-163">Using Dumpchk.exe</span></span>

<span data-ttu-id="622d1-164">Dumpchk.exe é um utilitário de linha de comando que pode ser usado para verificar se um arquivo de despejo foi criado corretamente.</span><span class="sxs-lookup"><span data-stu-id="622d1-164">Dumpchk.exe is a command-line utility that can be used to verify that a dump file was created correctly.</span></span> <span data-ttu-id="622d1-165">Se Dumpchk.exe gerar um erro, o arquivo de despejo estará corrompido e não poderá ser analisado.</span><span class="sxs-lookup"><span data-stu-id="622d1-165">If Dumpchk.exe generates an error, then the dump file is corrupt and cannot be analyzed.</span></span> <span data-ttu-id="622d1-166">Para obter informações sobre como usar Dumpchk.exe, consulte [como usar Dumpchk.exe para verificar um arquivo de despejo de memória](https://support.microsoft.com/kb/315271/).</span><span class="sxs-lookup"><span data-stu-id="622d1-166">For information on using Dumpchk.exe, see [How to Use Dumpchk.exe to Check a Memory Dump File](https://support.microsoft.com/kb/315271/).</span></span>

<span data-ttu-id="622d1-167">Dumpchk.exe está incluído no CD do produto Windows XP e pode ser instalado na unidade do sistema \\ arquivos \\ de programa de suporte ferramentas \\ executando Setup.exe na \\ pasta ferramentas de suporte \\ no CD do produto Windows XP.</span><span class="sxs-lookup"><span data-stu-id="622d1-167">Dumpchk.exe is included on the Windows XP product CD and can be installed to System Drive\\Program Files\\Support Tools\\ by running Setup.exe in the Support\\Tools\\ folder on the Windows XP product CD.</span></span> <span data-ttu-id="622d1-168">Você também pode obter a versão mais recente do Dumpchk.exe baixando e instalando as ferramentas de depuração disponíveis nas [ferramentas de depuração do Windows](https://www.microsoft.com/whdc/devtools/debugging/) no [Windows hardware Developer Central](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="622d1-168">You can also get the latest version of Dumpchk.exe by download and installing the debugging tools available from [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

## <a name="analyzing-a-minidump"></a><span data-ttu-id="622d1-169">Analisando um minidespejo</span><span class="sxs-lookup"><span data-stu-id="622d1-169">Analyzing a Minidump</span></span>

<span data-ttu-id="622d1-170">Abrir um minidespejo para análise é tão fácil quanto criar um.</span><span class="sxs-lookup"><span data-stu-id="622d1-170">Opening a minidump for analysis is as easy as creating one.</span></span>

<span data-ttu-id="622d1-171">**Para analisar um minidespejo**</span><span class="sxs-lookup"><span data-stu-id="622d1-171">**To analyze a minidump**</span></span>

1.  <span data-ttu-id="622d1-172">Abra o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="622d1-172">Open Visual Studio.</span></span>
2.  <span data-ttu-id="622d1-173">No menu **arquivo** , clique em **Abrir projeto**.</span><span class="sxs-lookup"><span data-stu-id="622d1-173">On the **File** menu, click **Open Project**.</span></span>
3.  <span data-ttu-id="622d1-174">Defina **arquivos do tipo** para **despejar arquivos**, navegue até o arquivo de despejo, selecione-o e clique em **abrir.**</span><span class="sxs-lookup"><span data-stu-id="622d1-174">Set **Files of type** to **Dump Files**, navigate to the dump file, select it, and click **Open.**</span></span>
4.  <span data-ttu-id="622d1-175">Execute o depurador.</span><span class="sxs-lookup"><span data-stu-id="622d1-175">Run the debugger.</span></span>

<span data-ttu-id="622d1-176">O depurador criará um processo simulado.</span><span class="sxs-lookup"><span data-stu-id="622d1-176">The debugger will create a simulated process.</span></span> <span data-ttu-id="622d1-177">O processo simulado será interrompido na instrução que causou a falha.</span><span class="sxs-lookup"><span data-stu-id="622d1-177">The simulated process will be halted at the instruction that caused the crash.</span></span>

### <a name="using-the-microsoft-public-symbol-server"></a><span data-ttu-id="622d1-178">Usando o servidor de símbolos público da Microsoft</span><span class="sxs-lookup"><span data-stu-id="622d1-178">Using the Microsoft Public Symbol Server</span></span>

<span data-ttu-id="622d1-179">Para obter a pilha para falhas em nível de driver ou de sistema, pode ser necessário configurar o Visual Studio para apontar para o servidor de símbolos público da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="622d1-179">To get the stack for driver- or system-level crashes, it might be necessary to configure Visual Studio to point to the Microsoft public symbol server.</span></span>

<span data-ttu-id="622d1-180">**Para definir um caminho para o servidor de símbolos da Microsoft**</span><span class="sxs-lookup"><span data-stu-id="622d1-180">**To set a path to the Microsoft symbol server**</span></span>

1.  <span data-ttu-id="622d1-181">No menu **depurar** , clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="622d1-181">On the **Debug** menu, click **Options**.</span></span>
2.  <span data-ttu-id="622d1-182">Na caixa de diálogo **Opções** , abra o nó **depuração** e clique em **símbolos**.</span><span class="sxs-lookup"><span data-stu-id="622d1-182">In the **Options** dialog box, open the **Debugging** node, and click **Symbols**.</span></span>
3.  <span data-ttu-id="622d1-183">Certifique-se **de Pesquisar os locais acima somente quando os símbolos são carregados manualmente** não estiver selecionado, a menos que você queira carregar os símbolos manualmente ao depurar.</span><span class="sxs-lookup"><span data-stu-id="622d1-183">Make sure **Search the above locations only when symbols are loaded manually** is not selected, unless you want to load symbols manually when you debug.</span></span>
4.  <span data-ttu-id="622d1-184">Se você estiver usando símbolos em um servidor de símbolos remoto, poderá melhorar o desempenho especificando um diretório local para o qual os símbolos podem ser copiados.</span><span class="sxs-lookup"><span data-stu-id="622d1-184">If you are using symbols on a remote symbol server, you can improve performance by specifying a local directory that symbols can be copied to.</span></span> <span data-ttu-id="622d1-185">Para fazer isso, insira um caminho para os **símbolos de cache do servidor de símbolo para esse diretório**.</span><span class="sxs-lookup"><span data-stu-id="622d1-185">To do this, enter a path for **Cache symbols from symbol server to this directory**.</span></span> <span data-ttu-id="622d1-186">Para se conectar ao servidor de símbolos público da Microsoft, você precisa habilitar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="622d1-186">To connect to the Microsoft public symbol server, you need to enable this setting.</span></span> <span data-ttu-id="622d1-187">Observe que, se você estiver depurando um programa em um computador remoto, o diretório de cache se referirá a um diretório no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="622d1-187">Note that if you are debugging a program on a remote computer, the cache directory refers to a directory on the remote computer.</span></span>
5.  <span data-ttu-id="622d1-188">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="622d1-188">Click **OK**.</span></span>
6.  <span data-ttu-id="622d1-189">Como você está usando o servidor de símbolos público da Microsoft, uma caixa de diálogo de contrato de licença de usuário final é exibida.</span><span class="sxs-lookup"><span data-stu-id="622d1-189">Because you are using the Microsoft public symbol server, an End User License Agreement dialog box appears.</span></span> <span data-ttu-id="622d1-190">Clique em **Sim** para aceitar o contrato e baixar símbolos em seu cache local.</span><span class="sxs-lookup"><span data-stu-id="622d1-190">Click **Yes** to accept the agreement and download symbols to your local cache.</span></span>

### <a name="debugging-a-minidump-with-windbg"></a><span data-ttu-id="622d1-191">Depurando um minidespejo com o WinDbg</span><span class="sxs-lookup"><span data-stu-id="622d1-191">Debugging a Minidump with WinDbg</span></span>

<span data-ttu-id="622d1-192">Você também pode usar o WinDbg, um depurador que faz parte das ferramentas de depuração do Windows, para depurar um minidespejo.</span><span class="sxs-lookup"><span data-stu-id="622d1-192">You can also use WinDbg, a debugger that is part of the Windows Debugging Tools, to debug a minidump.</span></span> <span data-ttu-id="622d1-193">O WinDbg permite que você depure sem precisar usar o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="622d1-193">WinDbg allows you to debug without having to use Visual Studio.</span></span> <span data-ttu-id="622d1-194">Para baixar as ferramentas de depuração do Windows, consulte [ferramentas de depuração do Windows](https://www.microsoft.com/whdc/devtools/debugging/) no [Windows hardware Developer Central](https://www.microsoft.com/whdc/).</span><span class="sxs-lookup"><span data-stu-id="622d1-194">To download Windows Debugging Tools, see [Windows Debugging Tools](https://www.microsoft.com/whdc/devtools/debugging/) on [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).</span></span>

<span data-ttu-id="622d1-195">Depois de instalar as ferramentas de depuração do Windows, você deve inserir o caminho do símbolo no WinDbg.</span><span class="sxs-lookup"><span data-stu-id="622d1-195">After installing Windows Debugging Tools, you must enter the symbol path in WinDbg.</span></span>

<span data-ttu-id="622d1-196">**Para inserir um caminho de símbolo no WinDbg**</span><span class="sxs-lookup"><span data-stu-id="622d1-196">**To enter a symbol path in WinDbg**</span></span>

1.  <span data-ttu-id="622d1-197">No menu **arquivo** , clique em **caminho do símbolo**.</span><span class="sxs-lookup"><span data-stu-id="622d1-197">On the **File** menu, click **Symbol Path**.</span></span>
2.  <span data-ttu-id="622d1-198">Na janela **caminho de pesquisa de símbolos** , insira o seguinte:</span><span class="sxs-lookup"><span data-stu-id="622d1-198">In the **Symbol Search Path** window, enter the following:</span></span>

    <span data-ttu-id="622d1-199">"SRV \* c: \\ cache \* https://msdl.microsoft.com/download/symbols ;"</span><span class="sxs-lookup"><span data-stu-id="622d1-199">"srv\*c:\\cache\*https://msdl.microsoft.com/download/symbols;"</span></span>

### <a name="using-copy-protection-tools-with-minidumps"></a><span data-ttu-id="622d1-200">Usando ferramentas de Copy-Protection com minidespejos</span><span class="sxs-lookup"><span data-stu-id="622d1-200">Using Copy-Protection Tools with Minidumps</span></span>

<span data-ttu-id="622d1-201">Os desenvolvedores também precisam estar cientes de como seu esquema de proteção de cópia pode afetar o minidespejo.</span><span class="sxs-lookup"><span data-stu-id="622d1-201">Developers also need to be aware of how their copy-protection scheme might affect the minidump.</span></span> <span data-ttu-id="622d1-202">A maioria dos esquemas de proteção de cópia tem suas próprias ferramentas de deembaralhamento, e cabe ao desenvolvedor aprender como usar essas ferramentas com o [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span><span class="sxs-lookup"><span data-stu-id="622d1-202">Most copy-protection schemes have their own descramble tools, and it is up to the developer to learn how to use those tools with [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump).</span></span>

## <a name="summary"></a><span data-ttu-id="622d1-203">Resumo</span><span class="sxs-lookup"><span data-stu-id="622d1-203">Summary</span></span>

<span data-ttu-id="622d1-204">A função [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) pode ser uma ferramenta extremamente útil para coletar e resolver bugs após o lançamento do produto.</span><span class="sxs-lookup"><span data-stu-id="622d1-204">The [**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump) function can be an extremely useful tool in collecting and solving bugs after the product has been released.</span></span> <span data-ttu-id="622d1-205">Escrever um manipulador de exceção personalizado que usa **MiniDumpWriteDump** permite que o desenvolvedor Personalize a coleta de informações e aprimore o processo de depuração.</span><span class="sxs-lookup"><span data-stu-id="622d1-205">Writing a custom exception handler that uses **MiniDumpWriteDump** allows the developer to customize the information collection and improve the debugging process.</span></span> <span data-ttu-id="622d1-206">A função é flexível o suficiente para ser usada em qualquer projeto baseado em C++ e deve ser considerada parte do processo de estabilidade de qualquer projeto.</span><span class="sxs-lookup"><span data-stu-id="622d1-206">The function is flexible enough to be used in any C++-based project and should be considered part of any project's stability process.</span></span>

 

 