---
description: A propriedade MediaDisks enumera todos os discos de mídia para esta instância de produto. Essa propriedade chama o MsiSourceListEnumMediaDisks. Retorna as informações de disco como matriz de objetos de registro.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Propriedade patch. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747959"
---
# <a name="patchmediadisks-property"></a><span data-ttu-id="e40f1-105">Propriedade patch. MediaDisks</span><span class="sxs-lookup"><span data-stu-id="e40f1-105">Patch.MediaDisks property</span></span>

<span data-ttu-id="e40f1-106">A propriedade **MediaDisks** enumera todos os discos de mídia para esta instância de produto.</span><span class="sxs-lookup"><span data-stu-id="e40f1-106">The **MediaDisks** property enumerates all the media disks for this product instance.</span></span> <span data-ttu-id="e40f1-107">Essa propriedade chama o [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span><span class="sxs-lookup"><span data-stu-id="e40f1-107">This property calls the [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa).</span></span> <span data-ttu-id="e40f1-108">Retorna as informações de disco como matriz de objetos de [**registro**](record-object.md) .</span><span class="sxs-lookup"><span data-stu-id="e40f1-108">Returns the disk information as array of [**Record**](record-object.md) objects.</span></span>

<span data-ttu-id="e40f1-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e40f1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40f1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e40f1-110">Syntax</span></span>


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a><span data-ttu-id="e40f1-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e40f1-111">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="e40f1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e40f1-112">Remarks</span></span>

<span data-ttu-id="e40f1-113">Em cada registro, o primeiro campo contém a ID do disco, o segundo campo contém o rótulo do volume e o terceiro campo contém o prompt do disco registrado para o disco.</span><span class="sxs-lookup"><span data-stu-id="e40f1-113">In each record the first field contains the disk Id, the second field contains the volume label and the third field contains the disk prompt registered for the disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="e40f1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e40f1-114">Requirements</span></span>



| <span data-ttu-id="e40f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e40f1-115">Requirement</span></span> | <span data-ttu-id="e40f1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e40f1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e40f1-117">Versão</span><span class="sxs-lookup"><span data-stu-id="e40f1-117">Version</span></span><br/> | <span data-ttu-id="e40f1-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e40f1-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e40f1-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e40f1-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e40f1-120">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="e40f1-120">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="e40f1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e40f1-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="e40f1-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40f1-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="e40f1-123">IID</span><span class="sxs-lookup"><span data-stu-id="e40f1-123">IID</span></span><br/>     | <span data-ttu-id="e40f1-124">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e40f1-124">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="e40f1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e40f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40f1-126">**Patch**</span><span class="sxs-lookup"><span data-stu-id="e40f1-126">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="e40f1-127">**MsiSourceListEnumMediaDisks**</span><span class="sxs-lookup"><span data-stu-id="e40f1-127">**MsiSourceListEnumMediaDisks**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[<span data-ttu-id="e40f1-128">**Gravável**</span><span class="sxs-lookup"><span data-stu-id="e40f1-128">**Record**</span></span>](record-object.md)
</dt> <dt>

[<span data-ttu-id="e40f1-129">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="e40f1-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




