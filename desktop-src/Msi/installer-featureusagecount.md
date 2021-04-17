---
description: A propriedade FeatureUsageCount é uma propriedade somente leitura que retorna o número de vezes que o recurso foi usado.
ms.assetid: 70171e22-d73a-4718-a360-df9d1722761b
title: Propriedade Installer. FeatureUsageCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageCount
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fbacb6b6fd5dc4d31d7c727d719e1253969c0d43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748980"
---
# <a name="installerfeatureusagecount-property"></a><span data-ttu-id="03d6a-103">Propriedade Installer. FeatureUsageCount</span><span class="sxs-lookup"><span data-stu-id="03d6a-103">Installer.FeatureUsageCount property</span></span>

<span data-ttu-id="03d6a-104">A propriedade **FeatureUsageCount** é uma propriedade somente leitura que retorna o número de vezes que o recurso foi usado.</span><span class="sxs-lookup"><span data-stu-id="03d6a-104">The **FeatureUsageCount** property is a read-only property that returns the number of times the feature has been used.</span></span>

<span data-ttu-id="03d6a-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="03d6a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d6a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03d6a-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageCount
```



## <a name="property-value"></a><span data-ttu-id="03d6a-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="03d6a-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="03d6a-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="03d6a-108">Remarks</span></span>

<span data-ttu-id="03d6a-109">O uso dos métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou seus equivalentes de API no recurso especificado incrementa essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="03d6a-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature increments this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d6a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03d6a-110">Requirements</span></span>



| <span data-ttu-id="03d6a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d6a-111">Requirement</span></span> | <span data-ttu-id="03d6a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="03d6a-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d6a-113">Versão</span><span class="sxs-lookup"><span data-stu-id="03d6a-113">Version</span></span><br/> | <span data-ttu-id="03d6a-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="03d6a-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="03d6a-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="03d6a-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="03d6a-116">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="03d6a-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="03d6a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="03d6a-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="03d6a-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d6a-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="03d6a-119">IID</span><span class="sxs-lookup"><span data-stu-id="03d6a-119">IID</span></span><br/>     | <span data-ttu-id="03d6a-120">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="03d6a-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="03d6a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="03d6a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d6a-122">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="03d6a-122">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




