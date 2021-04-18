---
title: Propriedade MyItem. Value
description: Recupera o último valor de amostra do contador.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Propriedade de valor SysMon
- Propriedade de valor SysMon, classe de coitem
- Classe monoitem SysMon, propriedade Value
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749429"
---
# <a name="counteritemvalue-property"></a><span data-ttu-id="da172-106">Propriedade MyItem. Value</span><span class="sxs-lookup"><span data-stu-id="da172-106">CounterItem.Value property</span></span>

<span data-ttu-id="da172-107">Recupera o último valor de amostra do contador.</span><span class="sxs-lookup"><span data-stu-id="da172-107">Retrieves the last sampled value of the counter.</span></span>

<span data-ttu-id="da172-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="da172-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="da172-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da172-109">Syntax</span></span>


```VB
Property Value As Double
```



## <a name="property-value"></a><span data-ttu-id="da172-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="da172-110">Property value</span></span>

<span data-ttu-id="da172-111">Último valor de amostra do contador.</span><span class="sxs-lookup"><span data-stu-id="da172-111">Last sampled value of the counter.</span></span> <span data-ttu-id="da172-112">O valor será-1 se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="da172-112">The value is -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="da172-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="da172-113">Remarks</span></span>

<span data-ttu-id="da172-114">Essa é a propriedade padrão do objeto [**MYITEM**](counteritem.md) .</span><span class="sxs-lookup"><span data-stu-id="da172-114">This is the default property of the [**CounterItem**](counteritem.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="da172-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da172-115">Requirements</span></span>



| <span data-ttu-id="da172-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="da172-116">Requirement</span></span> | <span data-ttu-id="da172-117">Valor</span><span class="sxs-lookup"><span data-stu-id="da172-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da172-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da172-118">Minimum supported client</span></span><br/> | <span data-ttu-id="da172-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da172-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="da172-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da172-120">Minimum supported server</span></span><br/> | <span data-ttu-id="da172-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="da172-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da172-122">DLL</span><span class="sxs-lookup"><span data-stu-id="da172-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da172-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="da172-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da172-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="da172-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da172-125">**Item**</span><span class="sxs-lookup"><span data-stu-id="da172-125">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="da172-126">**MYITEM. GetValue**</span><span class="sxs-lookup"><span data-stu-id="da172-126">**CounterItem.GetValue**</span></span>](counteritem-getvalue.md)
</dt> </dl>

 

 





