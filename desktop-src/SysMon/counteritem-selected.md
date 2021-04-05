---
title: Propriedade MyItem. Selected
description: Recupera ou define um valor que indica se o contador está selecionado.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Propriedade selecionada SysMon
- Propriedade selecionada SysMon, objeto de coitem
- Objeto monoitem SysMon, propriedade selecionada
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918552"
---
# <a name="counteritemselected-property"></a><span data-ttu-id="8e53e-106">Propriedade MyItem. Selected</span><span class="sxs-lookup"><span data-stu-id="8e53e-106">CounterItem.Selected property</span></span>

<span data-ttu-id="8e53e-107">Recupera ou define um valor que indica se o contador está selecionado.</span><span class="sxs-lookup"><span data-stu-id="8e53e-107">Retrieves or sets a value that indicates if the counter is selected.</span></span>

<span data-ttu-id="8e53e-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8e53e-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e53e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e53e-109">Syntax</span></span>


```VB
Property Selected As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8e53e-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8e53e-110">Property value</span></span>

<span data-ttu-id="8e53e-111">True se o contador for selecionado; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="8e53e-111">True if the counter is selected; otherwise, false.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e53e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e53e-112">Remarks</span></span>

<span data-ttu-id="8e53e-113">Você pode selecionar um ou mais contadores da coleção de contadores.</span><span class="sxs-lookup"><span data-stu-id="8e53e-113">You can select one or more counters from the collection of counters.</span></span> <span data-ttu-id="8e53e-114">Selecionar um contador, seleciona o contador na legenda, torna o contador visível na legenda e gera um evento [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .</span><span class="sxs-lookup"><span data-stu-id="8e53e-114">Selecting a counter, selects the counter in the Legend, makes the counter visible in the Legend, and generates an [**OnCounterSelected**](-systemmonitor-oncounterselected.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e53e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e53e-115">Requirements</span></span>



| <span data-ttu-id="8e53e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e53e-116">Requirement</span></span> | <span data-ttu-id="8e53e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8e53e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e53e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e53e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8e53e-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e53e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e53e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e53e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8e53e-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e53e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e53e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8e53e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e53e-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="8e53e-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e53e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e53e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e53e-125">**Item**</span><span class="sxs-lookup"><span data-stu-id="8e53e-125">**CounterItem**</span></span>](counteritem.md)
</dt> </dl>

 

 





