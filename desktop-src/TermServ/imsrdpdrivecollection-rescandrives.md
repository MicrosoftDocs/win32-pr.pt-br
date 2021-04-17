---
title: Método IMsRdpDriveCollection RescanDrives
description: Atualiza a lista de objetos na coleção. | Método IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método RescanDrives
- Método RescanDrives Serviços de Área de Trabalho Remota, interface IMsRdpDriveCollection
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveCollection, método RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105813030"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="aa7ce-107">Método IMsRdpDriveCollection:: RescanDrives</span><span class="sxs-lookup"><span data-stu-id="aa7ce-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="aa7ce-108">Atualiza a lista de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7ce-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa7ce-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="aa7ce-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa7ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa7ce-111">*vboolDynRedir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa7ce-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa7ce-112">O estado de redirecionamento padrão que será aplicado a quaisquer unidades ou dispositivos descobertos recentemente.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa7ce-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa7ce-113">Return value</span></span>

<span data-ttu-id="aa7ce-114">Se o método for bem sucedido, **S \_ OK** será retornado.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="aa7ce-115">Qualquer outro valor **HRESULT** indica que a chamada falhou.</span><span class="sxs-lookup"><span data-stu-id="aa7ce-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa7ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa7ce-116">Requirements</span></span>



| <span data-ttu-id="aa7ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa7ce-117">Requirement</span></span> | <span data-ttu-id="aa7ce-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa7ce-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7ce-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa7ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7ce-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa7ce-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="aa7ce-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa7ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7ce-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa7ce-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aa7ce-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa7ce-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa7ce-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ce-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="aa7ce-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aa7ce-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa7ce-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa7ce-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="aa7ce-127">IID</span><span class="sxs-lookup"><span data-stu-id="aa7ce-127">IID</span></span><br/>                      | <span data-ttu-id="aa7ce-128">IID \_ IMsRdpDriveCollection é definido como 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="aa7ce-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa7ce-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa7ce-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7ce-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="aa7ce-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





