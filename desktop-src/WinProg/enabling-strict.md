---
title: Habilitando STRICT
description: Ao definir o símbolo estrito, você habilita recursos que exigem mais cuidado na declaração e no uso de tipos.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "105764476"
---
# <a name="enabling-strict"></a><span data-ttu-id="57610-103">Habilitando STRICT</span><span class="sxs-lookup"><span data-stu-id="57610-103">Enabling STRICT</span></span>

<span data-ttu-id="57610-104">Ao definir o símbolo **estrito** , você habilita recursos que exigem mais cuidado na declaração e no uso de tipos.</span><span class="sxs-lookup"><span data-stu-id="57610-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="57610-105">Isso ajuda a escrever código mais portátil.</span><span class="sxs-lookup"><span data-stu-id="57610-105">This helps you write more portable code.</span></span> <span data-ttu-id="57610-106">Esse cuidado extra também reduzirá o tempo de depuração.</span><span class="sxs-lookup"><span data-stu-id="57610-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="57610-107">Habilitar **estrito** redefine determinados tipos de dados para que o compilador não permita a atribuição de um tipo para outro sem uma conversão explícita.</span><span class="sxs-lookup"><span data-stu-id="57610-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="57610-108">Isso é especialmente útil com o código do Windows.</span><span class="sxs-lookup"><span data-stu-id="57610-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="57610-109">Erros na passagem de tipos de dados são relatados em tempo de compilação em vez de causar erros fatais em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="57610-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="57610-110">Com Visual C++, a verificação de tipo **estrito** é definida por padrão.</span><span class="sxs-lookup"><span data-stu-id="57610-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="57610-111">Para definir **Strict** em uma base file-by-file, insira uma instrução de **\# definição** antes de incluir Windows. h:</span><span class="sxs-lookup"><span data-stu-id="57610-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="57610-112">Quando **Strict** é definido, as definições de [tipo de dados](windows-data-types.md) são alteradas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="57610-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="57610-113">Tipos de identificador específicos são definidos para serem mutuamente exclusivos; por exemplo, você não poderá passar um **HWND** onde um argumento de tipo **HDC** é necessário.</span><span class="sxs-lookup"><span data-stu-id="57610-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="57610-114">Sem **estrito**, todos os identificadores são definidos como **identificadores**, portanto, o compilador não impede que você use um tipo de identificador em que outro tipo é esperado.</span><span class="sxs-lookup"><span data-stu-id="57610-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="57610-115">Todos os tipos de função de retorno de chamada (como procedimentos de caixa de diálogo, procedimentos de janela e procedimentos de gancho) são definidos com protótipos completos.</span><span class="sxs-lookup"><span data-stu-id="57610-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="57610-116">Isso impede que você declare funções de retorno de chamada com listas de parâmetros incorretas.</span><span class="sxs-lookup"><span data-stu-id="57610-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="57610-117">Os tipos de valor de parâmetro e de retorno que devem usar um ponteiro genérico são declarados corretamente como **LPVOID** , em vez de um **LPSTR** ou outro tipo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="57610-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="57610-118">A estrutura [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) é declarada de acordo com o padrão ANSI.</span><span class="sxs-lookup"><span data-stu-id="57610-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57610-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57610-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57610-120">Desabilitando estrito</span><span class="sxs-lookup"><span data-stu-id="57610-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="57610-121">Conformidade estrita</span><span class="sxs-lookup"><span data-stu-id="57610-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
