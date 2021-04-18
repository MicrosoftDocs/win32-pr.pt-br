---
description: O método ConfigureProduct do objeto do instalador instala ou desinstala um produto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Installer.Configmétodo ureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749792"
---
# <a name="installerconfigureproduct-method"></a><span data-ttu-id="15c48-103">Installer.Configmétodo ureProduct</span><span class="sxs-lookup"><span data-stu-id="15c48-103">Installer.ConfigureProduct method</span></span>

<span data-ttu-id="15c48-104">O método **ConfigureProduct** do objeto do [**instalador**](installer-object.md) instala ou desinstala um produto.</span><span class="sxs-lookup"><span data-stu-id="15c48-104">The **ConfigureProduct** method of the [**Installer**](installer-object.md) object installs or uninstalls a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c48-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15c48-105">Syntax</span></span>


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a><span data-ttu-id="15c48-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15c48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c48-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="15c48-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="15c48-108">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="15c48-108">Specifies the product code of the product.</span></span>

</dd> <dt>

<span data-ttu-id="15c48-109">*InstallLevel*</span><span class="sxs-lookup"><span data-stu-id="15c48-109">*InstallLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="15c48-110">Especifica a configuração de instalação padrão do produto.</span><span class="sxs-lookup"><span data-stu-id="15c48-110">Specifies the default installation configuration of the product.</span></span> <span data-ttu-id="15c48-111">O parâmetro InstallLevel será ignorado e todos os recursos serão instalados se o parâmetro InstallState for definido como qualquer outro valor que msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="15c48-111">The InstallLevel parameter is ignored and all features are installed if the InstallState parameter is set to any other value than msiInstallStateDefault.</span></span>

<span data-ttu-id="15c48-112">Esse parâmetro deve ser 0 (instalar usando níveis de recurso criados), 65535 (instalar todos os recursos) ou um valor entre 0 e 65535 para instalar um subconjunto de recursos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="15c48-112">This parameter must be either 0 (install using authored feature levels), 65535 (install all features), or a value between 0 and 65535 to install a subset of available features.</span></span>

</dd> <dt>

<span data-ttu-id="15c48-113">*InstallState*</span><span class="sxs-lookup"><span data-stu-id="15c48-113">*InstallState*</span></span> 
</dt> <dd>

<span data-ttu-id="15c48-114">Especifica o estado de instalação para o recurso.</span><span class="sxs-lookup"><span data-stu-id="15c48-114">Specifies the installation state for the feature.</span></span> <span data-ttu-id="15c48-115">Esse parâmetro deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="15c48-115">This parameter must be one of the following values.</span></span>



| <span data-ttu-id="15c48-116">Valor</span><span class="sxs-lookup"><span data-stu-id="15c48-116">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="15c48-117">Significado</span><span class="sxs-lookup"><span data-stu-id="15c48-117">Meaning</span></span>                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <span data-ttu-id="15c48-118"><dt>**msiInstallStateAdvertised**</dt></span><span class="sxs-lookup"><span data-stu-id="15c48-118"><dt>**msiInstallStateAdvertised**</dt></span></span> </dl> | <span data-ttu-id="15c48-119">O recurso é anunciado</span><span class="sxs-lookup"><span data-stu-id="15c48-119">The feature is advertised</span></span><br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <span data-ttu-id="15c48-120"><dt>**msiInstallStateLocal**</dt></span><span class="sxs-lookup"><span data-stu-id="15c48-120"><dt>**msiInstallStateLocal**</dt></span></span> </dl>                     | <span data-ttu-id="15c48-121">O recurso é instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="15c48-121">The feature is installed locally.</span></span><br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <span data-ttu-id="15c48-122"><dt>**msiInstallStateAbsent**</dt></span><span class="sxs-lookup"><span data-stu-id="15c48-122"><dt>**msiInstallStateAbsent**</dt></span></span> </dl>                 | <span data-ttu-id="15c48-123">O recurso é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="15c48-123">The feature is uninstalled.</span></span><br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <span data-ttu-id="15c48-124"><dt>**msiInstallStateSource**</dt></span><span class="sxs-lookup"><span data-stu-id="15c48-124"><dt>**msiInstallStateSource**</dt></span></span> </dl>                 | <span data-ttu-id="15c48-125">O recurso é instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="15c48-125">The feature is installed to run from source.</span></span><br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <span data-ttu-id="15c48-126"><dt>**msiInstallStateDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="15c48-126"><dt>**msiInstallStateDefault**</dt></span></span> </dl>             | <span data-ttu-id="15c48-127">O recurso é instalado em seu local padrão.</span><span class="sxs-lookup"><span data-stu-id="15c48-127">The feature is installed to its default location.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c48-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15c48-128">Return value</span></span>

<span data-ttu-id="15c48-129">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="15c48-129">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15c48-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="15c48-130">Remarks</span></span>

<span data-ttu-id="15c48-131">O método **ConfigureProduct** exibe a interface do usuário usando as configurações atuais.</span><span class="sxs-lookup"><span data-stu-id="15c48-131">The **ConfigureProduct** method displays the user interface using current settings.</span></span> <span data-ttu-id="15c48-132">As configurações de interface do usuário podem ser alteradas modificando a [**Propriedade UILevel (objeto do instalador)**](installer-uilevel.md) antes de chamar o método **ConfigureProduct** .</span><span class="sxs-lookup"><span data-stu-id="15c48-132">User interface settings can be changed by modifying the [**UILevel property (Installer object)**](installer-uilevel.md) before calling the **ConfigureProduct** method.</span></span>

<span data-ttu-id="15c48-133">Se o parâmetro *InstallState* for definido como qualquer outro valor diferente de msiInstallStateDefault, o parâmetro *InstallLevel* será ignorado e todos os recursos do produto serão instalados.</span><span class="sxs-lookup"><span data-stu-id="15c48-133">If the *InstallState* parameter is set to any other value than msiInstallStateDefault, the *InstallLevel* parameter is ignored and all features of the product are installed.</span></span> <span data-ttu-id="15c48-134">Use o método [**ConfigureFeature**](installer-configurefeature.md) para controlar a instalação de recursos individuais quando o parâmetro *InstallState* não estiver definido como msiInstallStateDefault.</span><span class="sxs-lookup"><span data-stu-id="15c48-134">Use the [**ConfigureFeature**](installer-configurefeature.md) method to control the installation of individual features when the *InstallState* parameter is not set to msiInstallStateDefault.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c48-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15c48-135">Requirements</span></span>



| <span data-ttu-id="15c48-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c48-136">Requirement</span></span> | <span data-ttu-id="15c48-137">Valor</span><span class="sxs-lookup"><span data-stu-id="15c48-137">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c48-138">Versão</span><span class="sxs-lookup"><span data-stu-id="15c48-138">Version</span></span><br/> | <span data-ttu-id="15c48-139">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="15c48-139">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="15c48-140">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="15c48-140">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="15c48-141">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="15c48-141">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="15c48-142">DLL</span><span class="sxs-lookup"><span data-stu-id="15c48-142">DLL</span></span><br/>     | <dl> <span data-ttu-id="15c48-143"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15c48-143"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="15c48-144">IID</span><span class="sxs-lookup"><span data-stu-id="15c48-144">IID</span></span><br/>     | <span data-ttu-id="15c48-145">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="15c48-145">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="15c48-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="15c48-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c48-147">**MsiConfigureProduct**</span><span class="sxs-lookup"><span data-stu-id="15c48-147">**MsiConfigureProduct**</span></span>](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[<span data-ttu-id="15c48-148">Funções de instalação e configuração</span><span class="sxs-lookup"><span data-stu-id="15c48-148">Installation and Configuration Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




