---
description: O método SourceListAddMediaDisk adiciona um disco ao conjunto de discos registrados. Aceita DiskId, VolumeLabel e DiskPrompt como parâmetros. Esse método chama em MsiSourceListAddMediaDisk.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Método patch. SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a7c74ccdfb90a0cb365e6110defc9b60dac1f471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751190"
---
# <a name="patchsourcelistaddmediadisk-method"></a><span data-ttu-id="a5db7-105">Método patch. SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="a5db7-105">Patch.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="a5db7-106">O método **SourceListAddMediaDisk** adiciona um disco ao conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="a5db7-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="a5db7-107">Aceita *DiskId*, *VolumeLabel* e *DiskPrompt* como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a5db7-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="a5db7-108">Esse método chama em [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="a5db7-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5db7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5db7-109">Syntax</span></span>


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="a5db7-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5db7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5db7-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="a5db7-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="a5db7-112">Esse parâmetro fornece a ID do disco que está sendo adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="a5db7-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="a5db7-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="a5db7-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="a5db7-114">Esse parâmetro fornece o rótulo do disco que está sendo adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="a5db7-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="a5db7-115">Uma atualização substitui o rótulo de volume existente no registro.</span><span class="sxs-lookup"><span data-stu-id="a5db7-115">An update, overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="a5db7-116">Para alterar apenas a solicitação de disco, obtenha o rótulo de volume registrado existente e forneça-o junto com o novo prompt de disco.</span><span class="sxs-lookup"><span data-stu-id="a5db7-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="a5db7-117">Uma cadeia de caracteres nula ou vazia registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o rótulo do volume.</span><span class="sxs-lookup"><span data-stu-id="a5db7-117">A NULL or empty string registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="a5db7-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="a5db7-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="a5db7-119">Esse parâmetro fornece o prompt de disco do disco que está sendo adicionado ou atualizado.</span><span class="sxs-lookup"><span data-stu-id="a5db7-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="a5db7-120">Uma atualização substitui o prompt de disco existente no registro.</span><span class="sxs-lookup"><span data-stu-id="a5db7-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="a5db7-121">Para alterar apenas o rótulo do volume, obtenha o prompt de disco existente do registro e forneça o novo rótulo de volume.</span><span class="sxs-lookup"><span data-stu-id="a5db7-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="a5db7-122">Uma cadeia de caracteres nula ou vazia registra uma cadeia de caracteres vazia (0 bytes de comprimento) como o prompt de disco.</span><span class="sxs-lookup"><span data-stu-id="a5db7-122">A NULL or empty string registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5db7-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a5db7-123">Return value</span></span>

<span data-ttu-id="a5db7-124">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a5db7-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5db7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5db7-125">Requirements</span></span>



| <span data-ttu-id="a5db7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5db7-126">Requirement</span></span> | <span data-ttu-id="a5db7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a5db7-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5db7-128">Versão</span><span class="sxs-lookup"><span data-stu-id="a5db7-128">Version</span></span><br/> | <span data-ttu-id="a5db7-129">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a5db7-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a5db7-130">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5db7-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a5db7-131">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a5db7-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="a5db7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a5db7-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="a5db7-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5db7-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="a5db7-134">IID</span><span class="sxs-lookup"><span data-stu-id="a5db7-134">IID</span></span><br/>     | <span data-ttu-id="a5db7-135">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="a5db7-135">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="a5db7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5db7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5db7-137">**Patch**</span><span class="sxs-lookup"><span data-stu-id="a5db7-137">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="a5db7-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="a5db7-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="a5db7-139">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="a5db7-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




