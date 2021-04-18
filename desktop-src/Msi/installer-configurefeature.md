---
description: O método ConfigureFeature do objeto do instalador configura o estado instalado de um recurso do produto.
ms.assetid: cc950951-3b43-4d86-9ff1-80aa2ccd11d5
title: Installer.Configmétodo ureFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 737019f5c404beabef404751e617be975b946c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751650"
---
# <a name="installerconfigurefeature-method"></a><span data-ttu-id="0e0f6-103">Installer.Configmétodo ureFeature</span><span class="sxs-lookup"><span data-stu-id="0e0f6-103">Installer.ConfigureFeature method</span></span>

<span data-ttu-id="0e0f6-104">O método **ConfigureFeature** do objeto do [**instalador**](installer-object.md) configura o estado instalado de um recurso do produto.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-104">The **ConfigureFeature** method of the [**Installer**](installer-object.md) object configures the installed state of a product feature.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e0f6-105">Syntax</span></span>


```JScript
Installer.ConfigureFeature(
  Product,
  Feature,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="0e0f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e0f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e0f6-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="0e0f6-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="0e0f6-108">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="0e0f6-109">*Recurso*</span><span class="sxs-lookup"><span data-stu-id="0e0f6-109">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="0e0f6-110">Especifica a ID do recurso a ser configurado.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-110">Specifies the feature ID of the feature to be configured.</span></span>

</dd> <dt>

<span data-ttu-id="0e0f6-111">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="0e0f6-111">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="0e0f6-112">Especifica o estado de instalação para o recurso.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-112">Specifies the installation state for the feature.</span></span> <span data-ttu-id="0e0f6-113">Esse parâmetro deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-113">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="0e0f6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0e0f6-114">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="0e0f6-115">Significado</span><span class="sxs-lookup"><span data-stu-id="0e0f6-115">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="0e0f6-116"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="0e0f6-116"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="0e0f6-117">O recurso é anunciado</span><span class="sxs-lookup"><span data-stu-id="0e0f6-117">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="0e0f6-118"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="0e0f6-118"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="0e0f6-119">O recurso é instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-119">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="0e0f6-120"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="0e0f6-120"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="0e0f6-121">O recurso é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-121">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="0e0f6-122"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="0e0f6-122"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="0e0f6-123">O recurso é instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-123">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="0e0f6-124"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="0e0f6-124"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="0e0f6-125">O recurso é instalado em seu local padrão.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-125">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e0f6-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e0f6-126">Return value</span></span>

<span data-ttu-id="0e0f6-127">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e0f6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e0f6-128">Requirements</span></span>



| <span data-ttu-id="0e0f6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e0f6-129">Requirement</span></span> | <span data-ttu-id="0e0f6-130">Valor</span><span class="sxs-lookup"><span data-stu-id="0e0f6-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0f6-131">Versão</span><span class="sxs-lookup"><span data-stu-id="0e0f6-131">Version</span></span><br/> | <span data-ttu-id="0e0f6-132">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0e0f6-133">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e0f6-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0e0f6-134">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e0f6-134">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0e0f6-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0e0f6-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e0f6-136"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e0f6-136"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0e0f6-137">IID</span><span class="sxs-lookup"><span data-stu-id="0e0f6-137">IID</span></span><br/>     | <span data-ttu-id="0e0f6-138">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0e0f6-138">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0e0f6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e0f6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0f6-140">**MsiConfigureFeature**</span><span class="sxs-lookup"><span data-stu-id="0e0f6-140">**MsiConfigureFeature**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea)
</dt> <dt>

[<span data-ttu-id="0e0f6-141">Funções de instalação e configuração</span><span class="sxs-lookup"><span data-stu-id="0e0f6-141">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




