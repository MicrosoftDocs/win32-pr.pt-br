---
description: A propriedade CIMType do objeto SWbemProperty é um inteiro que pode ser usado para determinar o tipo CIM dessa propriedade. Esta propriedade é somente para leitura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Propriedade SWbemProperty. CIMType (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921885"
---
# <a name="swbempropertycimtype-property"></a><span data-ttu-id="279af-104">Propriedade SWbemProperty. CIMType</span><span class="sxs-lookup"><span data-stu-id="279af-104">SWbemProperty.CIMType property</span></span>

<span data-ttu-id="279af-105">A propriedade **CIMType** do objeto [**SWbemProperty**](swbemproperty.md) é um inteiro que pode ser usado para determinar o tipo CIM dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="279af-105">The **CIMType** property of the [**SWbemProperty**](swbemproperty.md) object is an integer that can be used to determine the CIM type of this property.</span></span> <span data-ttu-id="279af-106">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="279af-106">This property is read-only.</span></span>

<span data-ttu-id="279af-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="279af-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="279af-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="279af-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="279af-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="279af-109">Syntax</span></span>


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a><span data-ttu-id="279af-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="279af-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="279af-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="279af-111">Remarks</span></span>

<span data-ttu-id="279af-112">Para obter mais informações sobre tipos válidos para essa propriedade, consulte [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="279af-112">For more information about valid types for this property, see [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>

<span data-ttu-id="279af-113">As instâncias de objetos inseridos são armazenadas em objetos compostos como propriedades do tipo **\_ objeto CIM**.</span><span class="sxs-lookup"><span data-stu-id="279af-113">Instances of embedded objects are stored in composite objects as properties of type **CIM\_OBJECT**.</span></span> <span data-ttu-id="279af-114">Para determinar a classe de um objeto incorporado em uma instância de uma classe composta, você deve examinar o qualificador **CIMType** da propriedade tipo de **\_ objeto CIM** .</span><span class="sxs-lookup"><span data-stu-id="279af-114">To determine the class of an embedded object in an instance of a composite class, you must examine the **CIMType** qualifier of the **CIM\_OBJECT** type property.</span></span>

<span data-ttu-id="279af-115">As referências de objeto em uma classe de associação são armazenadas em Propriedades do tipo **\_ referência de CIM**.</span><span class="sxs-lookup"><span data-stu-id="279af-115">The object references in an association class are stored in properties of type **CIM\_REFERENCE**.</span></span> <span data-ttu-id="279af-116">Para determinar os caminhos de objeto reais, você deve examinar o qualificador **CIMType** da Propriedade do tipo de **\_ referência CIM** .</span><span class="sxs-lookup"><span data-stu-id="279af-116">To determine the actual object paths you must examine the **CIMType** qualifier of the **CIM\_REFERENCE** type property.</span></span>

## <a name="requirements"></a><span data-ttu-id="279af-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="279af-117">Requirements</span></span>



| <span data-ttu-id="279af-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="279af-118">Requirement</span></span> | <span data-ttu-id="279af-119">Valor</span><span class="sxs-lookup"><span data-stu-id="279af-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="279af-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="279af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="279af-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="279af-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="279af-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="279af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="279af-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="279af-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="279af-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="279af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="279af-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="279af-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="279af-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="279af-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="279af-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="279af-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="279af-128">DLL</span><span class="sxs-lookup"><span data-stu-id="279af-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="279af-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="279af-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="279af-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="279af-130">CLSID</span></span><br/>                    | <span data-ttu-id="279af-131">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="279af-131">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="279af-132">IID</span><span class="sxs-lookup"><span data-stu-id="279af-132">IID</span></span><br/>                      | <span data-ttu-id="279af-133">ISWbemProperty de IID \_</span><span class="sxs-lookup"><span data-stu-id="279af-133">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




