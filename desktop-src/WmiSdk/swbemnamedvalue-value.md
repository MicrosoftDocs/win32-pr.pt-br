---
description: A propriedade Value do objeto SWbemNamedValue retorna o valor de variante de um item SWbemNamedValue.
ms.assetid: f9609bd2-893a-48c3-9faa-93cd033c4109
ms.tgt_platform: multiple
title: Propriedade SWbemNamedValue. Value (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValue.Value
- ISWbemNamedValue.Value
- ISWbemNamedValue.get_Value
- ISWbemNamedValue.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bf63b15a27c1149341200f29e938bdba6cd7bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091290"
---
# <a name="swbemnamedvaluevalue-property"></a><span data-ttu-id="81ba4-103">Propriedade SWbemNamedValue. Value</span><span class="sxs-lookup"><span data-stu-id="81ba4-103">SWbemNamedValue.Value property</span></span>

<span data-ttu-id="81ba4-104">A propriedade **Value** do objeto [**SWbemNamedValue**](swbemnamedvalue.md) retorna o valor de variante de um item **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="81ba4-104">The **Value** property of the [**SWbemNamedValue**](swbemnamedvalue.md) object returns the variant value of an **SWbemNamedValue** item.</span></span> <span data-ttu-id="81ba4-105">Essa é a propriedade padrão para objetos **SWbemNamedValue** .</span><span class="sxs-lookup"><span data-stu-id="81ba4-105">This is the default property for **SWbemNamedValue** objects.</span></span> <span data-ttu-id="81ba4-106">As alterações feitas na propriedade Value são refletidas automaticamente na coleção [**SWbemNamedValueSet**](swbemnamedvalueset.md) à qual o objeto **SWbemNamedValue** pertence.</span><span class="sxs-lookup"><span data-stu-id="81ba4-106">Changes made to the value property are reflected automatically in the [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection to which the **SWbemNamedValue** object belongs.</span></span>

<span data-ttu-id="81ba4-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="81ba4-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="81ba4-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="81ba4-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81ba4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="81ba4-109">Syntax</span></span>


```VB
SWbemNamedValue.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="81ba4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="81ba4-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="81ba4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81ba4-111">Requirements</span></span>



| <span data-ttu-id="81ba4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ba4-112">Requirement</span></span> | <span data-ttu-id="81ba4-113">Valor</span><span class="sxs-lookup"><span data-stu-id="81ba4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81ba4-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81ba4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="81ba4-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81ba4-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81ba4-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81ba4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="81ba4-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81ba4-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81ba4-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81ba4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="81ba4-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ba4-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81ba4-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="81ba4-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="81ba4-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81ba4-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81ba4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="81ba4-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81ba4-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81ba4-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="81ba4-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="81ba4-124">CLSID</span></span><br/>                    | <span data-ttu-id="81ba4-125">\_SWBEMNAMEDVALUE CLSID</span><span class="sxs-lookup"><span data-stu-id="81ba4-125">CLSID\_SWbemNamedValue</span></span><br/>                                                       |
| <span data-ttu-id="81ba4-126">IID</span><span class="sxs-lookup"><span data-stu-id="81ba4-126">IID</span></span><br/>                      | <span data-ttu-id="81ba4-127">ISWbemNamedValue de IID \_</span><span class="sxs-lookup"><span data-stu-id="81ba4-127">IID\_ISWbemNamedValue</span></span><br/>                                                        |



 

 




