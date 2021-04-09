---
description: O código a seguir demonstra como chamar a função SymFromName.
ms.assetid: d3a9d73e-fb77-4be3-a881-c258bcc587fe
title: Recuperando informações de símbolo por nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f5f4477be4f494383c7d9c1ca462f3beb69690
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089081"
---
# <a name="retrieving-symbol-information-by-name"></a><span data-ttu-id="e2e8e-103">Recuperando informações de símbolo por nome</span><span class="sxs-lookup"><span data-stu-id="e2e8e-103">Retrieving Symbol Information by Name</span></span>

<span data-ttu-id="e2e8e-104">O código a seguir demonstra como chamar a função [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) .</span><span class="sxs-lookup"><span data-stu-id="e2e8e-104">The following code demonstrates how to call the [**SymFromName**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromname) function.</span></span> <span data-ttu-id="e2e8e-105">Essa função preenche uma estrutura [**de \_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="e2e8e-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="e2e8e-106">Como o nome é variável em comprimento, você deve fornecer um buffer que seja grande o suficiente para manter o nome armazenado no final da estrutura **de \_ informações de símbolo** .</span><span class="sxs-lookup"><span data-stu-id="e2e8e-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="e2e8e-107">Além disso, o membro **MaxNameLen** deve ser definido como o número de bytes reservados para o nome.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="e2e8e-108">Neste exemplo, szSymbolName é um buffer que armazena o nome do símbolo solicitado.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-108">In this example, szSymbolName is a buffer that stores the name of the requested symbol.</span></span> <span data-ttu-id="e2e8e-109">O exemplo supõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolo](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="e2e8e-109">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR szSymbolName[MAX_SYM_NAME];
ULONG64 buffer[(sizeof(SYMBOL_INFO) +
    MAX_SYM_NAME * sizeof(TCHAR) +
    sizeof(ULONG64) - 1) /
    sizeof(ULONG64)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

_tcscpy_s(szSymbolName, MAX_SYM_NAME, TEXT("WinMain"));
pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromName(hProcess, szSymbolName, pSymbol))
{
    // SymFromName returned success
}
else
{
    // SymFromName failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymFromName returned error : %d\n"), error);
}
```



<span data-ttu-id="e2e8e-110">Se um aplicativo tiver um módulo ou nome de arquivo de origem, bem como informações de número de linha, ele poderá usar [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) para recuperar um endereço de código virtual.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-110">If an application has a module or source file name as well as line number information, it can use [**SymGetLineFromName64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromname) to retrieve a virtual code address.</span></span> <span data-ttu-id="e2e8e-111">Essa função requer um ponteiro para uma [**estrutura \_ LINE64 do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para receber o endereço de código virtual.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-111">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the virtual code address.</span></span> <span data-ttu-id="e2e8e-112">Observe que o manipulador de símbolos pode recuperar informações de número de linha somente quando \_ \_ a opção SYMOPT carregar linhas é definida usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="e2e8e-112">Note that the symbol handler can retrieve line number information only when SYMOPT\_LOAD\_LINES option is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="e2e8e-113">Essa opção deve ser definida antes de carregar o módulo.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-113">This option must be set before loading the module.</span></span> <span data-ttu-id="e2e8e-114">O parâmetro szModuleName contém o nome do módulo de origem; é opcional e pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-114">The szModuleName parameter contains the source module name; it is optional and can be **NULL**.</span></span> <span data-ttu-id="e2e8e-115">O parâmetro szFileName deve conter o nome do arquivo de origem e o parâmetro dwLineNumber deve conter o número de linha para o qual o endereço virtual será recuperado.</span><span class="sxs-lookup"><span data-stu-id="e2e8e-115">The szFileName parameter should contain the source file name, and dwLineNumber parameter should contain the line number for which the virtual address will be retrieved.</span></span>


```C++
TCHAR  szModuleName[MAX_PATH];
TCHAR  szFileName[MAX_PATH];
DWORD  dwLineNumber;
LONG   lDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
_tcscpy_s(szModuleName, MAX_PATH, TEXT("MyApp"));
_tcscpy_s(szFileName, MAX_PATH, TEXT("main.c"));
dwLineNumber = 248;

if (SymGetLineFromName64(hProcess, szModuleName, szFileName,
    dwLineNumber, &lDisplacement, &line))
{
    // SymGetLineFromName64 returned success
}
else
{
    // SymGetLineFromName64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromName64 returned error : %d\n"), error);
}
```



 

 



