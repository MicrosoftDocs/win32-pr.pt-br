---
description: Para cada produto listado pelo pacote de patches como qualificado para receber o patch, o método ApplyPatch do objeto do instalador invoca uma instalação e define a propriedade PATCH para o caminho do pacote de patch.
ms.assetid: eee93b6d-f45b-40ae-8e17-cfe6f46b66f4
title: Método Installer. ApplyPatch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyPatch
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc1b7509ddb4c61fa84a4547dcd47f2c7637b913
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751854"
---
# <a name="installerapplypatch-method"></a><span data-ttu-id="e0e8d-103">Método Installer. ApplyPatch</span><span class="sxs-lookup"><span data-stu-id="e0e8d-103">Installer.ApplyPatch method</span></span>

<span data-ttu-id="e0e8d-104">Para cada produto listado pelo pacote de patches como qualificado para receber o patch, o método **ApplyPatch** do objeto do [**instalador**](installer-object.md) invoca uma instalação e define a propriedade [**patch**](patch.md) para o caminho do pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-104">For each product listed by the patch package as eligible to receive the patch, the **ApplyPatch** method of the [**Installer**](installer-object.md) object invokes an installation and sets the [**PATCH**](patch.md) property to the path of the patch package.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0e8d-105">Syntax</span></span>


```JScript
Installer.ApplyPatch(
  PatchPackage,
  InstallPackage,
  InstallType,
  CommandLine
)
```



## <a name="parameters"></a><span data-ttu-id="e0e8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0e8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e8d-107">*PatchPackage*</span><span class="sxs-lookup"><span data-stu-id="e0e8d-107">*PatchPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e8d-108">Especifica um caminho para o pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-108">Specifies a path to the patch package.</span></span>

</dd> <dt>

<span data-ttu-id="e0e8d-109">*InstallPackage*</span><span class="sxs-lookup"><span data-stu-id="e0e8d-109">*InstallPackage*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e8d-110">Se *InstallType* for definido como MsiInstallTypeNetworkImage, *InstallPackage* especificará o caminho para o produto a ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-110">If *InstallType* is set to msiInstallTypeNetworkImage, *InstallPackage* specifies the path to the product that is to be patched.</span></span> <span data-ttu-id="e0e8d-111">Se *InstallType* for definido como MsiInstallTypeDefault e *InstallPackage* for definido como 0, o instalador aplicará o patch a todos os produtos qualificados listados no pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-111">If *InstallType* is set to msiInstallTypeDefault and *InstallPackage* is set to 0, the installer applies the patch to every eligible product listed in the patch package.</span></span>

<span data-ttu-id="e0e8d-112">Se *InstallType* for msiInstallTypeSingleInstance, o instalador aplicará o patch ao produto especificado por *InstallPackage*.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-112">If *InstallType* is msiInstallTypeSingleInstance, the installer applies the patch to the product specified by *InstallPackage*.</span></span> <span data-ttu-id="e0e8d-113">Nesse caso, outros produtos qualificados listados no pacote de patch são ignorados e o parâmetro *InstallPackage* contém a cadeia de caracteres terminada em nulo que representa o código do produto da instância a ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-113">In this case, other eligible products listed in the patch package are ignored and the *InstallPackage* parameter contains the null-terminated string representing the product code of the instance to patch.</span></span> <span data-ttu-id="e0e8d-114">Esse tipo de instalação requer a versão Windows Installer fornecida com o Windows Server 2003 ou posterior ou o Windows Installer XP SP1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-114">This type of installation requires the Windows Installer version shipped with the Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e0e8d-115">*InstallType*</span><span class="sxs-lookup"><span data-stu-id="e0e8d-115">*InstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e8d-116">Esse parâmetro especifica o tipo de instalação a ser corrigido.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-116">This parameter specifies the type of installation to patch.</span></span> <span data-ttu-id="e0e8d-117">O parâmetro *InstallType* será ignorado se *InstallPackage* for omitido.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-117">The *InstallType* parameter is ignored if *InstallPackage* is omitted.</span></span>



| <span data-ttu-id="e0e8d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e8d-118">Value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="e0e8d-119">Significado</span><span class="sxs-lookup"><span data-stu-id="e0e8d-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallTypeNetworkImage"></span><span id="msiinstalltypenetworkimage"></span><span id="MSIINSTALLTYPENETWORKIMAGE"></span><dl> <span data-ttu-id="e0e8d-120"><dt>**msiInstallTypeNetworkImage**</dt></span><span class="sxs-lookup"><span data-stu-id="e0e8d-120"><dt>**msiInstallTypeNetworkImage**</dt></span></span> </dl> | <span data-ttu-id="e0e8d-121">Indica uma instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-121">Indicates a administrative installation.</span></span> <span data-ttu-id="e0e8d-122">Nesse caso, *InstallPackage* deve ser definido como um caminho de pacote.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-122">In this case, *InstallPackage* must be set to a package path.</span></span> <span data-ttu-id="e0e8d-123">Um valor de 1 para msiInstallTypeNetworkImage especifica uma instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-123">A value of 1 for msiInstallTypeNetworkImage specifies a administrative installation.</span></span><br/>                                                                                                                                                                                                                    |
| <span id="msiInstallTypeDefault"></span><span id="msiinstalltypedefault"></span><span id="MSIINSTALLTYPEDEFAULT"></span><dl> <span data-ttu-id="e0e8d-124"><dt>**msiInstallTypeDefault**</dt></span><span class="sxs-lookup"><span data-stu-id="e0e8d-124"><dt>**msiInstallTypeDefault**</dt></span></span> </dl>                     | <span data-ttu-id="e0e8d-125">Pesquisa o sistema para obter os produtos a serem corrigidos.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-125">Searches system for products to patch.</span></span> <span data-ttu-id="e0e8d-126">Nesse caso, *InstallPackage* deve ser uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-126">In this case, *InstallPackage* must be an empty string.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiInstallSingleInstance"></span><span id="msiinstallsingleinstance"></span><span id="MSIINSTALLSINGLEINSTANCE"></span><dl> <span data-ttu-id="e0e8d-127"><dt>**msiInstallSingleInstance**</dt></span><span class="sxs-lookup"><span data-stu-id="e0e8d-127"><dt>**msiInstallSingleInstance**</dt></span></span> </dl>         | <span data-ttu-id="e0e8d-128">Aplicar patch ao produto especificado por *InstallPackage*.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-128">Patch the product specified by *InstallPackage*.</span></span> <span data-ttu-id="e0e8d-129">*InstallPackage* é o código do produto da instância a ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-129">*InstallPackage* is the product code of the instance to patch.</span></span> <span data-ttu-id="e0e8d-130">Esse tipo de instalação requer a versão Windows Installer fornecida com o Windows Server 2003 ou posterior ou Windows Installer XP SP1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-130">This type of installation requires the Windows Installer version shipped with Windows Server 2003 or later or Windows Installer XP SP1 or later.</span></span> <span data-ttu-id="e0e8d-131">Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="e0e8d-131">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0e8d-132">*CommandLine*</span><span class="sxs-lookup"><span data-stu-id="e0e8d-132">*CommandLine*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e8d-133">Especifica as configurações de propriedade que estão sendo definidas na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-133">Specifies property settings being set on the command line.</span></span> <span data-ttu-id="e0e8d-134">Consulte a seção Observações.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-134">See Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e8d-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0e8d-135">Return value</span></span>

<span data-ttu-id="e0e8d-136">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-136">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e8d-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0e8d-137">Remarks</span></span>

<span data-ttu-id="e0e8d-138">Como o delimitador de lista para transformações, origens e patches é um ponto e vírgula, esse caractere não deve ser usado para nomes de arquivo ou caminhos.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-138">Because the list delimiter for transforms, sources, and patches is a semicolon, this character should not be used for file names or paths.</span></span>

<span data-ttu-id="e0e8d-139">A propriedade [**REINSTALL**](reinstall.md) é necessária ao aplicar uma [atualização pequena](small-updates.md) ou um patch de [atualização secundária](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e8d-139">The [**REINSTALL**](reinstall.md) property is required when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="e0e8d-140">Sem essa propriedade, o patch é registrado no sistema, mas não pode atualizar arquivos.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-140">Without this property, the patch is registered on the system but cannot update files.</span></span>

<span data-ttu-id="e0e8d-141">**Windows Installer 2,0:** Você deve definir a propriedade [**REINSTALL**](reinstall.md) na linha de comando ao aplicar uma [atualização pequena](small-updates.md) ou um patch de [atualização secundária](minor-upgrades.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e8d-141">**Windows Installer 2.0:** You must set the [**REINSTALL**](reinstall.md) property on the command line when applying a [small update](small-updates.md) or [minor upgrade](minor-upgrades.md) patch.</span></span> <span data-ttu-id="e0e8d-142">Para patches que não usam um [tipo de ação personalizada 51](custom-action-type-51.md) para definir automaticamente as propriedades **reinstalar** e [**reinstalarmode**](reinstallmode.md) , a propriedade **reinstalar** deve ser explicitamente definida com o parâmetro *CommandLine* .</span><span class="sxs-lookup"><span data-stu-id="e0e8d-142">For patches that do not use a [Custom Action Type 51](custom-action-type-51.md) to automatically set the **REINSTALL** and [**REINSTALLMODE**](reinstallmode.md) properties, the **REINSTALL** property must be explicitly set with the *CommandLine* parameter.</span></span> <span data-ttu-id="e0e8d-143">Defina a propriedade **REINSTALL** para listar os recursos afetados pelo patch ou use uma configuração padrão prática de "REINSTALL = ALL".</span><span class="sxs-lookup"><span data-stu-id="e0e8d-143">Set the **REINSTALL** property to list the features affected by the patch, or use a practical default setting of "REINSTALL=ALL".</span></span> <span data-ttu-id="e0e8d-144">O valor padrão da propriedade **REinstallmode** é "omus".</span><span class="sxs-lookup"><span data-stu-id="e0e8d-144">The default value of the **REINSTALLMODE** property is "omus".</span></span>

<span data-ttu-id="e0e8d-145">**Windows Installer 3,0 e posterior:** A partir do Windows Installer versão 3,0, a propriedade [**REINSTALL**](reinstall.md) é configurada pelo instalador e não precisa ser definida na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-145">**Windows Installer 3.0 and later:** Beginning with Windows Installer version 3.0, the [**REINSTALL**](reinstall.md) property is configured by the installer and does not need to be set on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e8d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e8d-146">Requirements</span></span>



| <span data-ttu-id="e0e8d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e8d-147">Requirement</span></span> | <span data-ttu-id="e0e8d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e8d-148">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e8d-149">Versão</span><span class="sxs-lookup"><span data-stu-id="e0e8d-149">Version</span></span><br/> | <span data-ttu-id="e0e8d-150">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-150">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e0e8d-151">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-151">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e0e8d-152">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e0e8d-152">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="e0e8d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="e0e8d-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0e8d-154"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e8d-154"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="e0e8d-155">IID</span><span class="sxs-lookup"><span data-stu-id="e0e8d-155">IID</span></span><br/>     | <span data-ttu-id="e0e8d-156">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e0e8d-156">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="e0e8d-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0e8d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e8d-158">**MsiApplyPatch**</span><span class="sxs-lookup"><span data-stu-id="e0e8d-158">**MsiApplyPatch**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)
</dt> <dt>

[<span data-ttu-id="e0e8d-159">Sobre propriedades</span><span class="sxs-lookup"><span data-stu-id="e0e8d-159">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="e0e8d-160">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="e0e8d-160">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




