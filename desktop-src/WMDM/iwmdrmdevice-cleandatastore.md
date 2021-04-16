---
title: Método IWMDRMDevice CleanDataStore
description: O método CleanDataStore inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Método CleanDataStore Windows Media Gerenciador de Dispositivos
- Método CleanDataStore Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794535"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="6df0a-106">Método IWMDRMDevice:: CleanDataStore</span><span class="sxs-lookup"><span data-stu-id="6df0a-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="6df0a-107">O método **CleanDataStore** inicia o processo de limpeza do armazenamento de dados DRM no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6df0a-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df0a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6df0a-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6df0a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6df0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df0a-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6df0a-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6df0a-111">Sinalizadores para critérios de limpeza de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6df0a-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df0a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6df0a-112">Return value</span></span>

<span data-ttu-id="6df0a-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6df0a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6df0a-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6df0a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6df0a-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6df0a-115">Return code</span></span>                                                                          | <span data-ttu-id="6df0a-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6df0a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6df0a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6df0a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6df0a-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6df0a-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6df0a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6df0a-119">Requirements</span></span>



| <span data-ttu-id="6df0a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6df0a-120">Requirement</span></span> | <span data-ttu-id="6df0a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6df0a-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6df0a-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6df0a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="6df0a-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6df0a-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="6df0a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6df0a-124">Library</span></span><br/> | <dl> <span data-ttu-id="6df0a-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6df0a-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df0a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6df0a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df0a-127">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="6df0a-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





