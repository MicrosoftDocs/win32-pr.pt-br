---
title: Método IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: O método GetAnalogVideoRestrictionLevels recupera todas as restrições de vídeo analógicas definidas na licença atual.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Formato de mídia do Windows do método GetAnalogVideoRestrictionLevels
- Método GetAnalogVideoRestrictionLevels Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807841"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="f9a70-106">Método IWMDRMLicense:: GetAnalogVideoRestrictionLevels</span><span class="sxs-lookup"><span data-stu-id="f9a70-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="f9a70-107">O método **GetAnalogVideoRestrictionLevels** recupera todas as restrições de vídeo analógicas definidas na licença atual.</span><span class="sxs-lookup"><span data-stu-id="f9a70-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a70-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9a70-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="f9a70-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9a70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a70-110">*\[ rgAnalogVideoRestrictions \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="f9a70-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a70-111">Recebe uma matriz de estruturas de [**\_ \_ \_ restrições de vídeo analógicos do WMDRM**](wmdrm-analog-video-restrictions.md) .</span><span class="sxs-lookup"><span data-stu-id="f9a70-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="f9a70-112">Defina como **NULL** para obter o número de elementos na matriz em *pcResctrictions*.</span><span class="sxs-lookup"><span data-stu-id="f9a70-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="f9a70-113">*pcRestrictions* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="f9a70-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a70-114">O número de elementos na matriz de restrições.</span><span class="sxs-lookup"><span data-stu-id="f9a70-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="f9a70-115">Se *rgAnalogVideoRestrictions* for definido como **NULL**, esse valor será definido como o número de elementos necessários na matriz.</span><span class="sxs-lookup"><span data-stu-id="f9a70-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a70-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9a70-116">Return value</span></span>

<span data-ttu-id="f9a70-117">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f9a70-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f9a70-118">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f9a70-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f9a70-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f9a70-119">Return code</span></span>                                                                          | <span data-ttu-id="f9a70-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9a70-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f9a70-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9a70-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f9a70-122">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f9a70-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9a70-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9a70-123">Remarks</span></span>

<span data-ttu-id="f9a70-124">Você deve alocar memória para a matriz de restrições.</span><span class="sxs-lookup"><span data-stu-id="f9a70-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="f9a70-125">Para fazer isso, primeiro chame o método com *rgAnalogVideoRestrictions* definido como **NULL**, que definirá o valor em *pcRestrictions* como o número de elementos necessários.</span><span class="sxs-lookup"><span data-stu-id="f9a70-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a70-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9a70-126">Requirements</span></span>



| <span data-ttu-id="f9a70-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9a70-127">Requirement</span></span> | <span data-ttu-id="f9a70-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f9a70-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a70-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9a70-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f9a70-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a70-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9a70-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9a70-131">Library</span></span><br/> | <dl> <span data-ttu-id="f9a70-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9a70-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a70-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9a70-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a70-134">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="f9a70-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





