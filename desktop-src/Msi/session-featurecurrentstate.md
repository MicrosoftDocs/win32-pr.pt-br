---
description: A propriedade FeatureCurrentState do objeto Session é uma propriedade somente leitura que retorna o estado atual instalado do recurso designado. Para valores de estado, consulte a propriedade FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Propriedade Session. FeatureCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787067"
---
# <a name="sessionfeaturecurrentstate-property"></a><span data-ttu-id="2c874-104">Propriedade Session. FeatureCurrentState</span><span class="sxs-lookup"><span data-stu-id="2c874-104">Session.FeatureCurrentState property</span></span>

<span data-ttu-id="2c874-105">A propriedade **FeatureCurrentState** do objeto [**Session**](session-object.md) é uma propriedade somente leitura que retorna o estado atual instalado do recurso designado.</span><span class="sxs-lookup"><span data-stu-id="2c874-105">The **FeatureCurrentState** property of the [**Session**](session-object.md) object is a read-only property that returns the current installed state of the designated feature.</span></span> <span data-ttu-id="2c874-106">Para valores de estado, consulte a propriedade [**FeatureRequestState**](session-featurerequeststate.md) .</span><span class="sxs-lookup"><span data-stu-id="2c874-106">For state values, see the [**FeatureRequestState**](session-featurerequeststate.md) property.</span></span>

<span data-ttu-id="2c874-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="2c874-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c874-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c874-108">Syntax</span></span>


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a><span data-ttu-id="2c874-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="2c874-109">Property value</span></span>

<span data-ttu-id="2c874-110">Nome de cadeia de caracteres necessário do recurso solicitado e uma chave primária na [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2c874-110">Required string name of the requested feature, and a primary key into the [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c874-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c874-111">Remarks</span></span>

<span data-ttu-id="2c874-112">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="2c874-112">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c874-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c874-113">Requirements</span></span>



| <span data-ttu-id="2c874-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c874-114">Requirement</span></span> | <span data-ttu-id="2c874-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2c874-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c874-116">Versão</span><span class="sxs-lookup"><span data-stu-id="2c874-116">Version</span></span><br/> | <span data-ttu-id="2c874-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c874-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2c874-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2c874-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2c874-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c874-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="2c874-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2c874-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2c874-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c874-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="2c874-122">IID</span><span class="sxs-lookup"><span data-stu-id="2c874-122">IID</span></span><br/>     | <span data-ttu-id="2c874-123">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="2c874-123">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="2c874-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c874-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c874-125">**Session**</span><span class="sxs-lookup"><span data-stu-id="2c874-125">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="2c874-126">**Propriedade FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="2c874-126">**FeatureRequestState property**</span></span>](session-featurerequeststate.md)
</dt> </dl>

 

 




