---
description: Os dispositivos portáteis do Windows (WPD) oferecem suporte às seguintes propriedades de parâmetros de comando.
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: Parâmetros de comando (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7687488c38f95fd6d7e7b69d64ad6ae32631700d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765003"
---
# <a name="command-parameters"></a><span data-ttu-id="fe383-103">Parâmetros de comando</span><span class="sxs-lookup"><span data-stu-id="fe383-103">Command Parameters</span></span>

<span data-ttu-id="fe383-104">Os dispositivos portáteis do Windows (WPD) oferecem suporte às seguintes propriedades de parâmetros de comando.</span><span class="sxs-lookup"><span data-stu-id="fe383-104">Windows Portable Devices (WPD) supports the following properties of command parameters.</span></span>




| <span data-ttu-id="fe383-105">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="fe383-105">**Property**</span></span>                                            | <span data-ttu-id="fe383-106">**VarType**</span><span class="sxs-lookup"><span data-stu-id="fe383-106">**VarType**</span></span>     | <span data-ttu-id="fe383-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fe383-107">**Description**</span></span>                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe383-108">**\_ \_ informações comuns do \_ cliente da propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-108">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION**</span></span>          | <span data-ttu-id="fe383-109">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="fe383-109">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="fe383-110">Uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) que o driver usa para identificar o cliente.</span><span class="sxs-lookup"><span data-stu-id="fe383-110">An [**IPortableDeviceValues**](iportabledevicevalues.md) interface that the driver uses to identify the client.</span></span>                                                             |
| <span data-ttu-id="fe383-111">**\_contexto de \_ informações comuns do \_ cliente da \_ Propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-111">**WPD\_PROPERTY\_COMMON\_CLIENT\_INFORMATION\_CONTEXT**</span></span> | <span data-ttu-id="fe383-112">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="fe383-113">Um contexto especificado pelo driver que identifica um cliente para todas as operações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fe383-113">A driver-specified context which identifies a client for all subsequent operations.</span></span>                                                                                          |
| <span data-ttu-id="fe383-114">**\_categoria de \_ \_ comando comum de propriedade \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="fe383-114">**WPD\_PROPERTY\_COMMON\_COMMAND\_CATEGORY**</span></span>            | <span data-ttu-id="fe383-115">**CLSID do VT \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-115">**VT\_CLSID**</span></span>   | <span data-ttu-id="fe383-116">A parte **GUID** do valor **PROPERTYKEY** do comando.</span><span class="sxs-lookup"><span data-stu-id="fe383-116">The **GUID** portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                                            |
| <span data-ttu-id="fe383-117">**\_ID de \_ \_ comando comum da propriedade \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="fe383-117">**WPD\_PROPERTY\_COMMON\_COMMAND\_ID**</span></span>                  | <span data-ttu-id="fe383-118">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="fe383-118">**VT\_UI4**</span></span>     | <span data-ttu-id="fe383-119">A porção de ID exclusiva persistente (PID) do valor **PROPERTYKEY** do comando.</span><span class="sxs-lookup"><span data-stu-id="fe383-119">The Persistent Unique ID (PID) portion of the **PROPERTYKEY** value of the command.</span></span>                                                                                          |
| <span data-ttu-id="fe383-120">**\_destino de \_ \_ comando comum de propriedade \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="fe383-120">**WPD\_PROPERTY\_COMMON\_COMMAND\_TARGET**</span></span>              | <span data-ttu-id="fe383-121">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-121">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="fe383-122">O identificador de objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="fe383-122">The target-object identifier.</span></span>                                                                                                                                                |
| <span data-ttu-id="fe383-123">**\_código de \_ \_ erro de driver comum de propriedade \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-123">**WPD\_PROPERTY\_COMMON\_DRIVER\_ERROR\_CODE**</span></span>          | <span data-ttu-id="fe383-124">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="fe383-124">**VT\_UI4**</span></span>     | <span data-ttu-id="fe383-125">Um código de erro específico do driver retornado por um driver WPD.</span><span class="sxs-lookup"><span data-stu-id="fe383-125">A driver-specific error code returned by a WPD driver.</span></span>                                                                                                                       |
| <span data-ttu-id="fe383-126">**\_ \_ HRESULT comum de propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-126">**WPD\_PROPERTY\_COMMON\_HRESULT**</span></span>                      | <span data-ttu-id="fe383-127">**erro de VT \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-127">**VT\_ERROR**</span></span>   | <span data-ttu-id="fe383-128">O valor **HRESULT** retornado por um driver WPD para uma operação específica.</span><span class="sxs-lookup"><span data-stu-id="fe383-128">The **HRESULT** value returned by a WPD driver for a particular operation.</span></span>                                                                                                   |
| <span data-ttu-id="fe383-129">**\_IDs de \_ \_ objeto comum de propriedade \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="fe383-129">**WPD\_PROPERTY\_COMMON\_OBJECT\_IDS**</span></span>                  | <span data-ttu-id="fe383-130">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="fe383-130">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="fe383-131">Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de Variant Type **VT \_ LPWSTR** que contém uma lista de identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="fe383-131">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of object identifiers.</span></span> |
| <span data-ttu-id="fe383-132">**as \_ \_ \_ \_ IDs exclusivas persistentes comuns da propriedade WPD \_**</span><span class="sxs-lookup"><span data-stu-id="fe383-132">**WPD\_PROPERTY\_COMMON\_PERSISTENT\_UNIQUE\_IDS**</span></span>      | <span data-ttu-id="fe383-133">**VT \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="fe383-133">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="fe383-134">Uma interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de Variant Type **VT \_ LPWSTR** que contém uma lista de PIDs.</span><span class="sxs-lookup"><span data-stu-id="fe383-134">An [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface of variant type **VT\_LPWSTR** that contains a list of PIDs.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="fe383-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe383-135">Requirements</span></span>



| <span data-ttu-id="fe383-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe383-136">Requirement</span></span> | <span data-ttu-id="fe383-137">Valor</span><span class="sxs-lookup"><span data-stu-id="fe383-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe383-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe383-138">Header</span></span><br/> | <dl> <span data-ttu-id="fe383-139"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe383-139"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe383-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe383-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe383-141">**Propriedades e atributos**</span><span class="sxs-lookup"><span data-stu-id="fe383-141">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




