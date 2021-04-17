---
description: O \_ método Get MediaType retorna o tipo de mídia de saída atual do filtro de redimensionador.
ms.assetid: b9900f7c-05f6-47e4-9cb0-683df2aea404
title: 'Método IResize:: get_MediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b03bad7f8686fd580f7dd5fc347c347ade1c1c97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759533"
---
# <a name="iresizeget_mediatype-method"></a><span data-ttu-id="861c8-103">Método IResize:: get \_ MediaType</span><span class="sxs-lookup"><span data-stu-id="861c8-103">IResize::get\_MediaType method</span></span>

> [!Note]  
> <span data-ttu-id="861c8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="861c8-104">\[Deprecated.</span></span> <span data-ttu-id="861c8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="861c8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="861c8-106">O `get_MediaType` método retorna o tipo de mídia de saída atual do filtro de redimensionador.</span><span class="sxs-lookup"><span data-stu-id="861c8-106">The `get_MediaType` method returns the resizer filter's current output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="861c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="861c8-107">Syntax</span></span>


```C++
HRESULT get_MediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="861c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="861c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="861c8-109">*PGTO* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="861c8-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="861c8-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) alocada pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="861c8-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure allocated by the caller.</span></span> <span data-ttu-id="861c8-111">O método preenche essa estrutura com o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="861c8-111">The method fills this structure with the media type.</span></span> <span data-ttu-id="861c8-112">O chamador deve liberar o bloco de formato, se houver.</span><span class="sxs-lookup"><span data-stu-id="861c8-112">The caller must release the format block, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="861c8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="861c8-113">Return value</span></span>

<span data-ttu-id="861c8-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="861c8-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="861c8-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="861c8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="861c8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="861c8-116">Remarks</span></span>

<span data-ttu-id="861c8-117">Se o tipo de mídia de saída não tiver sido definido, retorne um tipo de mídia padrão.</span><span class="sxs-lookup"><span data-stu-id="861c8-117">If the output media type has not been set, return a default media type.</span></span> <span data-ttu-id="861c8-118">O filtro deve atualizar seu tipo de mídia de saída quando os métodos **Put \_ MediaType** ou **Put \_ size** são chamados; o tipo de mídia retornado por `get_MediaType` deve refletir essas alterações.</span><span class="sxs-lookup"><span data-stu-id="861c8-118">The filter must update its output media type when the **put\_MediaType** or **put\_Size** methods are called; the media type returned by `get_MediaType` must reflect these changes.</span></span>

> [!Note]  
> <span data-ttu-id="861c8-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="861c8-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="861c8-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="861c8-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="861c8-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="861c8-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="861c8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="861c8-122">Requirements</span></span>



| <span data-ttu-id="861c8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="861c8-123">Requirement</span></span> | <span data-ttu-id="861c8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="861c8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="861c8-125">Versão</span><span class="sxs-lookup"><span data-stu-id="861c8-125">Version</span></span><br/> | <span data-ttu-id="861c8-126">DirectX 9,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="861c8-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="861c8-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="861c8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="861c8-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="861c8-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="861c8-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="861c8-129">Library</span></span><br/> | <dl> <span data-ttu-id="861c8-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="861c8-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="861c8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="861c8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="861c8-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="861c8-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="861c8-133">**Interface IResize**</span><span class="sxs-lookup"><span data-stu-id="861c8-133">**IResize Interface**</span></span>](iresize.md)
</dt> </dl>

 

 




