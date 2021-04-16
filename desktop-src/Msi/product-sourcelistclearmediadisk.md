---
description: O método SourceListClearMediaDisk do objeto Product remove um disco especificado do conjunto de discos registrados para um produto. Aceita DiskId como um parâmetro. Esse método chama MsiSourceListClearMediaDisk.
ms.assetid: 7eec644e-5127-4c17-a8bd-6b0eb091c8aa
title: Método Product. SourceListClearMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a607591f45208854118b0f97849cd7072e484bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750221"
---
# <a name="productsourcelistclearmediadisk-method"></a><span data-ttu-id="9bd02-105">Método Product. SourceListClearMediaDisk</span><span class="sxs-lookup"><span data-stu-id="9bd02-105">Product.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="9bd02-106">O método **SourceListClearMediaDisk** do objeto [**Product**](product-object.md) remove um disco especificado do conjunto de discos registrados para um produto.</span><span class="sxs-lookup"><span data-stu-id="9bd02-106">The **SourceListClearMediaDisk** method of the [**Product**](product-object.md) object removes a specified disk from the set of registered disks for a product.</span></span> <span data-ttu-id="9bd02-107">Aceita *DiskId* como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9bd02-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="9bd02-108">Esse método chama [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span><span class="sxs-lookup"><span data-stu-id="9bd02-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="9bd02-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9bd02-109">Syntax</span></span>


```JScript
Product.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="9bd02-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bd02-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd02-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="9bd02-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="9bd02-112">Esse parâmetro fornece a ID do disco a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9bd02-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bd02-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bd02-113">Return value</span></span>

<span data-ttu-id="9bd02-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9bd02-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd02-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bd02-115">Requirements</span></span>



| <span data-ttu-id="9bd02-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd02-116">Requirement</span></span> | <span data-ttu-id="9bd02-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9bd02-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd02-118">Versão</span><span class="sxs-lookup"><span data-stu-id="9bd02-118">Version</span></span><br/> | <span data-ttu-id="9bd02-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9bd02-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9bd02-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9bd02-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9bd02-121">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9bd02-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9bd02-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9bd02-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="9bd02-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bd02-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9bd02-124">IID</span><span class="sxs-lookup"><span data-stu-id="9bd02-124">IID</span></span><br/>     | <span data-ttu-id="9bd02-125">IID \_ IProduct é definido como 000C10A0-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9bd02-125">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="9bd02-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bd02-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd02-127">**Remessa**</span><span class="sxs-lookup"><span data-stu-id="9bd02-127">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="9bd02-128">**MsiSourceListClearMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="9bd02-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="9bd02-129">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="9bd02-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




