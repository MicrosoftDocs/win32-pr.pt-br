---
description: O método SourceListAddMediaDisk adiciona um disco ao conjunto de discos registrados. Aceita DiskId, VolumeLabel e DiskPrompt como parâmetros. Esse método chama em MsiSourceListAddMediaDisk.
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Método Product. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2f81b21570d708f361e45be7f6f42a93fd0d335
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747325"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="dd1db-105">Método Product. SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="dd1db-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="dd1db-106">O método **SourceListAddMediaDisk** adiciona um disco ao conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="dd1db-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="dd1db-107">Aceita *DiskId*, *VolumeLabel* e *DiskPrompt* como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dd1db-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="dd1db-108">Esse método chama em [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="dd1db-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1db-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd1db-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="dd1db-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd1db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1db-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="dd1db-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1db-112">Esse parâmetro fornece a ID do disco que está sendo adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="dd1db-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="dd1db-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="dd1db-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1db-114">Esse parâmetro fornece o rótulo do disco que está sendo adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="dd1db-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="dd1db-115">Uma atualização substitui o rótulo de volume existente no registro.</span><span class="sxs-lookup"><span data-stu-id="dd1db-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="dd1db-116">Para alterar apenas a solicitação de disco, obtenha o rótulo de volume registrado existente e forneça-o junto com o novo prompt de disco.</span><span class="sxs-lookup"><span data-stu-id="dd1db-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="dd1db-117">Uma cadeia de caracteres vazia para esse parâmetro registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o rótulo do volume.</span><span class="sxs-lookup"><span data-stu-id="dd1db-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="dd1db-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="dd1db-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1db-119">Esse parâmetro fornece o prompt de disco do disco que está sendo adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="dd1db-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="dd1db-120">Uma atualização substitui o prompt de disco existente no registro.</span><span class="sxs-lookup"><span data-stu-id="dd1db-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="dd1db-121">Para alterar apenas o rótulo do volume, obtenha o prompt de disco existente do registro e forneça o novo rótulo de volume.</span><span class="sxs-lookup"><span data-stu-id="dd1db-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="dd1db-122">Uma cadeia de caracteres vazia para esse parâmetro registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o prompt de disco.</span><span class="sxs-lookup"><span data-stu-id="dd1db-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd1db-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dd1db-123">Return value</span></span>

<span data-ttu-id="dd1db-124">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dd1db-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd1db-125">Requirements</span></span>



| <span data-ttu-id="dd1db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd1db-126">Requirement</span></span> | <span data-ttu-id="dd1db-127">Valor</span><span class="sxs-lookup"><span data-stu-id="dd1db-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1db-128">Versão</span><span class="sxs-lookup"><span data-stu-id="dd1db-128">Version</span></span><br/> | <span data-ttu-id="dd1db-129">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dd1db-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dd1db-130">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dd1db-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dd1db-131">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="dd1db-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="dd1db-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dd1db-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="dd1db-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd1db-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="dd1db-134">IID</span><span class="sxs-lookup"><span data-stu-id="dd1db-134">IID</span></span><br/>     | <span data-ttu-id="dd1db-135">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dd1db-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="dd1db-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd1db-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1db-137">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="dd1db-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="dd1db-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="dd1db-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="dd1db-139">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="dd1db-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




