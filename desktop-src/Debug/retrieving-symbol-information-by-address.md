---
description: O código a seguir demonstra como chamar a função SymFromAddr.
ms.assetid: 63dfadea-b0c4-4050-add8-d1f3aef7a495
title: Recuperando informações de símbolo por endereço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ad9d2879dbfd5820c4aa6c2e7563a1575ebe1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089082"
---
# <a name="retrieving-symbol-information-by-address"></a><span data-ttu-id="a04ab-103">Recuperando informações de símbolo por endereço</span><span class="sxs-lookup"><span data-stu-id="a04ab-103">Retrieving Symbol Information by Address</span></span>

<span data-ttu-id="a04ab-104">O código a seguir demonstra como chamar a função [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) .</span><span class="sxs-lookup"><span data-stu-id="a04ab-104">The following code demonstrates how to call the [**SymFromAddr**](/windows/desktop/api/Dbghelp/nf-dbghelp-symfromaddr) function.</span></span> <span data-ttu-id="a04ab-105">Essa função preenche uma estrutura [**de \_ informações de símbolo**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) .</span><span class="sxs-lookup"><span data-stu-id="a04ab-105">This function fills in a [**SYMBOL\_INFO**](/windows/desktop/api/DbgHelp/ns-dbghelp-symbol_info) structure.</span></span> <span data-ttu-id="a04ab-106">Como o nome é variável em comprimento, você deve fornecer um buffer que seja grande o suficiente para manter o nome armazenado no final da estrutura **de \_ informações de símbolo** .</span><span class="sxs-lookup"><span data-stu-id="a04ab-106">Because the name is variable in length, you must supply a buffer that is large enough to hold the name stored at the end of the **SYMBOL\_INFO** structure.</span></span> <span data-ttu-id="a04ab-107">Além disso, o membro **MaxNameLen** deve ser definido como o número de bytes reservados para o nome.</span><span class="sxs-lookup"><span data-stu-id="a04ab-107">Also, the **MaxNameLen** member must be set to the number of bytes reserved for the name.</span></span> <span data-ttu-id="a04ab-108">Neste exemplo, *dwAddress* é o endereço a ser mapeado para um símbolo.</span><span class="sxs-lookup"><span data-stu-id="a04ab-108">In this example, *dwAddress* is the address to be mapped to a symbol.</span></span> <span data-ttu-id="a04ab-109">A função **SymFromAddr** irá armazenar um deslocamento no início do símbolo para o endereço em *dwDisplacement*.</span><span class="sxs-lookup"><span data-stu-id="a04ab-109">The **SymFromAddr** function will store an offset to the beginning of the symbol to the address in *dwDisplacement*.</span></span> <span data-ttu-id="a04ab-110">O exemplo supõe que você tenha inicializado o manipulador de símbolo usando o código na [inicialização do manipulador de símbolo](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="a04ab-110">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
DWORD64  dwDisplacement = 0;
DWORD64  dwAddress = SOME_ADDRESS;

char buffer[sizeof(SYMBOL_INFO) + MAX_SYM_NAME * sizeof(TCHAR)];
PSYMBOL_INFO pSymbol = (PSYMBOL_INFO)buffer;

pSymbol->SizeOfStruct = sizeof(SYMBOL_INFO);
pSymbol->MaxNameLen = MAX_SYM_NAME;

if (SymFromAddr(hProcess, dwAddress, &dwDisplacement, pSymbol))
{
    // SymFromAddr returned success
}
else
{
    // SymFromAddr failed
    DWORD error = GetLastError();
    printf("SymFromAddr returned error : %d\n", error);
}
```



<span data-ttu-id="a04ab-111">Para recuperar o número de linha de código-fonte de um endereço especificado, um aplicativo pode usar [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span><span class="sxs-lookup"><span data-stu-id="a04ab-111">To retrieve the source code line number for a specified address, an application can use [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr).</span></span> <span data-ttu-id="a04ab-112">Essa função requer um ponteiro para uma [**estrutura \_ LINE64 do imagehlp**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) para receber o nome do arquivo de origem e o número da linha correspondente a um endereço de código especificado.</span><span class="sxs-lookup"><span data-stu-id="a04ab-112">This function requires a pointer to an [**IMAGEHLP\_LINE64**](/windows/desktop/api/DbgHelp/ns-dbghelp-imagehlp_line) structure to receive the source file name and line number corresponding to a specified code address.</span></span> <span data-ttu-id="a04ab-113">Observe que o manipulador de símbolos pode recuperar informações de número de linha somente quando **SYMOPT \_ \_ linhas de carregamento** são definidas usando a função [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="a04ab-113">Note that the symbol handler can retrieve line number information only when **SYMOPT\_LOAD\_LINES** is set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span> <span data-ttu-id="a04ab-114">Essa opção deve ser definida antes de carregar o módulo.</span><span class="sxs-lookup"><span data-stu-id="a04ab-114">This option must be set before loading the module.</span></span> <span data-ttu-id="a04ab-115">O parâmetro dwAddress contém o endereço de código para o qual o nome do arquivo de origem e o número da linha serão localizados.</span><span class="sxs-lookup"><span data-stu-id="a04ab-115">The dwAddress parameter contains the code address for which the source file name and line number will be located.</span></span>


```C++
DWORD64  dwAddress;
DWORD  dwDisplacement;
IMAGEHLP_LINE64 line;

SymSetOptions(SYMOPT_LOAD_LINES);

line.SizeOfStruct = sizeof(IMAGEHLP_LINE64);
dwAddress = 0x1000000; // Address you want to check on.

if (SymGetLineFromAddr64(hProcess, dwAddress, &dwDisplacement, &line))
{
    // SymGetLineFromAddr64 returned success
}
else
{
    // SymGetLineFromAddr64 failed
    DWORD error = GetLastError();
    _tprintf(TEXT("SymGetLineFromAddr64 returned error : %d\n"), error);
}
```



 

 



