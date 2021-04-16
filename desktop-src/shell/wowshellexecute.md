---
description: Executa uma operação em um arquivo especificado.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: Função WOWShellExecute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187803"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="adbfe-103">Função WOWShellExecute</span><span class="sxs-lookup"><span data-stu-id="adbfe-103">WOWShellExecute function</span></span>

<span data-ttu-id="adbfe-104">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="adbfe-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="adbfe-105">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="adbfe-106">Executa uma operação em um arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="adbfe-107">**WOWShellExecute** existe apenas para uso com o computador virtual dos do Microsoft Windows NT (Ntvdm.exe), que permite que o sistema operacional de disco (dos) e o software de 16 bits sejam executados em um sistema Windows e não deve ser usado por outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="adbfe-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="adbfe-108">Em vez disso, use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="adbfe-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbfe-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="adbfe-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="adbfe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="adbfe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adbfe-111">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbfe-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="adbfe-112">Type: **HWND**</span></span>

<span data-ttu-id="adbfe-113">Um identificador para a janela do proprietário usado para exibir uma interface do usuário ou mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="adbfe-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="adbfe-114">Esse valor pode ser **nulo** se a operação não estiver associada a uma janela.</span><span class="sxs-lookup"><span data-stu-id="adbfe-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="adbfe-115">*lpOperation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbfe-116">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="adbfe-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="adbfe-117">Um ponteiro para uma cadeia de caracteres terminada em **nulo**, referido neste caso como um *verbo*, que especifica a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="adbfe-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="adbfe-118">O conjunto de verbos disponíveis depende do arquivo ou da pasta em particular.</span><span class="sxs-lookup"><span data-stu-id="adbfe-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="adbfe-119">Em geral, as ações disponíveis no menu de atalho de um objeto são verbos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="adbfe-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="adbfe-120">Para obter mais informações sobre verbos e sua disponibilidade, consulte a seção *verbos de objeto* de [iniciando aplicativos](launch.md).</span><span class="sxs-lookup"><span data-stu-id="adbfe-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="adbfe-121">Consulte [estendendo menus de atalho](context.md) para mais discussões sobre menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="adbfe-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="adbfe-122">Os verbos a seguir são usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="adbfe-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="adbfe-123"><span id="edit"></span><span id="EDIT"></span>**editar**</span><span class="sxs-lookup"><span data-stu-id="adbfe-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="adbfe-124">Inicia um editor e abre o documento para edição.</span><span class="sxs-lookup"><span data-stu-id="adbfe-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="adbfe-125">Se *lpFile* não for um arquivo de documento, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="adbfe-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="adbfe-126"><span id="explore"></span><span id="EXPLORE"></span>**apresenta**</span><span class="sxs-lookup"><span data-stu-id="adbfe-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="adbfe-127">Explora a pasta especificada por *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="adbfe-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="adbfe-128"><span id="find"></span><span id="FIND"></span>**considerar**</span><span class="sxs-lookup"><span data-stu-id="adbfe-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="adbfe-129">Inicia uma pesquisa a partir do diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="adbfe-130"><span id="open"></span><span id="OPEN"></span>**abrir**</span><span class="sxs-lookup"><span data-stu-id="adbfe-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="adbfe-131">Abre o arquivo especificado pelo parâmetro *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="adbfe-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="adbfe-132">O arquivo pode ser um arquivo executável, um arquivo de documento ou uma pasta.</span><span class="sxs-lookup"><span data-stu-id="adbfe-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="adbfe-133"><span id="print"></span><span id="PRINT"></span>**imprimir**</span><span class="sxs-lookup"><span data-stu-id="adbfe-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="adbfe-134">Imprime o arquivo de documento especificado por *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="adbfe-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="adbfe-135">Se *lpFile* não for um arquivo de documento, a função falhará.</span><span class="sxs-lookup"><span data-stu-id="adbfe-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="adbfe-136"><span id="NULL"></span><span id="null"></span>**NULO**</span><span class="sxs-lookup"><span data-stu-id="adbfe-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="adbfe-137">Para sistemas anteriores ao Windows 2000, o verbo padrão é usado se ele é válido e está disponível no registro.</span><span class="sxs-lookup"><span data-stu-id="adbfe-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="adbfe-138">Caso contrário, o verbo "Open" será usado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="adbfe-139">Para sistemas Windows 2000 e posteriores, o verbo padrão é usado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="adbfe-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="adbfe-140">Caso contrário, o verbo "Open" será usado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="adbfe-141">Se nenhum verbo estiver disponível, o sistema usará o primeiro verbo listado no registro.</span><span class="sxs-lookup"><span data-stu-id="adbfe-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="adbfe-142">*lpFile* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbfe-143">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="adbfe-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="adbfe-144">Um ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica o arquivo ou objeto no qual executar o verbo especificado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="adbfe-145">Para especificar um objeto de namespace de Shell, passe o nome de análise totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="adbfe-146">Observe que nem todos os verbos têm suporte em todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="adbfe-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="adbfe-147">Por exemplo, nem todos os tipos de documento dão suporte ao verbo "Print".</span><span class="sxs-lookup"><span data-stu-id="adbfe-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="adbfe-148">*lpParameters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbfe-149">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="adbfe-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="adbfe-150">Se o parâmetro *lpFile* especificar um arquivo executável, *lpParameters* será um ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica os parâmetros a serem passados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="adbfe-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="adbfe-151">O formato dessa cadeia de caracteres é determinado pelo verbo a ser invocado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="adbfe-152">Se *lpFile* especificar um arquivo de documento, *LpParameters* deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="adbfe-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="adbfe-153">*lpDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbfe-154">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="adbfe-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="adbfe-155">Um ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica o diretório padrão.</span><span class="sxs-lookup"><span data-stu-id="adbfe-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="adbfe-156">*nShowCmd* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="adbfe-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="adbfe-157">Type: **INT**</span></span>

<span data-ttu-id="adbfe-158">Os sinalizadores que especificam como um aplicativo deve ser exibido quando ele é aberto.</span><span class="sxs-lookup"><span data-stu-id="adbfe-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="adbfe-159">Se *lpFile* especificar um arquivo de documento, o sinalizador será simplesmente passado para o aplicativo associado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="adbfe-160">Cabe ao aplicativo decidir como tratá-lo.</span><span class="sxs-lookup"><span data-stu-id="adbfe-160">It is up to the application to decide how to handle it.</span></span> <span data-ttu-id="adbfe-161">Pode ser qualquer um dos valores que podem ser especificados no parâmetro *nCmdShow* para a função de [janela](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="adbfe-161">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="adbfe-162">*lpfnCBWinExec*</span><span class="sxs-lookup"><span data-stu-id="adbfe-162">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="adbfe-163">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="adbfe-163">Type: **void\***</span></span>

<span data-ttu-id="adbfe-164">Função de retorno de chamada usada para chamar [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) no kernel de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="adbfe-164">Callback function used to call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adbfe-165">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="adbfe-165">Return value</span></span>

<span data-ttu-id="adbfe-166">Tipo: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="adbfe-166">Type: **HINSTANCE**</span></span>

<span data-ttu-id="adbfe-167">Retorna um valor maior que 32 se for bem-sucedido ou um valor de erro menor ou igual a 32, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="adbfe-167">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="adbfe-168">A tabela a seguir lista os valores de erro.</span><span class="sxs-lookup"><span data-stu-id="adbfe-168">The following table lists the error values.</span></span> <span data-ttu-id="adbfe-169">O valor de retorno é convertido como um HINSTANCE para compatibilidade com versões anteriores com aplicativos do Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="adbfe-169">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="adbfe-170">No entanto, não é um verdadeiro HINSTANCE.</span><span class="sxs-lookup"><span data-stu-id="adbfe-170">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="adbfe-171">A única coisa que pode ser feita com o HINSTANCE retornado é convertê-lo em um **int** e compará-lo com o valor 32 ou um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="adbfe-171">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="adbfe-172">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="adbfe-172">Return code</span></span>                                                                                             | <span data-ttu-id="adbfe-173">Descrição</span><span class="sxs-lookup"><span data-stu-id="adbfe-173">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="adbfe-174"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-174"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="adbfe-175">O sistema operacional está sem memória ou recursos.</span><span class="sxs-lookup"><span data-stu-id="adbfe-175">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="adbfe-176"><dt>**arquivo de erro \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-176"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="adbfe-177">O arquivo especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-177">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="adbfe-178"><dt>**caminho de erro \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-178"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="adbfe-179">O caminho especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-179">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="adbfe-180"><dt>**ERRO \_ de \_ formato inadequado**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-180"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="adbfe-181">O arquivo. exe é inválido (não Win32. exe ou erro na imagem. exe).</span><span class="sxs-lookup"><span data-stu-id="adbfe-181">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="adbfe-182"><dt>**SE \_ Err \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-182"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="adbfe-183">O sistema operacional negou o acesso ao arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-183">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="adbfe-184"><dt>**SE \_ Err \_ ASSOCINCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-184"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="adbfe-185">A associação de nome de arquivo está incompleta ou inválida.</span><span class="sxs-lookup"><span data-stu-id="adbfe-185">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="adbfe-186"><dt>**SE \_ Err \_ DDEBUSY**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-186"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="adbfe-187">A transação DDE não pôde ser concluída porque outras transações DDE estavam sendo processadas.</span><span class="sxs-lookup"><span data-stu-id="adbfe-187">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="adbfe-188"><dt>**SE \_ Err \_ DDEFAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-188"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="adbfe-189">Falha na transação DDE.</span><span class="sxs-lookup"><span data-stu-id="adbfe-189">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="adbfe-190"><dt>**SE \_ Err \_ DDETIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-190"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="adbfe-191">A transação DDE não pôde ser concluída porque o tempo limite da solicitação foi atingido.</span><span class="sxs-lookup"><span data-stu-id="adbfe-191">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="adbfe-192"><dt>**SE \_ Err \_ DLLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-192"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="adbfe-193">A DLL especificada não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="adbfe-193">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="adbfe-194"><dt>**SE \_ Err \_ FNF**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-194"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="adbfe-195">O arquivo especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-195">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="adbfe-196"><dt>**SE \_ Err \_ noassoc**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-196"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="adbfe-197">Não há nenhum aplicativo associado à extensão de nome de arquivo fornecida.</span><span class="sxs-lookup"><span data-stu-id="adbfe-197">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="adbfe-198">Esse erro também será retornado se você tentar imprimir um arquivo que não seja imprimível.</span><span class="sxs-lookup"><span data-stu-id="adbfe-198">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="adbfe-199"><dt>**inoom de \_ erro se \_**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-199"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="adbfe-200">Não havia memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="adbfe-200">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="adbfe-201"><dt>**SE \_ erro \_ PNF**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-201"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="adbfe-202">O caminho especificado não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="adbfe-202">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="adbfe-203"><dt>**\_compartilhamento de erro se \_**</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-203"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="adbfe-204">Ocorreu uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="adbfe-204">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="adbfe-205">Comentários</span><span class="sxs-lookup"><span data-stu-id="adbfe-205">Remarks</span></span>

<span data-ttu-id="adbfe-206">**WOWShellExecute** não está incluído em um cabeçalho ou em um arquivo. lib.</span><span class="sxs-lookup"><span data-stu-id="adbfe-206">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="adbfe-207">Ele é exportado de Shell32.dll por nome.</span><span class="sxs-lookup"><span data-stu-id="adbfe-207">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="adbfe-208">Esse método permite executar qualquer comando no menu de atalho de uma pasta ou armazenado no registro.</span><span class="sxs-lookup"><span data-stu-id="adbfe-208">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="adbfe-209">Se *lpOperation* for **NULL**, a função abrirá o arquivo especificado por *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="adbfe-209">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="adbfe-210">Se *lpOperation* for "Open" ou "Explore", a função tentará abrir ou explorar a pasta.</span><span class="sxs-lookup"><span data-stu-id="adbfe-210">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="adbfe-211">Para obter informações sobre o aplicativo que é iniciado como resultado da chamada de **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="adbfe-211">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="adbfe-212">As **janelas de pasta de inicialização em uma configuração de processo separada** em opções de pasta afetam **WOWShellExecute**.</span><span class="sxs-lookup"><span data-stu-id="adbfe-212">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="adbfe-213">Se essa opção estiver desabilitada (a configuração padrão), o **WOWShellExecute** usará uma janela aberta do Explorer em vez de iniciar uma nova.</span><span class="sxs-lookup"><span data-stu-id="adbfe-213">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="adbfe-214">Se nenhuma janela do Explorer estiver aberta, o **WOWShellExecute** iniciará uma nova.</span><span class="sxs-lookup"><span data-stu-id="adbfe-214">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="adbfe-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adbfe-215">Requirements</span></span>



| <span data-ttu-id="adbfe-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="adbfe-216">Requirement</span></span> | <span data-ttu-id="adbfe-217">Valor</span><span class="sxs-lookup"><span data-stu-id="adbfe-217">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="adbfe-218">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adbfe-218">Minimum supported client</span></span><br/> | <span data-ttu-id="adbfe-219">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-219">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="adbfe-220">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="adbfe-220">Minimum supported server</span></span><br/> | <span data-ttu-id="adbfe-221">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="adbfe-221">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="adbfe-222">DLL</span><span class="sxs-lookup"><span data-stu-id="adbfe-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbfe-223"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adbfe-223"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adbfe-224">Confira também</span><span class="sxs-lookup"><span data-stu-id="adbfe-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adbfe-225">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="adbfe-225">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
