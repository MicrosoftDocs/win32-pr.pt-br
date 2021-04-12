---
description: Cria uma cópia da interface IEnumPortableDeviceConnectors atual.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: 'Método IEnumPortableDeviceConnectors:: clone (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 0e5273f1c400732c94c7c63918787f5e130a854d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297362"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a><span data-ttu-id="7f732-103">Método IEnumPortableDeviceConnectors:: clone</span><span class="sxs-lookup"><span data-stu-id="7f732-103">IEnumPortableDeviceConnectors::Clone method</span></span>

<span data-ttu-id="7f732-104">O método **clone** cria uma cópia da interface [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) atual.</span><span class="sxs-lookup"><span data-stu-id="7f732-104">The **Clone** method creates a copy of the current [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f732-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7f732-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="7f732-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f732-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f732-107">*ppEnum* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7f732-107">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f732-108">O endereço de um ponteiro para uma interface [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) .</span><span class="sxs-lookup"><span data-stu-id="7f732-108">The address of a pointer to an [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) interface.</span></span> <span data-ttu-id="7f732-109">O aplicativo de chamada deve liberar essa interface quando ela é feita com ela.</span><span class="sxs-lookup"><span data-stu-id="7f732-109">The calling application must release this interface when it is done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f732-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f732-110">Return value</span></span>

<span data-ttu-id="7f732-111">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7f732-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f732-112">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f732-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f732-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7f732-113">Return code</span></span>                                                                          | <span data-ttu-id="7f732-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f732-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f732-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f732-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7f732-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="7f732-116">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f732-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f732-117">Requirements</span></span>



| <span data-ttu-id="7f732-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f732-118">Requirement</span></span> | <span data-ttu-id="7f732-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7f732-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f732-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f732-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7f732-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f732-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                             |
| <span data-ttu-id="7f732-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f732-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7f732-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7f732-123">None supported</span></span><br/>                                                                                                                                              |
| <span data-ttu-id="7f732-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f732-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f732-125"><dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f732-125"><dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt></span></span> </dl> |
| <span data-ttu-id="7f732-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="7f732-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f732-127"><dt>Portabledeviceconnectapi. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f732-127"><dt>Portabledeviceconnectapi.idl</dt></span></span> </dl>                                                                |
| <span data-ttu-id="7f732-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f732-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="7f732-129"><dt>PortableDeviceGuids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7f732-129"><dt>PortableDeviceGuids.lib</dt></span></span> </dl>                                                                     |



## <a name="see-also"></a><span data-ttu-id="7f732-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f732-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f732-131">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="7f732-131">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




