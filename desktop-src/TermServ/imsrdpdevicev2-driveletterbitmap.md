---
title: Propriedade IMsRdpDeviceV2 DriveLetterBitmap
description: Contém um campo de bits que representa um mapa de letras de unidade contidas no dispositivo.
ms.assetid: 13b7c9b9-a97f-4474-b5ad-833abff384f5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DriveLetterBitmap
- Propriedade DriveLetterBitmap Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade DriveLetterBitmap
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DriveLetterBitmap
- IMsRdpDeviceV2.get_DriveLetterBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d13189415630539ac47d7a0e0a094b7b3212e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644273"
---
# <a name="imsrdpdevicev2driveletterbitmap-property"></a><span data-ttu-id="d148d-106">IMsRdpDeviceV2: Propriedade riveLetterBitmap de:D</span><span class="sxs-lookup"><span data-stu-id="d148d-106">IMsRdpDeviceV2::DriveLetterBitmap property</span></span>

<span data-ttu-id="d148d-107">Contém um campo de bits que representa um mapa de letras de unidade contidas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d148d-107">Contains a bitfield that represents a map of drive letters contained within the device.</span></span>

<span data-ttu-id="d148d-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="d148d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d148d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d148d-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterBitmap(
  [out, retval] ULONG *pDriveLetterBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="d148d-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d148d-110">Property value</span></span>

<span data-ttu-id="d148d-111">Um mapa de letras de unidade contidas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d148d-111">A map of drive letters contained within the device.</span></span> <span data-ttu-id="d148d-112">Cada bit no valor representa uma letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="d148d-112">Each bit in the value represents a drive letter.</span></span> <span data-ttu-id="d148d-113">O bit menos significativo representa a letra da unidade "A", o próximo bit representa a letra da unidade "B" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d148d-113">The least significant bit represents drive letter "A", the next bit represents drive letter "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="d148d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d148d-114">Requirements</span></span>



| <span data-ttu-id="d148d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d148d-115">Requirement</span></span> | <span data-ttu-id="d148d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d148d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d148d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d148d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d148d-118">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="d148d-118">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="d148d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d148d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d148d-120">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="d148d-120">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="d148d-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d148d-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="d148d-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d148d-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d148d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d148d-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d148d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d148d-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d148d-125">IID</span><span class="sxs-lookup"><span data-stu-id="d148d-125">IID</span></span><br/>                      | <span data-ttu-id="d148d-126">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="d148d-126">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="d148d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d148d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d148d-128">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="d148d-128">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





