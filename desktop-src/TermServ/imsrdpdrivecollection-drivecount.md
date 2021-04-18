---
title: Propriedade IMsRdpDriveCollection DriveCount
description: Recupera a contagem de objetos na coleção. | Propriedade IMsRdpDriveCollection DriveCount
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DriveCount
- Propriedade DriveCount Serviços de Área de Trabalho Remota, interface IMsRdpDriveCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveCollection, Propriedade DriveCount
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105789435"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="e1f79-107">IMsRdpDriveCollection: Propriedade riveCount de:D</span><span class="sxs-lookup"><span data-stu-id="e1f79-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="e1f79-108">Recupera a contagem de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="e1f79-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="e1f79-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e1f79-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f79-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1f79-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="e1f79-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e1f79-111">Property value</span></span>

<span data-ttu-id="e1f79-112">A contagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="e1f79-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e1f79-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e1f79-113">Error codes</span></span>

<span data-ttu-id="e1f79-114">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="e1f79-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e1f79-115">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="e1f79-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f79-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1f79-116">Requirements</span></span>



| <span data-ttu-id="e1f79-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1f79-117">Requirement</span></span> | <span data-ttu-id="e1f79-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e1f79-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f79-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1f79-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e1f79-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1f79-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="e1f79-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1f79-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e1f79-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1f79-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e1f79-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e1f79-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1f79-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1f79-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e1f79-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e1f79-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1f79-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1f79-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="e1f79-127">IID</span><span class="sxs-lookup"><span data-stu-id="e1f79-127">IID</span></span><br/>                      | <span data-ttu-id="e1f79-128">IID \_ IMsRdpDriveCollection é definido como 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="e1f79-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1f79-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1f79-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f79-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="e1f79-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





