---
description: O método UseFeature do objeto do instalador incrementa a contagem de uso de um recurso específico e retorna o estado de instalação para esse recurso. Esse método deve ser usado para indicar a intenção de um aplicativo usar um recurso.
ms.assetid: c9ea812c-2f95-4ba4-ad8e-b96f7fc14bb1
title: Método Installer. UseFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UseFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 355e7f4e64a5cb69ffc0371473cb0db1ac6313a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747965"
---
# <a name="installerusefeature-method"></a><span data-ttu-id="a7294-104">Método Installer. UseFeature</span><span class="sxs-lookup"><span data-stu-id="a7294-104">Installer.UseFeature method</span></span>

<span data-ttu-id="a7294-105">O método **UseFeature** do objeto do [**instalador**](installer-object.md) incrementa a contagem de uso de um recurso específico e retorna o estado de instalação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="a7294-105">The **UseFeature** method of the [**Installer**](installer-object.md) object increments the usage count for a particular feature and returns the installation state for that feature.</span></span> <span data-ttu-id="a7294-106">Esse método deve ser usado para indicar a intenção de um aplicativo usar um recurso.</span><span class="sxs-lookup"><span data-stu-id="a7294-106">This method should be used to indicate an application's intent to use a feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7294-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7294-107">Syntax</span></span>


```JScript
Installer.UseFeature(
  Product,
  Feature,
  InstallMode
)
```



## <a name="parameters"></a><span data-ttu-id="a7294-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7294-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7294-109">*Product*</span><span class="sxs-lookup"><span data-stu-id="a7294-109">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="a7294-110">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="a7294-110">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="a7294-111">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="a7294-111">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="a7294-112">Identifica o recurso a ser usado.</span><span class="sxs-lookup"><span data-stu-id="a7294-112">Identifies the feature to be used.</span></span>

</dd> <dt>

<span data-ttu-id="a7294-113">*InstallMode*</span><span class="sxs-lookup"><span data-stu-id="a7294-113">*InstallMode*</span></span> 
</dt> <dd>

<span data-ttu-id="a7294-114">Esse parâmetro deve ser *msiInstallModeNoDetection*.</span><span class="sxs-lookup"><span data-stu-id="a7294-114">This parameter must be *msiInstallModeNoDetection*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7294-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7294-115">Return value</span></span>

<span data-ttu-id="a7294-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a7294-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7294-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7294-117">Remarks</span></span>

<span data-ttu-id="a7294-118">O método **UseFeature** só deve ser usado em recursos conhecidos para publicação.</span><span class="sxs-lookup"><span data-stu-id="a7294-118">The **UseFeature** method should only be used on features known to be published.</span></span> <span data-ttu-id="a7294-119">O aplicativo deve determinar o status do recurso chamando a propriedade [**featurestate**](installer-featurestate.md) ou os [**recursos**](installer-features.md) ou seus equivalentes de API.</span><span class="sxs-lookup"><span data-stu-id="a7294-119">The application should determine the status of the feature by calling either the [**FeatureState**](installer-featurestate.md) property or [**Features**](installer-features.md) property or their API equivalents.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7294-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7294-120">Requirements</span></span>



| <span data-ttu-id="a7294-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7294-121">Requirement</span></span> | <span data-ttu-id="a7294-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a7294-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7294-123">Versão</span><span class="sxs-lookup"><span data-stu-id="a7294-123">Version</span></span><br/> | <span data-ttu-id="a7294-124">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a7294-124">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a7294-125">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a7294-125">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a7294-126">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a7294-126">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="a7294-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a7294-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="a7294-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7294-128"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="a7294-129">IID</span><span class="sxs-lookup"><span data-stu-id="a7294-129">IID</span></span><br/>     | <span data-ttu-id="a7294-130">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a7294-130">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="a7294-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7294-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7294-132">**MsiUseFeatureEx**</span><span class="sxs-lookup"><span data-stu-id="a7294-132">**MsiUseFeatureEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msiusefeatureexa)
</dt> </dl>

 

 




