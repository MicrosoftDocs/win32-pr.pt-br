---
description: Redefine a sequência de enumeração para o início.
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
ms.openlocfilehash: 3a6846ea928afb6cd52f20098cd100b94b3a564e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798243"
---
# <a name="ienumportabledeviceconnectorsreset-method"></a><span data-ttu-id="c7e8e-103">Método IEnumPortableDeviceConnectors:: Reset</span><span class="sxs-lookup"><span data-stu-id="c7e8e-103">IEnumPortableDeviceConnectors::Reset method</span></span>

<span data-ttu-id="c7e8e-104">O método de **redefinição** redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-104">The **Reset** method resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e8e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7e8e-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="c7e8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7e8e-106">Parameters</span></span>

<span data-ttu-id="c7e8e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7e8e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7e8e-108">Return value</span></span>

<span data-ttu-id="c7e8e-109">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c7e8e-110">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c7e8e-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c7e8e-111">Return code</span></span>                                                                          | <span data-ttu-id="c7e8e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7e8e-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c7e8e-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7e8e-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c7e8e-114">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="c7e8e-114">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7e8e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7e8e-115">Requirements</span></span>



| <span data-ttu-id="c7e8e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e8e-116">Requirement</span></span> | <span data-ttu-id="c7e8e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e8e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e8e-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e8e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e8e-119">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c7e8e-119">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="c7e8e-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e8e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e8e-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c7e8e-121">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="c7e8e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7e8e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e8e-123"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e8e-123"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="c7e8e-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="c7e8e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7e8e-125"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7e8e-125"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="c7e8e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7e8e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7e8e-127"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7e8e-127"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="c7e8e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7e8e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e8e-129">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="c7e8e-129">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




