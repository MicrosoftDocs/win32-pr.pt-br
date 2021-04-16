---
description: O \_ método obter filtro recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.
ms.assetid: 23d603c1-445d-425a-973e-7bfe0a2d19f2
title: 'Método IMediaDet:: get_Filter (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f80b5d5021ca7f04cd56dc319fb5416c3361108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782232"
---
# <a name="imediadetget_filter-method"></a><span data-ttu-id="f76dd-103">Método de filtro IMediaDet:: get \_</span><span class="sxs-lookup"><span data-stu-id="f76dd-103">IMediaDet::get\_Filter method</span></span>

> [!Note]  
> <span data-ttu-id="f76dd-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f76dd-104">\[Deprecated.</span></span> <span data-ttu-id="f76dd-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f76dd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f76dd-106">O `get_Filter` método recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="f76dd-106">The `get_Filter` method retrieves a pointer to the source filter currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76dd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f76dd-107">Syntax</span></span>


```C++
HRESULT get_Filter(
  [out, retval] IUnknown **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="f76dd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f76dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f76dd-109">*ppVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f76dd-109">*ppVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f76dd-110">Recebe um ponteiro para a interface **IUnknown** do filtro.</span><span class="sxs-lookup"><span data-stu-id="f76dd-110">Receives a pointer to the filter's **IUnknown** interface.</span></span> <span data-ttu-id="f76dd-111">Se nenhum filtro de origem estiver em uso, o valor será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f76dd-111">If no source filter is in use, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f76dd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f76dd-112">Return value</span></span>

<span data-ttu-id="f76dd-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f76dd-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f76dd-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f76dd-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f76dd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f76dd-115">Remarks</span></span>

<span data-ttu-id="f76dd-116">Quando o método retornar, se *\* ppVal* não for **NULL**, a interface **IUnknown** terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="f76dd-116">When the method returns, if *\*ppVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="f76dd-117">Libere a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="f76dd-117">Release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="f76dd-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f76dd-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f76dd-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f76dd-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f76dd-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f76dd-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f76dd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f76dd-121">Requirements</span></span>



| <span data-ttu-id="f76dd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f76dd-122">Requirement</span></span> | <span data-ttu-id="f76dd-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f76dd-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f76dd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f76dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f76dd-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f76dd-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f76dd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f76dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="f76dd-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f76dd-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f76dd-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f76dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76dd-129">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="f76dd-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="f76dd-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f76dd-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




