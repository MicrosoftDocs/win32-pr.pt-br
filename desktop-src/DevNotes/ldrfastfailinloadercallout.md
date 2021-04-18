---
description: Essa função força o programa de chamada se ele for invocado dentro de um texto explicativo do carregador. Caso contrário, ele não terá nenhum efeito.
ms.assetid: 5C10BF04-B7C7-4481-A184-FDD418FE5F52
title: Função LdrFastFailInLoaderCallout
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrFastFailInLoaderCallout
api_type:
- DllExport
api_location:
- NTDll.dll
ms.openlocfilehash: f74b9cdc0aec666242a8267fab8d6255c75dc94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754078"
---
# <a name="ldrfastfailinloadercallout-function"></a><span data-ttu-id="7b98d-104">Função LdrFastFailInLoaderCallout</span><span class="sxs-lookup"><span data-stu-id="7b98d-104">LdrFastFailInLoaderCallout function</span></span>

<span data-ttu-id="7b98d-105">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7b98d-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7b98d-106">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7b98d-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7b98d-107">Essa função força o programa de chamada se ele for invocado dentro de um texto explicativo do carregador.</span><span class="sxs-lookup"><span data-stu-id="7b98d-107">This function forcefully terminates the calling program if it is invoked inside a loader callout.</span></span> <span data-ttu-id="7b98d-108">Caso contrário, ele não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="7b98d-108">Otherwise, it has no effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b98d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b98d-109">Syntax</span></span>


```C++
VOID NTAPI LdrFastFailInLoaderCallout(void);
```



## <a name="parameters"></a><span data-ttu-id="7b98d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7b98d-110">Parameters</span></span>

<span data-ttu-id="7b98d-111">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7b98d-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b98d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7b98d-112">Return value</span></span>

<span data-ttu-id="7b98d-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7b98d-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b98d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b98d-114">Remarks</span></span>

<span data-ttu-id="7b98d-115">Essa rotina não captura todos os casos de deadlock em potencial; é possível que um thread dentro de um carregador de texto explicativo obtenha um bloqueio enquanto algum thread fora de um carregador de texto contém o mesmo bloqueio e faz uma chamada para o carregador.</span><span class="sxs-lookup"><span data-stu-id="7b98d-115">This routine does not catch all potential deadlock cases; it is possible for a thread inside a loader callout to acquire a lock while some thread outside a loader callout holds the same lock and makes a call into the loader.</span></span> <span data-ttu-id="7b98d-116">Em outras palavras, pode haver uma inversão de ordem de bloqueio entre o bloqueio de carregador e um bloqueio de cliente.</span><span class="sxs-lookup"><span data-stu-id="7b98d-116">In other words, there can be a lock order inversion between the loader lock and a client lock.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b98d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b98d-117">Requirements</span></span>



| <span data-ttu-id="7b98d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b98d-118">Requirement</span></span> | <span data-ttu-id="7b98d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7b98d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7b98d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b98d-120">Library</span></span><br/> | <dl> <span data-ttu-id="7b98d-121"><dt>NTDll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b98d-121"><dt>NTDll.lib</dt></span></span> </dl> |
| <span data-ttu-id="7b98d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7b98d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b98d-123"><dt>NTDll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b98d-123"><dt>NTDll.dll</dt></span></span> </dl> |



 

 




