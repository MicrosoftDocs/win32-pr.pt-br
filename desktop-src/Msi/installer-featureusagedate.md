---
description: A propriedade FeatureUsageDate é uma propriedade somente leitura que retorna a data em que o recurso especificado foi usado pela última vez.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Propriedade Installer. FeatureUsageDate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748590"
---
# <a name="installerfeatureusagedate-property"></a><span data-ttu-id="caf8c-103">Propriedade Installer. FeatureUsageDate</span><span class="sxs-lookup"><span data-stu-id="caf8c-103">Installer.FeatureUsageDate property</span></span>

<span data-ttu-id="caf8c-104">A propriedade **FeatureUsageDate** é uma propriedade somente leitura que retorna a data em que o recurso especificado foi usado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="caf8c-104">The **FeatureUsageDate** property is a read-only property that returns the date the specified feature was last used.</span></span>

<span data-ttu-id="caf8c-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="caf8c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="caf8c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caf8c-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a><span data-ttu-id="caf8c-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="caf8c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="caf8c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="caf8c-108">Remarks</span></span>

<span data-ttu-id="caf8c-109">O uso dos métodos [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) ou [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) ou seus equivalentes de API no recurso especificado define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="caf8c-109">Use of the [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) or [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) methods or their API equivalents on the specified feature sets this property.</span></span>

<span data-ttu-id="caf8c-110">A data está no formato de data do MS-DOS, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="caf8c-110">The date is in the MS-DOS date format as shown in the following table.</span></span>



| <span data-ttu-id="caf8c-111">Bits</span><span class="sxs-lookup"><span data-stu-id="caf8c-111">Bits</span></span> | <span data-ttu-id="caf8c-112">Sumário</span><span class="sxs-lookup"><span data-stu-id="caf8c-112">Contents</span></span>                                            |
|------|-----------------------------------------------------|
| <span data-ttu-id="caf8c-113">0-4</span><span class="sxs-lookup"><span data-stu-id="caf8c-113">0-4</span></span>  | <span data-ttu-id="caf8c-114">Dia do mês (1-31)</span><span class="sxs-lookup"><span data-stu-id="caf8c-114">Day of the month (1-31)</span></span>                             |
| <span data-ttu-id="caf8c-115">5-8</span><span class="sxs-lookup"><span data-stu-id="caf8c-115">5-8</span></span>  | <span data-ttu-id="caf8c-116">Mês (1 = Janeiro, 2 = fevereiro e assim por diante)</span><span class="sxs-lookup"><span data-stu-id="caf8c-116">Month (1 = January, 2 = February, and so on)</span></span>        |
| <span data-ttu-id="caf8c-117">9-15</span><span class="sxs-lookup"><span data-stu-id="caf8c-117">9-15</span></span> | <span data-ttu-id="caf8c-118">Deslocamento de ano de 1980 (adicione 1980 para obter o ano real)</span><span class="sxs-lookup"><span data-stu-id="caf8c-118">Year offset from 1980 (add 1980 to get actual year)</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="caf8c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caf8c-119">Requirements</span></span>



| <span data-ttu-id="caf8c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="caf8c-120">Requirement</span></span> | <span data-ttu-id="caf8c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="caf8c-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caf8c-122">Versão</span><span class="sxs-lookup"><span data-stu-id="caf8c-122">Version</span></span><br/> | <span data-ttu-id="caf8c-123">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="caf8c-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="caf8c-124">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="caf8c-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="caf8c-125">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="caf8c-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="caf8c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="caf8c-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="caf8c-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="caf8c-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="caf8c-128">IID</span><span class="sxs-lookup"><span data-stu-id="caf8c-128">IID</span></span><br/>     | <span data-ttu-id="caf8c-129">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="caf8c-129">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="caf8c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="caf8c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caf8c-131">**MsiGetFeatureUsage**</span><span class="sxs-lookup"><span data-stu-id="caf8c-131">**MsiGetFeatureUsage**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




