---
description: A propriedade Patchproperty Obtém informações sobre um patch específico aplicado a uma instância específica do produto. Essa propriedade chama MsiGetPatchInfoEx.
ms.assetid: c58897de-c30b-4269-9926-040613052616
title: Método patch. Patchproperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.PatchProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2ffabcfbfd7e8e97bef97e4e04fbe95fc720eea1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748145"
---
# <a name="patchpatchproperty-method"></a><span data-ttu-id="b5441-104">Método patch. Patchproperty</span><span class="sxs-lookup"><span data-stu-id="b5441-104">Patch.PatchProperty method</span></span>

<span data-ttu-id="b5441-105">A propriedade **patchproperty** Obtém informações sobre um patch específico aplicado a uma instância específica do produto.</span><span class="sxs-lookup"><span data-stu-id="b5441-105">The **PatchProperty** property gets information about a specific patch applied to a specific instance of the product.</span></span> <span data-ttu-id="b5441-106">Essa propriedade chama [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span><span class="sxs-lookup"><span data-stu-id="b5441-106">This property calls [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5441-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5441-107">Syntax</span></span>


```JScript
Patch.PatchProperty(
  szProperty
)
```



## <a name="parameters"></a><span data-ttu-id="b5441-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5441-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5441-109">*szProperty*</span><span class="sxs-lookup"><span data-stu-id="b5441-109">*szProperty*</span></span> 
</dt> <dd>

<span data-ttu-id="b5441-110">O parâmetro *szProperty* pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5441-110">The *szProperty* parameter can be one of the following values.</span></span>



| <span data-ttu-id="b5441-111">Nome</span><span class="sxs-lookup"><span data-stu-id="b5441-111">Name</span></span>          | <span data-ttu-id="b5441-112">Significado</span><span class="sxs-lookup"><span data-stu-id="b5441-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5441-113">LocalPackage</span><span class="sxs-lookup"><span data-stu-id="b5441-113">LocalPackage</span></span>  | <span data-ttu-id="b5441-114">Obtenha o arquivo de patch armazenado em cache usado pelo produto.</span><span class="sxs-lookup"><span data-stu-id="b5441-114">Get the cached patch file used by the product.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="b5441-115">Transformações</span><span class="sxs-lookup"><span data-stu-id="b5441-115">Transforms</span></span>    | <span data-ttu-id="b5441-116">Obtenha o conjunto de transformações de patch aplicadas ao produto pela última instalação do patch.</span><span class="sxs-lookup"><span data-stu-id="b5441-116">Get the set of patch transforms applied to the product by the last patch installation.</span></span> <span data-ttu-id="b5441-117">Esse valor pode não estar disponível para aplicativos não gerenciados por usuário se o usuário não estiver conectado ao computador.</span><span class="sxs-lookup"><span data-stu-id="b5441-117">This value may not be available for per-user-unmanaged applications if the user is not logged in to the computer.</span></span>                                                                                                                     |
| <span data-ttu-id="b5441-118">InstallDate</span><span class="sxs-lookup"><span data-stu-id="b5441-118">InstallDate</span></span>   | <span data-ttu-id="b5441-119">Obtenha a data em que o patch foi aplicado ao produto.</span><span class="sxs-lookup"><span data-stu-id="b5441-119">Get the date when the patch was applied to the product.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b5441-120">Desinstalado</span><span class="sxs-lookup"><span data-stu-id="b5441-120">Uninstallable</span></span> | <span data-ttu-id="b5441-121">Retorna "1" se o patch for marcado como possível para ser desinstalado do produto.</span><span class="sxs-lookup"><span data-stu-id="b5441-121">Returns "1" if the patch is marked as possible to uninstall from the product.</span></span> <span data-ttu-id="b5441-122">Nesse caso, o instalador ainda poderá bloquear a desinstalação se esse patch for exigido por outro patch que não pode ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b5441-122">In this case, the installer can still block the uninstallation if this patch is required by another patch that cannot be uninstalled.</span></span>                                                                                                          |
| <span data-ttu-id="b5441-123">Estado</span><span class="sxs-lookup"><span data-stu-id="b5441-123">State</span></span>         | <span data-ttu-id="b5441-124">Retorna "1" se esse patch estiver aplicado no momento ao produto.</span><span class="sxs-lookup"><span data-stu-id="b5441-124">Returns "1" if this patch is currently applied to the product.</span></span> <span data-ttu-id="b5441-125">Retorna "2" se esse patch tiver sido substituído por outro patch.</span><span class="sxs-lookup"><span data-stu-id="b5441-125">Returns "2" if this patch has been superseded by another patch.</span></span> <span data-ttu-id="b5441-126">Retorna "4" se esse patch tiver sido tornado obsoleto por outro patch.</span><span class="sxs-lookup"><span data-stu-id="b5441-126">Returns "4" if this patch has been made obsolete by another patch.</span></span> <span data-ttu-id="b5441-127">Esses valores correspondem às constantes usadas pelo parâmetro *dwFilter* de [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span><span class="sxs-lookup"><span data-stu-id="b5441-127">These values correspond to the constants used by the *dwFilter* parameter of [**MsiEnumPatchesEx**](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa).</span></span> |
| <span data-ttu-id="b5441-128">DisplayName</span><span class="sxs-lookup"><span data-stu-id="b5441-128">DisplayName</span></span>   | <span data-ttu-id="b5441-129">Obtenha o nome de exibição registrado para o patch.</span><span class="sxs-lookup"><span data-stu-id="b5441-129">Get the registered display name for the patch.</span></span> <span data-ttu-id="b5441-130">Para patches que não incluem a propriedade DisplayName na tabela [MsiPatchMetaData](msipatchmetadata-table.md) , o nome de exibição retornado é uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="b5441-130">For patches that do not include the DisplayName property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned display name is an empty string ("").</span></span>                                                                                                      |
| <span data-ttu-id="b5441-131">MoreInfoURL</span><span class="sxs-lookup"><span data-stu-id="b5441-131">MoreInfoURL</span></span>   | <span data-ttu-id="b5441-132">Obtenha a URL de informações de suporte registradas para o patch.</span><span class="sxs-lookup"><span data-stu-id="b5441-132">Get the registered support information URL for the patch.</span></span> <span data-ttu-id="b5441-133">Para patches que não incluem a propriedade MoreInfoURL na tabela [MsiPatchMetaData](msipatchmetadata-table.md) , a URL de informações de suporte retornada é uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="b5441-133">For patches that do not include the MoreInfoURL property in the [MsiPatchMetadata](msipatchmetadata-table.md) table, the returned support information URL is an empty string ("").</span></span>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5441-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5441-134">Return value</span></span>

<span data-ttu-id="b5441-135">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b5441-135">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5441-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5441-136">Remarks</span></span>

<span data-ttu-id="b5441-137">Esse método pode retornar \_ um patch desconhecido de erro \_ , se o objeto [**patch**](patch-object.md) for inicializado com uma cadeia de caracteres vazia para *ProductCode*.</span><span class="sxs-lookup"><span data-stu-id="b5441-137">This method can return ERROR\_UNKNOWN\_PATCH, if the [**Patch**](patch-object.md) object is initialized with an empty string for *ProductCode*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5441-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5441-138">Requirements</span></span>



| <span data-ttu-id="b5441-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5441-139">Requirement</span></span> | <span data-ttu-id="b5441-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b5441-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5441-141">Versão</span><span class="sxs-lookup"><span data-stu-id="b5441-141">Version</span></span><br/> | <span data-ttu-id="b5441-142">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b5441-142">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b5441-143">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b5441-143">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b5441-144">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b5441-144">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b5441-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b5441-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="b5441-146"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5441-146"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b5441-147">IID</span><span class="sxs-lookup"><span data-stu-id="b5441-147">IID</span></span><br/>     | <span data-ttu-id="b5441-148">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b5441-148">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="b5441-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5441-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5441-150">**Patch**</span><span class="sxs-lookup"><span data-stu-id="b5441-150">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="b5441-151">**MsiEnumPatchesEx**</span><span class="sxs-lookup"><span data-stu-id="b5441-151">**MsiEnumPatchesEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumpatchesexa)
</dt> <dt>

[<span data-ttu-id="b5441-152">**MsiGetPatchInfoEx**</span><span class="sxs-lookup"><span data-stu-id="b5441-152">**MsiGetPatchInfoEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[<span data-ttu-id="b5441-153">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="b5441-153">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




