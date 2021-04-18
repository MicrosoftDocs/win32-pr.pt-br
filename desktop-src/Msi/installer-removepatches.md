---
description: O método RemovePatches remove um ou mais patches para produtos qualificados para receber o patch. O método RemovePatches chama MsiRemovePatches.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Método Installer. RemovePatches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751851"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="8661b-104">Método Installer. RemovePatches</span><span class="sxs-lookup"><span data-stu-id="8661b-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="8661b-105">O método **RemovePatches** remove um ou mais patches para produtos qualificados para receber o patch.</span><span class="sxs-lookup"><span data-stu-id="8661b-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="8661b-106">O método **RemovePatches** chama [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span><span class="sxs-lookup"><span data-stu-id="8661b-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="8661b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8661b-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="8661b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8661b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8661b-109">*PATCHLIST*</span><span class="sxs-lookup"><span data-stu-id="8661b-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="8661b-110">Uma cadeia de caracteres que contém uma lista delimitada por ponto e vírgula de patches a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="8661b-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="8661b-111">Cada patch pode ser representado pelo caminho completo para o pacote de patch ou por GUID de patch.</span><span class="sxs-lookup"><span data-stu-id="8661b-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="8661b-112">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="8661b-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="8661b-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="8661b-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="8661b-114">Uma cadeia de caracteres com o GUID do produto do qual os patches devem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="8661b-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="8661b-115">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="8661b-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="8661b-116">*Desinstaletype*</span><span class="sxs-lookup"><span data-stu-id="8661b-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="8661b-117">Um valor inteiro que especifica o tipo de remoção de patch.</span><span class="sxs-lookup"><span data-stu-id="8661b-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="8661b-118">Esse parâmetro deve ser **msiInstallTypeSingleInstance**.</span><span class="sxs-lookup"><span data-stu-id="8661b-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="8661b-119">*PropertyList*</span><span class="sxs-lookup"><span data-stu-id="8661b-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="8661b-120">Uma cadeia de caracteres que especifica os pares de propriedade = valor a serem incluídos.</span><span class="sxs-lookup"><span data-stu-id="8661b-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="8661b-121">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="8661b-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8661b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8661b-122">Return value</span></span>

<span data-ttu-id="8661b-123">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8661b-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8661b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8661b-124">Remarks</span></span>

<span data-ttu-id="8661b-125">Consulte [desinstalando patches](uninstalling-patches.md) para obter um exemplo que demonstra como um aplicativo pode remover um patch de todos os produtos que estão disponíveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="8661b-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="8661b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8661b-126">Requirements</span></span>



| <span data-ttu-id="8661b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8661b-127">Requirement</span></span> | <span data-ttu-id="8661b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8661b-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8661b-129">Versão</span><span class="sxs-lookup"><span data-stu-id="8661b-129">Version</span></span><br/> | <span data-ttu-id="8661b-130">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8661b-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8661b-131">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8661b-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8661b-132">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8661b-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="8661b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8661b-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="8661b-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8661b-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="8661b-135">IID</span><span class="sxs-lookup"><span data-stu-id="8661b-135">IID</span></span><br/>     | <span data-ttu-id="8661b-136">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8661b-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="8661b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="8661b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8661b-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="8661b-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="8661b-139">**MsiRemovePatches**</span><span class="sxs-lookup"><span data-stu-id="8661b-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="8661b-140">Desinstalando patches</span><span class="sxs-lookup"><span data-stu-id="8661b-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="8661b-141">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="8661b-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




