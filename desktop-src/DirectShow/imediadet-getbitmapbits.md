---
description: O método GetBitmapBits recupera um quadro de vídeo no tempo de mídia especificado. O quadro retornado sempre está no formato RGB de 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Método IMediaDet:: GetBitmapBits (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760741"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="28e2c-104">Método IMediaDet:: GetBitmapBits</span><span class="sxs-lookup"><span data-stu-id="28e2c-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="28e2c-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="28e2c-105">\[Deprecated.</span></span> <span data-ttu-id="28e2c-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28e2c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="28e2c-107">O `GetBitmapBits` método recupera um quadro de vídeo no tempo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="28e2c-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="28e2c-108">O quadro retornado sempre está no formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="28e2c-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e2c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28e2c-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="28e2c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28e2c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e2c-111">*Fluxo de transmissão*</span><span class="sxs-lookup"><span data-stu-id="28e2c-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="28e2c-112">Hora na qual recuperar o quadro de vídeo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="28e2c-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="28e2c-113">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="28e2c-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="28e2c-114">Recebe o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="28e2c-114">Receives the required buffer size.</span></span> <span data-ttu-id="28e2c-115">Se *pBuffer* for **NULL**, a variável receberá o tamanho do buffer necessário para recuperar o quadro.</span><span class="sxs-lookup"><span data-stu-id="28e2c-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="28e2c-116">Se *pBuffer* não for **NULL**, esse parâmetro será ignorado.</span><span class="sxs-lookup"><span data-stu-id="28e2c-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="28e2c-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="28e2c-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="28e2c-118">Ponteiro para um buffer que recebe uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguida pelos bits DIB.</span><span class="sxs-lookup"><span data-stu-id="28e2c-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="28e2c-119">*Largura*</span><span class="sxs-lookup"><span data-stu-id="28e2c-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="28e2c-120">Largura da imagem de vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="28e2c-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="28e2c-121">*Altura*</span><span class="sxs-lookup"><span data-stu-id="28e2c-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="28e2c-122">Altura da imagem de vídeo, em pixels.</span><span class="sxs-lookup"><span data-stu-id="28e2c-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e2c-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28e2c-123">Return value</span></span>

<span data-ttu-id="28e2c-124">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28e2c-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="28e2c-125">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="28e2c-125">Possible values include the following:</span></span>



| <span data-ttu-id="28e2c-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="28e2c-126">Return code</span></span>                                                                                             | <span data-ttu-id="28e2c-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="28e2c-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28e2c-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="28e2c-129">Êxito.</span><span class="sxs-lookup"><span data-stu-id="28e2c-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="28e2c-130"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="28e2c-131">Não foi possível adicionar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ao grafo.</span><span class="sxs-lookup"><span data-stu-id="28e2c-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="28e2c-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="28e2c-133">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="28e2c-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="28e2c-134"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="28e2c-135">Erro de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="28e2c-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="28e2c-136"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="28e2c-137">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="28e2c-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="28e2c-138"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="28e2c-139">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="28e2c-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="28e2c-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="28e2c-140">Remarks</span></span>

<span data-ttu-id="28e2c-141">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="28e2c-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="28e2c-142">Para determinar o tamanho do buffer que é necessário, chame esse método com *pBuffer* igual a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="28e2c-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="28e2c-143">O tamanho é retornado na variável apontada por *pBufferSize*.</span><span class="sxs-lookup"><span data-stu-id="28e2c-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="28e2c-144">Em seguida, crie o buffer e chame o método novamente, com *pBuffer* igual ao endereço do buffer.</span><span class="sxs-lookup"><span data-stu-id="28e2c-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="28e2c-145">Quando o método retorna, o buffer contém uma estrutura **BITMAPINFOHEADER** seguida pelo bitmap.</span><span class="sxs-lookup"><span data-stu-id="28e2c-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="28e2c-146">O bitmap é dimensionado para as dimensões especificadas nos parâmetros *Width* e *Height* .</span><span class="sxs-lookup"><span data-stu-id="28e2c-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="28e2c-147">Esse método coloca o detector de mídia no modo de captura de bitmap.</span><span class="sxs-lookup"><span data-stu-id="28e2c-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="28e2c-148">Depois que esse método for chamado, os vários métodos de informações de fluxo no **IMediaDet** não funcionarão, a menos que você crie uma nova instância do detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="28e2c-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="28e2c-149">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="28e2c-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="28e2c-150">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="28e2c-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="28e2c-151">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="28e2c-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="28e2c-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="28e2c-152">Examples</span></span>

<span data-ttu-id="28e2c-153">O código a seguir usa o `GetBitmapBits` método para criar um bitmap independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28e2c-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="28e2c-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28e2c-154">Requirements</span></span>



| <span data-ttu-id="28e2c-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="28e2c-155">Requirement</span></span> | <span data-ttu-id="28e2c-156">Valor</span><span class="sxs-lookup"><span data-stu-id="28e2c-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28e2c-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28e2c-157">Header</span></span><br/>  | <dl> <span data-ttu-id="28e2c-158"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="28e2c-159">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28e2c-159">Library</span></span><br/> | <dl> <span data-ttu-id="28e2c-160"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28e2c-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28e2c-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="28e2c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e2c-162">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="28e2c-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="28e2c-163">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="28e2c-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




