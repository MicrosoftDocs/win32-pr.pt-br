---
description: O \_ método de filtro Put especifica um filtro de origem para o detector de mídia a ser usado.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: 'IMediaDet: método de ut_Filter de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789935"
---
# <a name="imediadetput_filter-method"></a><span data-ttu-id="8da40-103">Método de filtro IMediaDet::p UT \_</span><span class="sxs-lookup"><span data-stu-id="8da40-103">IMediaDet::put\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="8da40-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8da40-104">\[Deprecated.</span></span> <span data-ttu-id="8da40-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8da40-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8da40-106">O `put_Filter` método especifica um filtro de origem para o detector de mídia a ser usado.</span><span class="sxs-lookup"><span data-stu-id="8da40-106">The `put_Filter` method specifies a source filter for the media detector to use.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8da40-107">Não adicione o filtro de origem ao seu próprio grafo de filtro ou use um filtro que já esteja em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="8da40-107">Do not add the source filter to your own filter graph, or use a filter that is already in a filter graph.</span></span> <span data-ttu-id="8da40-108">O objeto do detector de mídia cria automaticamente um gráfico de filtro interno e colocar o filtro em outro grafo pode causar resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="8da40-108">The media detector object automatically builds an internal filter graph, and putting the filter in another graph can cause unexpected results.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8da40-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8da40-109">Syntax</span></span>


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="8da40-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8da40-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da40-111">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8da40-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8da40-112">Ponteiro para a interface **IUnknown** do filtro de origem.</span><span class="sxs-lookup"><span data-stu-id="8da40-112">Pointer to the source filter's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8da40-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8da40-113">Return value</span></span>

<span data-ttu-id="8da40-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8da40-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8da40-115">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="8da40-115">Possible values include the following:</span></span>



| <span data-ttu-id="8da40-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8da40-116">Return code</span></span>                                                                                   | <span data-ttu-id="8da40-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="8da40-117">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="8da40-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8da40-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8da40-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8da40-119">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="8da40-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="8da40-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="8da40-121">*newVal* não aponta para um filtro.</span><span class="sxs-lookup"><span data-stu-id="8da40-121">*newVal* does not point to a filter.</span></span><br/> |
| <dl> <span data-ttu-id="8da40-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="8da40-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8da40-123">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="8da40-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="8da40-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="8da40-124">Remarks</span></span>

<span data-ttu-id="8da40-125">Para a maioria dos aplicativos, é mais simples chamar o método [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) com o nome de um arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="8da40-125">For most applications, it is simpler to call the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method with the name of a source file.</span></span>

> [!Note]  
> <span data-ttu-id="8da40-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8da40-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8da40-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8da40-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8da40-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8da40-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8da40-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da40-129">Requirements</span></span>



| <span data-ttu-id="8da40-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da40-130">Requirement</span></span> | <span data-ttu-id="8da40-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8da40-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8da40-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8da40-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8da40-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8da40-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8da40-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8da40-134">Library</span></span><br/> | <dl> <span data-ttu-id="8da40-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8da40-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da40-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8da40-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da40-137">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="8da40-137">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="8da40-138">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="8da40-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




