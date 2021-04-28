---
description: 'Método IEnumPortableDeviceConnectors:: Reset – redefine a sequência de enumeração para o início.'
ms.assetid: 1df1ff95-06ae-4e5e-8064-17f832c5f0b3
title: 'Método IEnumPortableDeviceConnectors:: Reset (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Reset
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 10a356fbb8591568a9f99d9b92d681a46754a960
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083195"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="f8b41-103">Método IEnumPortableDeviceConnectors:: Reset</span><span class="sxs-lookup"><span data-stu-id="f8b41-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="f8b41-104">O método de **redefinição** redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="f8b41-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8b41-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f8b41-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="f8b41-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f8b41-106">Parameters</span></span>

<span data-ttu-id="f8b41-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f8b41-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8b41-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f8b41-108">Return value</span></span>

<span data-ttu-id="f8b41-109">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f8b41-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f8b41-110">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f8b41-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f8b41-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f8b41-111">Return code</span></span>                                                                          | <span data-ttu-id="f8b41-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8b41-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f8b41-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f8b41-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f8b41-114">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f8b41-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f8b41-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8b41-115">Requirements</span></span>



| <span data-ttu-id="f8b41-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b41-116">Requirement</span></span> | <span data-ttu-id="f8b41-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f8b41-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b41-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8b41-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f8b41-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f8b41-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="f8b41-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f8b41-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f8b41-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f8b41-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="f8b41-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f8b41-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8b41-123"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b41-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="f8b41-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="f8b41-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8b41-125"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8b41-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="f8b41-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f8b41-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f8b41-127"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8b41-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="f8b41-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f8b41-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b41-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="f8b41-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




