---
title: Propriedade IMsRdpDriveCollection DriveByIndex
description: Recupera a unidade no índice especificado.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DriveByIndex
- Propriedade DriveByIndex Serviços de Área de Trabalho Remota, interface IMsRdpDriveCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveCollection, Propriedade DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369778"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="3e3a6-106">IMsRdpDriveCollection: Propriedade riveByIndex de:D</span><span class="sxs-lookup"><span data-stu-id="3e3a6-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="3e3a6-107">Recupera a unidade no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="3e3a6-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="3e3a6-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="3e3a6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e3a6-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="3e3a6-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3e3a6-110">Property value</span></span>

<span data-ttu-id="3e3a6-111">Um ponteiro de interface [**IMsRdpDrive**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="3e3a6-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e3a6-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="3e3a6-112">Error codes</span></span>

<span data-ttu-id="3e3a6-113">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="3e3a6-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="3e3a6-114">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="3e3a6-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3a6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e3a6-115">Requirements</span></span>



| <span data-ttu-id="3e3a6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e3a6-116">Requirement</span></span> | <span data-ttu-id="3e3a6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3e3a6-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3a6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e3a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3e3a6-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e3a6-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="3e3a6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e3a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3e3a6-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e3a6-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3e3a6-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3e3a6-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e3a6-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e3a6-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="3e3a6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3e3a6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e3a6-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e3a6-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="3e3a6-126">IID</span><span class="sxs-lookup"><span data-stu-id="3e3a6-126">IID</span></span><br/>                      | <span data-ttu-id="3e3a6-127">IID \_ IMsRdpDriveCollection é definido como 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="3e3a6-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e3a6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e3a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3a6-129">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="3e3a6-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





