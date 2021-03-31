---
description: A propriedade origin do objeto SWbemProperty recupera o nome da classe WMI na qual essa propriedade foi introduzida. Para classes com hierarquias de herança profundas, geralmente é desejável saber quais propriedades foram declaradas em quais classes.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propriedade SWbemProperty. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169805"
---
# <a name="swbempropertyorigin-property"></a><span data-ttu-id="3fe55-104">Propriedade SWbemProperty. Origin</span><span class="sxs-lookup"><span data-stu-id="3fe55-104">SWbemProperty.Origin property</span></span>

<span data-ttu-id="3fe55-105">A propriedade **Origin** do objeto [**SWbemProperty**](swbemproperty.md) recupera o nome da classe WMI na qual essa propriedade foi introduzida.</span><span class="sxs-lookup"><span data-stu-id="3fe55-105">The **Origin** property of the [**SWbemProperty**](swbemproperty.md) object retrieves the name of the WMI class in which this property was introduced.</span></span> <span data-ttu-id="3fe55-106">Para classes com hierarquias de herança profundas, geralmente é desejável saber quais propriedades foram declaradas em quais classes.</span><span class="sxs-lookup"><span data-stu-id="3fe55-106">For classes with deep inheritance hierarchies, it is often desirable to know which properties were declared in which classes.</span></span>

<span data-ttu-id="3fe55-107">Se a propriedade for local (consulte [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)), esse valor será o mesmo que a classe proprietária.</span><span class="sxs-lookup"><span data-stu-id="3fe55-107">If the property is local (see [**SWbemQualifier.IsLocal**](swbemqualifier-islocal.md)), this value is the same as the owning class.</span></span> <span data-ttu-id="3fe55-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3fe55-108">This property is read-only.</span></span>

<span data-ttu-id="3fe55-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3fe55-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3fe55-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3fe55-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fe55-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fe55-111">Syntax</span></span>


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a><span data-ttu-id="3fe55-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3fe55-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="3fe55-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fe55-113">Requirements</span></span>



| <span data-ttu-id="3fe55-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fe55-114">Requirement</span></span> | <span data-ttu-id="3fe55-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3fe55-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fe55-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fe55-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3fe55-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fe55-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fe55-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fe55-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3fe55-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fe55-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fe55-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fe55-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fe55-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fe55-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fe55-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3fe55-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3fe55-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3fe55-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3fe55-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3fe55-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fe55-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fe55-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3fe55-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="3fe55-126">CLSID</span></span><br/>                    | <span data-ttu-id="3fe55-127">\_SWBEMPROPERTY CLSID</span><span class="sxs-lookup"><span data-stu-id="3fe55-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="3fe55-128">IID</span><span class="sxs-lookup"><span data-stu-id="3fe55-128">IID</span></span><br/>                      | <span data-ttu-id="3fe55-129">ISWbemProperty de IID \_</span><span class="sxs-lookup"><span data-stu-id="3fe55-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




