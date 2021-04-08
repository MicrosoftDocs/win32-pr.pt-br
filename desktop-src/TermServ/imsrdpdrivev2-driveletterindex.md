---
title: Propriedade IMsRdpDriveV2 DriveLetterIndex
description: Contém o índice da letra da unidade.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DriveLetterIndex
- Propriedade DriveLetterIndex Serviços de Área de Trabalho Remota, interface IMsRdpDriveV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveV2, Propriedade DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39284a94950935e2d273483db871a9b08f7daf36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919203"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a><span data-ttu-id="89a4a-106">IMsRdpDriveV2: Propriedade riveLetterIndex de:D</span><span class="sxs-lookup"><span data-stu-id="89a4a-106">IMsRdpDriveV2::DriveLetterIndex property</span></span>

<span data-ttu-id="89a4a-107">Contém o índice da letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="89a4a-107">Contains the index of the letter for the drive.</span></span>

<span data-ttu-id="89a4a-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="89a4a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a4a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89a4a-109">Syntax</span></span>


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a><span data-ttu-id="89a4a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="89a4a-110">Property value</span></span>

<span data-ttu-id="89a4a-111">O índice da letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="89a4a-111">The index of the letter for the drive.</span></span> <span data-ttu-id="89a4a-112">0 = "A", 1 = "B" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="89a4a-112">0 = "A", 1 = "B", and so on.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a4a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89a4a-113">Requirements</span></span>



| <span data-ttu-id="89a4a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="89a4a-114">Requirement</span></span> | <span data-ttu-id="89a4a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="89a4a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89a4a-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89a4a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="89a4a-117">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="89a4a-117">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="89a4a-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89a4a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="89a4a-119">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89a4a-119">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="89a4a-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="89a4a-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="89a4a-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a4a-121"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89a4a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="89a4a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89a4a-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a4a-123"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89a4a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="89a4a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a4a-125">**IMsRdpDriveV2**</span><span class="sxs-lookup"><span data-stu-id="89a4a-125">**IMsRdpDriveV2**</span></span>](imsrdpdrivev2.md)
</dt> </dl>

 

 





