---
title: O console do AccChecker
description: AccChecker console (AccCheckConsole.exe) é uma ferramenta de linha de comando para verificar a implementação de acessibilidade da interface do usuário do seu aplicativo.
ms.assetid: 9E80BFDD-FB5D-45C5-BE69-7036AD29D863
keywords:
- Console do AccChecker
- Ferramenta de linha de comando AccChecker
- linha de comando, AccChecker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef010b2079d364c43bf2a6e47b0e3b0f24bb37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822338"
---
# <a name="the-accchecker-console"></a><span data-ttu-id="69a4b-106">O console do AccChecker</span><span class="sxs-lookup"><span data-stu-id="69a4b-106">The AccChecker Console</span></span>

<span data-ttu-id="69a4b-107">AccChecker console (AccCheckConsole.exe) é uma ferramenta de linha de comando para verificar a implementação de acessibilidade da interface do usuário do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69a4b-107">AccChecker Console (AccCheckConsole.exe) is a command-line tool for verifying the accessibility implementation of your application's UI.</span></span> <span data-ttu-id="69a4b-108">A linha de comando aceita uma variedade de entradas (como HWND, título da janela e rotina de verificação) e fornece um código de saída que corresponde à contagem de log de erros.</span><span class="sxs-lookup"><span data-stu-id="69a4b-108">The command-line accepts a variety of inputs (such as HWND, window title, and verification routine) and supplies an exit code that corresponds to the error log count.</span></span>

-   [<span data-ttu-id="69a4b-109">Sintaxe de linha de comando</span><span class="sxs-lookup"><span data-stu-id="69a4b-109">Command-line Syntax</span></span>](#command-line-syntax)
-   [<span data-ttu-id="69a4b-110">Códigos de erro de linha de comando</span><span class="sxs-lookup"><span data-stu-id="69a4b-110">Command-line Error Codes</span></span>](#command-line-error-codes)
-   [<span data-ttu-id="69a4b-111">Exemplos de linha de comando</span><span class="sxs-lookup"><span data-stu-id="69a4b-111">Command-line Examples</span></span>](#command-line-examples)
-   [<span data-ttu-id="69a4b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69a4b-112">Related topics</span></span>](#related-topics)

![ferramenta de linha de comando do console do accchecker](images/accchecker-console.png)

## <a name="command-line-syntax"></a><span data-ttu-id="69a4b-114">Sintaxe da linha de comando</span><span class="sxs-lookup"><span data-stu-id="69a4b-114">Command-line Syntax</span></span>

<span data-ttu-id="69a4b-115">O console do AccChecker tem a seguinte sintaxe de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="69a4b-115">AccChecker Console has the following command-line syntax.</span></span>

<span data-ttu-id="69a4b-116">**Opções de AccCheckConsole \[ \] (-HWND <hwnd> \| -process <name> ) \[<dlls>\]**</span><span class="sxs-lookup"><span data-stu-id="69a4b-116">**AccCheckConsole \[options\] (-hwnd <hwnd> \| -process <name>) \[<dlls>\]**</span></span>

<span data-ttu-id="69a4b-117">As opções de linha de comando são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="69a4b-117">The command-line options are as follows.</span></span>



| <span data-ttu-id="69a4b-118">Opções</span><span class="sxs-lookup"><span data-stu-id="69a4b-118">Options</span></span>                                                                                                                                                         | <span data-ttu-id="69a4b-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="69a4b-119">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69a4b-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-HWND <hwnd></span><span class="sxs-lookup"><span data-stu-id="69a4b-120"><span id="-hwnd__hwnd_"></span><span id="-HWND__HWND_"></span>-hwnd <hwnd></span></span><br/>                                                                     | <span data-ttu-id="69a4b-121">Valida a janela que tem o identificador especificado (HWND).</span><span class="sxs-lookup"><span data-stu-id="69a4b-121">Validates the window that has the specified handle (HWND).</span></span> <span data-ttu-id="69a4b-122">O identificador pode ser especificado em hexadecimal ou Decimal.</span><span class="sxs-lookup"><span data-stu-id="69a4b-122">The handle can be specified in hexidecimal or decimal.</span></span><br/> |
| <span data-ttu-id="69a4b-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-janela <title></span><span class="sxs-lookup"><span data-stu-id="69a4b-123"><span id="-window__title_"></span><span id="-WINDOW__TITLE_"></span>-window <title></span></span><br/>                                                            | <span data-ttu-id="69a4b-124">Valida a janela que tem o título especificado.</span><span class="sxs-lookup"><span data-stu-id="69a4b-124">Validates the window that has the specified title.</span></span><br/>                                                                |
| <span data-ttu-id="69a4b-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -processo <name></span><span class="sxs-lookup"><span data-stu-id="69a4b-125"><span id="__________________-process__name_"></span><span id="__________________-PROCESS__NAME_"></span> -process <name></span></span><br/>                       | <span data-ttu-id="69a4b-126">Valida a janela principal do processo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="69a4b-126">Validates the main window of the process that has the specified name.</span></span><br/>                                             |
| <span data-ttu-id="69a4b-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -lista</span><span class="sxs-lookup"><span data-stu-id="69a4b-127"><span id="____________________________-list"></span><span id="____________________________-LIST"></span> -list</span></span><br/>                                       | <span data-ttu-id="69a4b-128">Lista todas as rotinas de verificação disponíveis.</span><span class="sxs-lookup"><span data-stu-id="69a4b-128">Lists all of the available verification routines.</span></span><br/>                                                                 |
| <span data-ttu-id="69a4b-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -habilitar <name></span><span class="sxs-lookup"><span data-stu-id="69a4b-129"><span id="__________________-enable__name_"></span><span id="__________________-ENABLE__NAME_"></span> -enable <name></span></span><br/>                          | <span data-ttu-id="69a4b-130">Executa a rotina de verificação especificada.</span><span class="sxs-lookup"><span data-stu-id="69a4b-130">Runs the specified verification routine.</span></span> <span data-ttu-id="69a4b-131">Essa opção pode ser especificada mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="69a4b-131">This option can be specified more than once.</span></span><br/>                             |
| <span data-ttu-id="69a4b-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -desabilitar <name></span><span class="sxs-lookup"><span data-stu-id="69a4b-132"><span id="_____________________________-disable__name_"></span><span id="_____________________________-DISABLE__NAME_"></span> -disable <name></span></span><br/> | <span data-ttu-id="69a4b-133">Executa tudo, exceto a rotina de verificação especificada.</span><span class="sxs-lookup"><span data-stu-id="69a4b-133">Runs all but the specified verification routine.</span></span> <span data-ttu-id="69a4b-134">Essa opção pode ser especificada mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="69a4b-134">This option can be specified more than once.</span></span><br/>                     |
| <span data-ttu-id="69a4b-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (erro de aviso de informação \| \| )</span><span class="sxs-lookup"><span data-stu-id="69a4b-135"><span id="___________-log__info_warn_err_"></span><span id="___________-LOG__INFO_WARN_ERR_"></span> -log (info\|warn\|err)</span></span><br/>                          | <span data-ttu-id="69a4b-136">A classificação de eventos mais baixa que será registrada em log.</span><span class="sxs-lookup"><span data-stu-id="69a4b-136">The lowest event rating that will be logged.</span></span><br/>                                                                      |
| <span data-ttu-id="69a4b-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -Logfile <file></span><span class="sxs-lookup"><span data-stu-id="69a4b-137"><span id="__________________-logfile__file_"></span><span id="__________________-LOGFILE__FILE_"></span> -logfile <file></span></span><br/>                       | <span data-ttu-id="69a4b-138">Grave a saída no arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="69a4b-138">Write the output to the specified log file.</span></span> <span data-ttu-id="69a4b-139">Essa opção pode ser especificada mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="69a4b-139">This option can be specified more than once.</span></span><br/>                          |
| <span data-ttu-id="69a4b-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suprimir <file></span><span class="sxs-lookup"><span data-stu-id="69a4b-140"><span id="-suppress__file_"></span><span id="-SUPPRESS__FILE_"></span>-suppress <file></span></span><br/>                                                         | <span data-ttu-id="69a4b-141">Use o arquivo XML especificado para suprimir erros.</span><span class="sxs-lookup"><span data-stu-id="69a4b-141">Use the specified XML file to suppress errors.</span></span> <br/>                                                                   |
| <span data-ttu-id="69a4b-142"><span id="-quiet"></span><span id="-QUIET"></span>-Quiet</span><span class="sxs-lookup"><span data-stu-id="69a4b-142"><span id="-quiet"></span><span id="-QUIET"></span>-quiet</span></span><br/>                                                                                             | <span data-ttu-id="69a4b-143">Não grave a saída de log para stdout.</span><span class="sxs-lookup"><span data-stu-id="69a4b-143">Do not write logging output to stdout.</span></span><br/>                                                                            |
| <span data-ttu-id="69a4b-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-ajuda</span><span class="sxs-lookup"><span data-stu-id="69a4b-144"><span id="-help__________________________________"></span><span id="-HELP__________________________________"></span>-help</span></span> <br/>                           | <span data-ttu-id="69a4b-145">Exibe a ajuda rápida.</span><span class="sxs-lookup"><span data-stu-id="69a4b-145">Displays quick help.</span></span> <br/>                                                                                             |



 

## <a name="command-line-error-codes"></a><span data-ttu-id="69a4b-146">Códigos de erro de linha de comando</span><span class="sxs-lookup"><span data-stu-id="69a4b-146">Command-line Error Codes</span></span>

<span data-ttu-id="69a4b-147">Veja a seguir os códigos de erro retornados de AccCheckConsole ao usar "Echo% ERRORLEVEL%"</span><span class="sxs-lookup"><span data-stu-id="69a4b-147">Following are error codes returned from AccCheckConsole when using "echo %errorlevel%"</span></span>



| <span data-ttu-id="69a4b-148">Código do erro</span><span class="sxs-lookup"><span data-stu-id="69a4b-148">Error code</span></span>                       | <span data-ttu-id="69a4b-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="69a4b-149">Description</span></span>                                 |
|----------------------------------|---------------------------------------------|
| <span data-ttu-id="69a4b-150"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="69a4b-150"><span id="0"></span>0</span></span><br/> | <span data-ttu-id="69a4b-151">Nenhum erro e nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="69a4b-151">No errors and no warnings.</span></span><br/>       |
| <span data-ttu-id="69a4b-152"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="69a4b-152"><span id="1"></span>1</span></span><br/> | <span data-ttu-id="69a4b-153">Instrução Usages foi solicitada.</span><span class="sxs-lookup"><span data-stu-id="69a4b-153">Usages statement was requested.</span></span> <br/> |
| <span data-ttu-id="69a4b-154"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="69a4b-154"><span id="2"></span>2</span></span><br/> | <span data-ttu-id="69a4b-155">Erros e nenhum aviso.</span><span class="sxs-lookup"><span data-stu-id="69a4b-155">Errors and no warnings.</span></span><br/>          |
| <span data-ttu-id="69a4b-156"><span id="3"></span>Beta</span><span class="sxs-lookup"><span data-stu-id="69a4b-156"><span id="3"></span>3</span></span><br/> | <span data-ttu-id="69a4b-157">Erros e avisos.</span><span class="sxs-lookup"><span data-stu-id="69a4b-157">Errors and warnings.</span></span><br/>             |
| <span data-ttu-id="69a4b-158"><span id="4"></span>4</span><span class="sxs-lookup"><span data-stu-id="69a4b-158"><span id="4"></span>4</span></span><br/> | <span data-ttu-id="69a4b-159">Avisos, mas sem erros.</span><span class="sxs-lookup"><span data-stu-id="69a4b-159">Warnings but no errors.</span></span><br/>          |
| <span data-ttu-id="69a4b-160"><span id="5"></span>05</span><span class="sxs-lookup"><span data-stu-id="69a4b-160"><span id="5"></span>5</span></span><br/> | <span data-ttu-id="69a4b-161">Linha de comando inválida.</span><span class="sxs-lookup"><span data-stu-id="69a4b-161">Invalid command line.</span></span> <br/>           |



 

## <a name="command-line-examples"></a><span data-ttu-id="69a4b-162">Exemplos de linha de comando</span><span class="sxs-lookup"><span data-stu-id="69a4b-162">Command-line Examples</span></span>

<span data-ttu-id="69a4b-163">A seguir estão vários exemplos de linha de comando do console AccChecker.</span><span class="sxs-lookup"><span data-stu-id="69a4b-163">Following are several AccChecker Console command-line examples.</span></span>

-   <span data-ttu-id="69a4b-164">Executar todas as verificações em uma janela com um nome especificado.</span><span class="sxs-lookup"><span data-stu-id="69a4b-164">Run all verifications on a window with a specified name.</span></span>

    <span data-ttu-id="69a4b-165">**AccCheckConsole-janela "sem título – bloco de notas"**</span><span class="sxs-lookup"><span data-stu-id="69a4b-165">**AccCheckConsole -window "Untitled - Notepad"**</span></span>

-   <span data-ttu-id="69a4b-166">Executar um subconjunto das verificações em um HWND, especificando um arquivo de supressão.</span><span class="sxs-lookup"><span data-stu-id="69a4b-166">Run a subset of the verifications against an HWND, specifying a suppression file.</span></span>

    <span data-ttu-id="69a4b-167">**AccCheckConsole-HWND 0x00382f00-habilitar CheckTabbing-habilitar CHECKNAME-suprime suppress.xml**</span><span class="sxs-lookup"><span data-stu-id="69a4b-167">**AccCheckConsole -hwnd 0x00382f00 -enable CheckTabbing -enable CheckName -suppress suppress.xml**</span></span>

-   <span data-ttu-id="69a4b-168">Execute todas as verificações de uma nova DLL de verificação.</span><span class="sxs-lookup"><span data-stu-id="69a4b-168">Run all verifications from a new verification DLL.</span></span>

    <span data-ttu-id="69a4b-169">**AccCheckConsole-janela "sem título-bloco de notas" VerificationRoutine1.dll**</span><span class="sxs-lookup"><span data-stu-id="69a4b-169">**AccCheckConsole -window "Untitled - Notepad" VerificationRoutine1.dll**</span></span>

## <a name="related-topics"></a><span data-ttu-id="69a4b-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69a4b-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a4b-171">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="69a4b-171">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 





