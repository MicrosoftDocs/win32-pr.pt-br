---
description: O método GetMediaType recupera o tipo de mídia descompactado para o grupo.
ms.assetid: 129ed688-0f03-4ccb-b65f-d61f02cb94b2
title: 'Método IAMTimelineGroup:: GetMediaType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2122b5429ffa66d278ccfe59553ac85fb0dee562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770074"
---
# <a name="iamtimelinegroupgetmediatype-method"></a><span data-ttu-id="994d3-103">Método IAMTimelineGroup:: GetMediaType</span><span class="sxs-lookup"><span data-stu-id="994d3-103">IAMTimelineGroup::GetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="994d3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="994d3-104">\[Deprecated.</span></span> <span data-ttu-id="994d3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="994d3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="994d3-106">O `GetMediaType` método recupera o tipo de mídia descompactado para o grupo.</span><span class="sxs-lookup"><span data-stu-id="994d3-106">The `GetMediaType` method retrieves the uncompressed media type for the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="994d3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="994d3-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
  [out] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="994d3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="994d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="994d3-109">*PGTO* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="994d3-109">*pmt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="994d3-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que é preenchida com o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="994d3-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that is filled with the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="994d3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="994d3-111">Return value</span></span>

<span data-ttu-id="994d3-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="994d3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="994d3-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="994d3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="994d3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="994d3-114">Remarks</span></span>

<span data-ttu-id="994d3-115">O chamador deve liberar o bloco de formato do tipo de mídia retornado, fornecido no membro **pbFormat** da estrutura do \_ tipo de mídia retornado \_ .</span><span class="sxs-lookup"><span data-stu-id="994d3-115">The caller must free the returned media type's format block, given in the **pbFormat** member of the returned AM\_MEDIA\_TYPE structure.</span></span> <span data-ttu-id="994d3-116">Você pode usar a função auxiliar [**FreeMediaType**](freemediatype.md) da biblioteca de classes base.</span><span class="sxs-lookup"><span data-stu-id="994d3-116">You can use the helper function [**FreeMediaType**](freemediatype.md) from the base class library.</span></span>

> [!Note]  
> <span data-ttu-id="994d3-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="994d3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="994d3-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="994d3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="994d3-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="994d3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="994d3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="994d3-120">Requirements</span></span>



| <span data-ttu-id="994d3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="994d3-121">Requirement</span></span> | <span data-ttu-id="994d3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="994d3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="994d3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="994d3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="994d3-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="994d3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="994d3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="994d3-125">Library</span></span><br/> | <dl> <span data-ttu-id="994d3-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="994d3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="994d3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="994d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994d3-128">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="994d3-128">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="994d3-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="994d3-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




