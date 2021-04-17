---
description: O \_ método Get StreamTypeB recupera uma cadeia de caracteres que representa o GUID do tipo de mídia para o fluxo atual.
ms.assetid: 99ae4b52-4449-4b7c-babf-1a6cba479499
title: 'Método IMediaDet:: get_StreamTypeB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamTypeB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd1cdf4bbadfa769654f20792cf2fda17dbe2806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754762"
---
# <a name="imediadetget_streamtypeb-method"></a><span data-ttu-id="04bcc-103">Método IMediaDet:: get \_ StreamTypeB</span><span class="sxs-lookup"><span data-stu-id="04bcc-103">IMediaDet::get\_StreamTypeB method</span></span>

> [!Note]  
> <span data-ttu-id="04bcc-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="04bcc-104">\[Deprecated.</span></span> <span data-ttu-id="04bcc-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="04bcc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="04bcc-106">O `get_StreamTypeB` método recupera uma cadeia de caracteres que representa o GUID do tipo de mídia para o fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="04bcc-106">The `get_StreamTypeB` method retrieves a string representing the GUID of the media type for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="04bcc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04bcc-107">Syntax</span></span>


```C++
HRESULT get_StreamTypeB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="04bcc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04bcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04bcc-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="04bcc-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="04bcc-110">Recebe uma representação de cadeia de caracteres do GUID do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="04bcc-110">Receives a string representation of the media type GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04bcc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04bcc-111">Return value</span></span>

<span data-ttu-id="04bcc-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="04bcc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04bcc-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04bcc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04bcc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="04bcc-114">Remarks</span></span>

<span data-ttu-id="04bcc-115">O **BSTR** retornado é formatado da seguinte maneira: `{73647561-0000-0010-8000-00AA00389B71}`</span><span class="sxs-lookup"><span data-stu-id="04bcc-115">The returned **BSTR** is formatted like the following: `{73647561-0000-0010-8000-00AA00389B71}`</span></span>

<span data-ttu-id="04bcc-116">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="04bcc-116">The method allocates memory for the string.</span></span> <span data-ttu-id="04bcc-117">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="04bcc-117">The application must call **SysFreeString** to free the memory.</span></span>

<span data-ttu-id="04bcc-118">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="04bcc-118">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="04bcc-119">Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="04bcc-119">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="04bcc-120">Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="04bcc-120">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="04bcc-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="04bcc-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="04bcc-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="04bcc-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="04bcc-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="04bcc-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="04bcc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04bcc-124">Requirements</span></span>



| <span data-ttu-id="04bcc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="04bcc-125">Requirement</span></span> | <span data-ttu-id="04bcc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="04bcc-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04bcc-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04bcc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="04bcc-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="04bcc-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="04bcc-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04bcc-129">Library</span></span><br/> | <dl> <span data-ttu-id="04bcc-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04bcc-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04bcc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="04bcc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04bcc-132">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="04bcc-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="04bcc-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="04bcc-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




