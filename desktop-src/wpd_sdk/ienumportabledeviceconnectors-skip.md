---
description: Ignora o número especificado de dispositivos na sequência de enumeração.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Método IEnumPortableDeviceConnectors:: Skip (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: c00daecccd12beee8e9e741c2906e47484fa6da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011378"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a><span data-ttu-id="3ee40-103">Método IEnumPortableDeviceConnectors:: Skip</span><span class="sxs-lookup"><span data-stu-id="3ee40-103">IEnumPortableDeviceConnectors::Skip method</span></span>

<span data-ttu-id="3ee40-104">O método **Skip** ignora o número especificado de dispositivos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3ee40-104">The **Skip** method skips the specified number of devices in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ee40-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ee40-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a><span data-ttu-id="3ee40-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ee40-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ee40-107">*cConnectors* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3ee40-107">*cConnectors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ee40-108">O número de dispositivos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="3ee40-108">The number of devices to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ee40-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3ee40-109">Return value</span></span>

<span data-ttu-id="3ee40-110">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3ee40-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3ee40-111">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ee40-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3ee40-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3ee40-112">Return code</span></span>                                                                             | <span data-ttu-id="3ee40-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ee40-113">Description</span></span>                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ee40-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ee40-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="3ee40-115">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="3ee40-115">The method succeeded.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="3ee40-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="3ee40-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="3ee40-117">O número especificado de dispositivos não pôde ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="3ee40-117">The specified number of devices could not be skipped.</span></span> <span data-ttu-id="3ee40-118">Uma causa possível: o parâmetro *cConnectors* especifica mais dispositivos do que realmente permanecem na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="3ee40-118">One possible cause: The *cConnectors* parameter specifies more devices than actually remain in the enumeration sequence.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ee40-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ee40-119">Requirements</span></span>



| <span data-ttu-id="3ee40-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ee40-120">Requirement</span></span> | <span data-ttu-id="3ee40-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3ee40-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee40-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ee40-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee40-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3ee40-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="3ee40-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3ee40-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee40-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3ee40-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                                   |
| <span data-ttu-id="3ee40-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3ee40-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee40-127"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee40-127"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="3ee40-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="3ee40-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ee40-129"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ee40-129"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="3ee40-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ee40-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ee40-131"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ee40-131"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="3ee40-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3ee40-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee40-133">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="3ee40-133">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




