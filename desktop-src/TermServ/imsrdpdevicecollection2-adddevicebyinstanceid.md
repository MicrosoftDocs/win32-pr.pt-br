---
title: Método IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Adiciona um dispositivo não listado à coleção de dispositivos.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddDeviceByInstanceId
- Método AddDeviceByInstanceId Serviços de Área de Trabalho Remota, interface IMsRdpDeviceCollection2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection2, método AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008884"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="a3d51-106">Método IMsRdpDeviceCollection2:: AddDeviceByInstanceId</span><span class="sxs-lookup"><span data-stu-id="a3d51-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="a3d51-107">Adiciona um dispositivo não listado à coleção de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a3d51-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d51-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d51-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="a3d51-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d51-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d51-110">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="a3d51-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d51-111">Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d51-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="a3d51-112">Um valor da enumeração [**RedirectDeviceType**](redirectdevicetype.md) que especifica o tipo de dispositivo que está sendo adicionado.</span><span class="sxs-lookup"><span data-stu-id="a3d51-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="a3d51-113">*InstanceId* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3d51-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d51-114">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a3d51-114">Type: **BSTR**</span></span>

<span data-ttu-id="a3d51-115">O identificador de instância do dispositivo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="a3d51-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d51-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3d51-116">Return value</span></span>

<span data-ttu-id="a3d51-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a3d51-117">Type: **HRESULT**</span></span>

<span data-ttu-id="a3d51-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3d51-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3d51-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3d51-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d51-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3d51-120">Requirements</span></span>



| <span data-ttu-id="a3d51-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d51-121">Requirement</span></span> | <span data-ttu-id="a3d51-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a3d51-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d51-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3d51-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3d51-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3d51-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a3d51-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3d51-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3d51-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3d51-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a3d51-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a3d51-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3d51-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3d51-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a3d51-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a3d51-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3d51-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3d51-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3d51-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3d51-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d51-132">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="a3d51-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="a3d51-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="a3d51-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





