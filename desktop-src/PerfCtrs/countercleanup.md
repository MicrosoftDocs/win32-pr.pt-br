---
description: Remove o registro de provedores.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Função de metalimpeza
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754617"
---
# <a name="countercleanup-function"></a><span data-ttu-id="0eac3-103">Função de metalimpeza</span><span class="sxs-lookup"><span data-stu-id="0eac3-103">CounterCleanup function</span></span>

<span data-ttu-id="0eac3-104">Remove o registro do provedor.</span><span class="sxs-lookup"><span data-stu-id="0eac3-104">Removes the provider's registration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eac3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0eac3-105">Syntax</span></span>


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a><span data-ttu-id="0eac3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eac3-106">Parameters</span></span>

<span data-ttu-id="0eac3-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0eac3-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0eac3-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0eac3-108">Return value</span></span>

<span data-ttu-id="0eac3-109">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0eac3-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eac3-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0eac3-110">Remarks</span></span>

<span data-ttu-id="0eac3-111">Seu provedor chama essa função.</span><span class="sxs-lookup"><span data-stu-id="0eac3-111">Your provider calls this function.</span></span> <span data-ttu-id="0eac3-112">A função chama a função [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para remover o registro do provedor.</span><span class="sxs-lookup"><span data-stu-id="0eac3-112">The function calls the [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) function to remove the provider's registration.</span></span>

<span data-ttu-id="0eac3-113">A ferramenta [**ctrpp**](ctrpp.md) gera essa função embutida quando você especifica o argumento **-o** .</span><span class="sxs-lookup"><span data-stu-id="0eac3-113">The [**CTRPP**](ctrpp.md) tool generates this inline function when you specify the **-o** argument.</span></span> <span data-ttu-id="0eac3-114">O nome da função inclui uma cadeia de caracteres de *prefixo* se você especificar o argumento **-prefix** (por exemplo, **_prefix_CounterCleanup**.</span><span class="sxs-lookup"><span data-stu-id="0eac3-114">The function's name includes a *prefix* string if you specify the **-prefix** argument (for example, **_prefix_CounterCleanup**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eac3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0eac3-115">Requirements</span></span>



| <span data-ttu-id="0eac3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eac3-116">Requirement</span></span> | <span data-ttu-id="0eac3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0eac3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0eac3-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0eac3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0eac3-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0eac3-119">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0eac3-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0eac3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0eac3-121">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="0eac3-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




