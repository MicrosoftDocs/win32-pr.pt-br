---
description: O \_ método Put size define o tamanho de saída e o modo Stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize: método de ut_Size de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783383"
---
# <a name="iresizeput_size-method"></a><span data-ttu-id="a796a-103">IResize: método de tamanho de UT:p \_</span><span class="sxs-lookup"><span data-stu-id="a796a-103">IResize::put\_Size method</span></span>

> [!Note]  
> <span data-ttu-id="a796a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a796a-104">\[Deprecated.</span></span> <span data-ttu-id="a796a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a796a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a796a-106">O `put_Size` método define o tamanho de saída e o modo de ampliação.</span><span class="sxs-lookup"><span data-stu-id="a796a-106">The `put_Size` method sets the output size and stretch mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a796a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a796a-107">Syntax</span></span>


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a796a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a796a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a796a-109">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a796a-109">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a796a-110">A altura do vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a796a-110">The video height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a796a-111">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a796a-111">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a796a-112">A largura do vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="a796a-112">The video width, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a796a-113">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a796a-113">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a796a-114">O modo de ampliação.</span><span class="sxs-lookup"><span data-stu-id="a796a-114">The stretch mode.</span></span> <span data-ttu-id="a796a-115">Consulte [**redimensionar sinalizadores**](resize-flags.md) para obter os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a796a-115">See [**Resize Flags**](resize-flags.md) for possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a796a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a796a-116">Return value</span></span>

<span data-ttu-id="a796a-117">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a796a-117">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a796a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a796a-118">Remarks</span></span>

<span data-ttu-id="a796a-119">O DES pode chamar esse método antes ou depois de chamar **Put \_ MediaType**.</span><span class="sxs-lookup"><span data-stu-id="a796a-119">DES may call this method before or after calling **put\_MediaType**.</span></span> <span data-ttu-id="a796a-120">Se o DES chamar esse método antes de chamar **Put \_ MediaType**, o filtro deverá selecionar um valor padrão para a profundidade de bits e usar os valores de tamanho para construir um tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="a796a-120">If DES calls this method before calling **put\_MediaType**, the filter should select a default value for the bit depth and use the size values to construct an output media type.</span></span> <span data-ttu-id="a796a-121">Se o DES chamar esse método depois de chamar **Put \_ MediaType**, o filtro deverá modificar seu tipo de saída atual com os novos tamanhos.</span><span class="sxs-lookup"><span data-stu-id="a796a-121">If DES calls this method after calling **put\_MediaType**, the filter should modify its current output type with the new sizes.</span></span>

<span data-ttu-id="a796a-122">O DES também pode chamar esse método depois que o pino de saída estiver conectado.</span><span class="sxs-lookup"><span data-stu-id="a796a-122">DES may also call this method after the output pin is connected.</span></span> <span data-ttu-id="a796a-123">Nesse caso, modifique o tipo de saída e reconecte o pino de saída com o novo tipo.</span><span class="sxs-lookup"><span data-stu-id="a796a-123">In that case, modify the output type and reconnect the output pin with the new type.</span></span> <span data-ttu-id="a796a-124">Consulte [reconectando Pins](reconnecting-pins.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="a796a-124">See [Reconnecting Pins](reconnecting-pins.md) for more information.</span></span>

<span data-ttu-id="a796a-125">O parâmetro *flags* especifica como o filtro deve executar a operação de redimensionamento.</span><span class="sxs-lookup"><span data-stu-id="a796a-125">The *Flags* parameter specifies how the filter should perform the resizing operation.</span></span>

> [!Note]  
> <span data-ttu-id="a796a-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a796a-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a796a-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a796a-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a796a-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a796a-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a796a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a796a-129">Requirements</span></span>



| <span data-ttu-id="a796a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="a796a-130">Requirement</span></span> | <span data-ttu-id="a796a-131">Valor</span><span class="sxs-lookup"><span data-stu-id="a796a-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a796a-132">Versão</span><span class="sxs-lookup"><span data-stu-id="a796a-132">Version</span></span><br/> | <span data-ttu-id="a796a-133">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="a796a-133">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="a796a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a796a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="a796a-135"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a796a-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a796a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a796a-136">Library</span></span><br/> | <dl> <span data-ttu-id="a796a-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a796a-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a796a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a796a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a796a-139">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="a796a-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="a796a-140">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="a796a-140">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




