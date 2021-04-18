---
title: Método getsincronizalist do IWMDRMDevice
description: O método getsincronizarlist recupera a lista de sincronização de licenças no dispositivo. A sincronização de licenças permite que o computador host transfira licenças atualizadas para um dispositivo de acordo com os critérios especificados.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Método getsincronizarlist Windows Media Gerenciador de Dispositivos
- Método getsincronizarlist Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método getsincronizarlist
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784930"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="6a045-107">Método IWMDRMDevice:: getsynclist</span><span class="sxs-lookup"><span data-stu-id="6a045-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="6a045-108">O método **Getsincronizarlist** recupera a lista de sincronização de licenças no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6a045-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="6a045-109">A sincronização de licenças permite que o computador host transfira licenças atualizadas para um dispositivo de acordo com os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="6a045-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a045-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a045-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="6a045-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a045-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a045-112">*cMinCountThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a045-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a045-113">Limite de contagem mínima.</span><span class="sxs-lookup"><span data-stu-id="6a045-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="6a045-114">*cMinHoursThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6a045-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a045-115">Limite mínimo de horas.</span><span class="sxs-lookup"><span data-stu-id="6a045-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="6a045-116">*ppbSyncList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a045-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a045-117">Lista de sincronização de licenças recuperada.</span><span class="sxs-lookup"><span data-stu-id="6a045-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="6a045-118">*pcbSyncList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a045-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a045-119">Tamanho da lista de sincronização de licenças, em bytes.</span><span class="sxs-lookup"><span data-stu-id="6a045-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a045-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a045-120">Return value</span></span>

<span data-ttu-id="6a045-121">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6a045-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6a045-122">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a045-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6a045-123">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6a045-123">Return code</span></span>                                                                          | <span data-ttu-id="6a045-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="6a045-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6a045-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6a045-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6a045-126">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6a045-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6a045-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a045-127">Requirements</span></span>



| <span data-ttu-id="6a045-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a045-128">Requirement</span></span> | <span data-ttu-id="6a045-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6a045-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a045-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a045-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6a045-131"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a045-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="6a045-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a045-132">Library</span></span><br/> | <dl> <span data-ttu-id="6a045-133"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a045-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a045-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a045-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a045-135">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="6a045-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





