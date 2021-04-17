---
title: Método getlicenciadostate IWMDRMDevice2
description: O método getlicenciadostate Obtém o estado da licença.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Método getlicenciadostate Windows Media Gerenciador de Dispositivos
- Método getlicenciadostate Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gerenciador de Dispositivos, método getlicenciadostate
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759761"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="78214-106">Método IWMDRMDevice2:: getlicenciadostate</span><span class="sxs-lookup"><span data-stu-id="78214-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="78214-107">O método **Getlicenciadostate** Obtém o estado da licença.</span><span class="sxs-lookup"><span data-stu-id="78214-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="78214-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78214-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="78214-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78214-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78214-110">*pbStateQueryData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78214-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78214-111">Ponteiro para os dados consultados do estado da licença.</span><span class="sxs-lookup"><span data-stu-id="78214-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="78214-112">*cbStateQueryData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="78214-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78214-113">Contagem dos dados consultados.</span><span class="sxs-lookup"><span data-stu-id="78214-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="78214-114">*pdwCategory* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="78214-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78214-115">Ponteiro para a categoria.</span><span class="sxs-lookup"><span data-stu-id="78214-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="78214-116">*pcRemainingCounts* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="78214-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78214-117">Ponteiro para as contagens restantes.</span><span class="sxs-lookup"><span data-stu-id="78214-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="78214-118">*pcRemainingHours* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="78214-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78214-119">Ponteiro para as horas restantes.</span><span class="sxs-lookup"><span data-stu-id="78214-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="78214-120">*pdwReserved* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="78214-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78214-121">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="78214-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78214-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78214-122">Return value</span></span>

<span data-ttu-id="78214-123">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="78214-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="78214-124">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="78214-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="78214-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="78214-125">Return code</span></span>                                                                          | <span data-ttu-id="78214-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="78214-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="78214-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78214-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="78214-128">O método é executado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="78214-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="78214-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78214-129">Requirements</span></span>



| <span data-ttu-id="78214-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="78214-130">Requirement</span></span> | <span data-ttu-id="78214-131">Valor</span><span class="sxs-lookup"><span data-stu-id="78214-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78214-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78214-132">Header</span></span><br/>  | <dl> <span data-ttu-id="78214-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78214-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="78214-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78214-134">Library</span></span><br/> | <dl> <span data-ttu-id="78214-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78214-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78214-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="78214-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78214-137">**Interface IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="78214-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





