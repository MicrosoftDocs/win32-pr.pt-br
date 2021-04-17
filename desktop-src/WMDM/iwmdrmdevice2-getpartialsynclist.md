---
title: Método IWMDRMDevice2 GetPartialSyncList
description: O método GetPartialSyncList Obtém uma lista de sincronização parcial.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Método GetPartialSyncList Windows Media Gerenciador de Dispositivos
- Método GetPartialSyncList Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gerenciador de Dispositivos, método GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811362"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="17ca8-106">Método IWMDRMDevice2:: GetPartialSyncList</span><span class="sxs-lookup"><span data-stu-id="17ca8-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="17ca8-107">O método **GetPartialSyncList** Obtém uma lista de sincronização parcial.</span><span class="sxs-lookup"><span data-stu-id="17ca8-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ca8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17ca8-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="17ca8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17ca8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ca8-110">*cMinCountThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-111">Limite de contagem mínima.</span><span class="sxs-lookup"><span data-stu-id="17ca8-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-112">*cMinHoursThreshold* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-113">Limite mínimo de horas.</span><span class="sxs-lookup"><span data-stu-id="17ca8-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-114">*dwStartingIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-115">Posição inicial para indexação.</span><span class="sxs-lookup"><span data-stu-id="17ca8-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-116">*cItems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-117">Contagem de itens a serem indexados.</span><span class="sxs-lookup"><span data-stu-id="17ca8-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-118">*ppbSyncList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-119">Lista de sincronização de licenças recuperada.</span><span class="sxs-lookup"><span data-stu-id="17ca8-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-120">*pcbSyncList* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-121">Tamanho da lista de sincronização de licenças, em bytes.</span><span class="sxs-lookup"><span data-stu-id="17ca8-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-122">*pdwNextStartingIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-123">Próxima posição de início para indexação.</span><span class="sxs-lookup"><span data-stu-id="17ca8-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="17ca8-124">*pcItemsProcessed* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="17ca8-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17ca8-125">Contagem de itens que estão sendo processados.</span><span class="sxs-lookup"><span data-stu-id="17ca8-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ca8-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17ca8-126">Return value</span></span>

<span data-ttu-id="17ca8-127">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="17ca8-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="17ca8-128">Todos os métodos de interface no Windows Media Gerenciador de Dispositivos podem retornar qualquer uma das seguintes classes de códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="17ca8-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="17ca8-129">Códigos de erro padrão COM</span><span class="sxs-lookup"><span data-stu-id="17ca8-129">Standard COM error codes</span></span>
-   <span data-ttu-id="17ca8-130">Códigos de erro do Windows convertidos em valores HRESULT</span><span class="sxs-lookup"><span data-stu-id="17ca8-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="17ca8-131">Códigos de erro do Windows Media Gerenciador de Dispositivos</span><span class="sxs-lookup"><span data-stu-id="17ca8-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="17ca8-132">Para obter uma lista extensa de possíveis códigos de erro, consulte [códigos de erro](error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="17ca8-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17ca8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17ca8-133">Requirements</span></span>



| <span data-ttu-id="17ca8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ca8-134">Requirement</span></span> | <span data-ttu-id="17ca8-135">Valor</span><span class="sxs-lookup"><span data-stu-id="17ca8-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17ca8-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17ca8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="17ca8-137"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17ca8-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="17ca8-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17ca8-138">Library</span></span><br/> | <dl> <span data-ttu-id="17ca8-139"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17ca8-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ca8-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="17ca8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ca8-141">**IWMDRMDevice:: getsynclist**</span><span class="sxs-lookup"><span data-stu-id="17ca8-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="17ca8-142">**Interface IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="17ca8-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





