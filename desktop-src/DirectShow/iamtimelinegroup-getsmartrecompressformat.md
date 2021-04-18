---
description: O método GetSmartRecompressFormat recupera o formato de compactação atual para a recompactação inteligente.
ms.assetid: 2d420fe9-691d-4cc9-a8de-363a4be1b364
title: 'Método IAMTimelineGroup:: GetSmartRecompressFormat (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8560bb9d8da6904cf74b62ffd238b234e9c74ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760091"
---
# <a name="iamtimelinegroupgetsmartrecompressformat-method"></a><span data-ttu-id="4384b-103">Método IAMTimelineGroup:: GetSmartRecompressFormat</span><span class="sxs-lookup"><span data-stu-id="4384b-103">IAMTimelineGroup::GetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="4384b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4384b-104">\[Deprecated.</span></span> <span data-ttu-id="4384b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4384b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4384b-106">O `GetSmartRecompressFormat` método recupera o formato de compactação atual para a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="4384b-106">The `GetSmartRecompressFormat` method retrieves the current compression format for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="4384b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4384b-107">Syntax</span></span>


```C++
HRESULT GetSmartRecompressFormat(
   long **ppFormat
);
```



## <a name="parameters"></a><span data-ttu-id="4384b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4384b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4384b-109">*ppFormat*</span><span class="sxs-lookup"><span data-stu-id="4384b-109">*ppFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="4384b-110">Recebe um ponteiro para uma estrutura [**SCompFmt0**](scompfmt0.md) , convertida como um ponteiro para um longo.</span><span class="sxs-lookup"><span data-stu-id="4384b-110">Receives a pointer to an [**SCompFmt0**](scompfmt0.md) structure, cast as a pointer to a long.</span></span> <span data-ttu-id="4384b-111">Se o método falhar, o valor será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4384b-111">If the method fails, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4384b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4384b-112">Return value</span></span>

<span data-ttu-id="4384b-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4384b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4384b-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4384b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4384b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4384b-115">Remarks</span></span>

<span data-ttu-id="4384b-116">Se o aplicativo não tiver definido um formato de compactação inteligente (chamando [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), o formato retornado por esse método será inválido.</span><span class="sxs-lookup"><span data-stu-id="4384b-116">If the application has not set a smart compression format (by calling [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md)), the format returned by this method will be invalid.</span></span> <span data-ttu-id="4384b-117">Chame o método [**IAMTimelineGroup:: IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) para determinar se um formato de compactação foi definido.</span><span class="sxs-lookup"><span data-stu-id="4384b-117">Call the [**IAMTimelineGroup::IsSmartRecompressFormatSet**](iamtimelinegroup-issmartrecompressformatset.md) method to determine whether a compression format was set.</span></span>

<span data-ttu-id="4384b-118">Se o método for bem sucedido, o chamador deverá liberar o tipo de mídia retornado e excluir a estrutura [**SCompFmt0**](scompfmt0.md) :</span><span class="sxs-lookup"><span data-stu-id="4384b-118">If the method succeeds, the caller must free the returned media type and delete the [**SCompFmt0**](scompfmt0.md) structure:</span></span>


```C++
if (pFormat) {
    FreeMediaType(pFormat->MediaType);
    delete pFormat;
}
```



> [!Note]  
> <span data-ttu-id="4384b-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4384b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4384b-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4384b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4384b-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4384b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4384b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4384b-122">Requirements</span></span>



| <span data-ttu-id="4384b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4384b-123">Requirement</span></span> | <span data-ttu-id="4384b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4384b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4384b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4384b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4384b-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4384b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4384b-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4384b-127">Library</span></span><br/> | <dl> <span data-ttu-id="4384b-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4384b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4384b-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4384b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4384b-130">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="4384b-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="4384b-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="4384b-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




