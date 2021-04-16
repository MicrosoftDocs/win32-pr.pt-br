---
description: O método ApplyMultiplePatches aplica um ou mais patches aos produtos qualificados para receber o patch. O método define a propriedade PATCH.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Método Installer. ApplyMultiplePatches
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750003"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="5b210-104">Método Installer. ApplyMultiplePatches</span><span class="sxs-lookup"><span data-stu-id="5b210-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="5b210-105">O método **ApplyMultiplePatches** aplica um ou mais patches aos produtos qualificados para receber o patch.</span><span class="sxs-lookup"><span data-stu-id="5b210-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="5b210-106">O método define a propriedade [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="5b210-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b210-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b210-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="5b210-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b210-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b210-109">*PatchPackagesList*</span><span class="sxs-lookup"><span data-stu-id="5b210-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="5b210-110">Uma cadeia de caracteres que contém uma lista delimitada por ponto-e-vírgula dos caminhos para arquivos de patch.</span><span class="sxs-lookup"><span data-stu-id="5b210-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="5b210-111">Por exemplo: "" c: \\ SUS \\ download de \\ cache \\ Office \\ SP1. msp; c: \\ SUS \\ baixar o \\ cache \\ Office \\ QFE1. msp; c: \\ SUS \\ Download \\ cache \\ Office \\ QFEn. msp ""</span><span class="sxs-lookup"><span data-stu-id="5b210-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="5b210-112">*Product*</span><span class="sxs-lookup"><span data-stu-id="5b210-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="5b210-113">Esse parâmetro fornece o [**ProductCode**](productcode.md) do produto que está sendo corrigido.</span><span class="sxs-lookup"><span data-stu-id="5b210-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="5b210-114">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5b210-114">This parameter is optional.</span></span> <span data-ttu-id="5b210-115">Quando esse parâmetro é nulo, os patches são aplicados a todos os produtos qualificados para receber esses patches.</span><span class="sxs-lookup"><span data-stu-id="5b210-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="5b210-116">*szPropertiesList*</span><span class="sxs-lookup"><span data-stu-id="5b210-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="5b210-117">Uma cadeia de caracteres terminada em nulo que especifica as configurações de propriedade de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="5b210-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="5b210-118">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="5b210-118">This parameter is optional.</span></span> <span data-ttu-id="5b210-119">Consulte [sobre propriedades](about-properties.md) e [definindo valores de propriedade pública na linha de comando](setting-public-property-values-on-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="5b210-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="5b210-120">Essas propriedades são compartilhadas por todos os produtos de destino.</span><span class="sxs-lookup"><span data-stu-id="5b210-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b210-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b210-121">Return value</span></span>

<span data-ttu-id="5b210-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5b210-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b210-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b210-123">Requirements</span></span>



| <span data-ttu-id="5b210-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b210-124">Requirement</span></span> | <span data-ttu-id="5b210-125">Valor</span><span class="sxs-lookup"><span data-stu-id="5b210-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b210-126">Versão</span><span class="sxs-lookup"><span data-stu-id="5b210-126">Version</span></span><br/> | <span data-ttu-id="5b210-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b210-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5b210-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5b210-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5b210-129">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b210-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="5b210-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5b210-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="5b210-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b210-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="5b210-132">IID</span><span class="sxs-lookup"><span data-stu-id="5b210-132">IID</span></span><br/>     | <span data-ttu-id="5b210-133">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5b210-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="5b210-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b210-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b210-135">Sobre propriedades</span><span class="sxs-lookup"><span data-stu-id="5b210-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="5b210-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="5b210-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="5b210-137">**DISTRIBUÍDO**</span><span class="sxs-lookup"><span data-stu-id="5b210-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="5b210-138">Definindo valores de propriedade pública na linha de comando</span><span class="sxs-lookup"><span data-stu-id="5b210-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="5b210-139">**MsiApplyMultiplePatches**</span><span class="sxs-lookup"><span data-stu-id="5b210-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="5b210-140">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="5b210-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




