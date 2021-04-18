---
description: Armazena internamente em cache a imagem não filtrada retornada do driver.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'Método IWiaPreview:: GetNewPreview (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798086"
---
# <a name="iwiapreviewgetnewpreview-method"></a><span data-ttu-id="06cfe-103">Método IWiaPreview:: GetNewPreview</span><span class="sxs-lookup"><span data-stu-id="06cfe-103">IWiaPreview::GetNewPreview method</span></span>

<span data-ttu-id="06cfe-104">Armazena internamente em cache a imagem não filtrada retornada do driver.</span><span class="sxs-lookup"><span data-stu-id="06cfe-104">Caches internally the unfiltered image returned from the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="06cfe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06cfe-105">Syntax</span></span>


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a><span data-ttu-id="06cfe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06cfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06cfe-107">*pWiaItem2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06cfe-107">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cfe-108">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="06cfe-108">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="06cfe-109">Especifica um ponteiro para o item [_ *IWiaItem2* \*](-wia-iwiaitem2.md) para a imagem.</span><span class="sxs-lookup"><span data-stu-id="06cfe-109">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for the image.</span></span>

</dd> <dt>

<span data-ttu-id="06cfe-110">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06cfe-110">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cfe-111">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="06cfe-111">Type: **LONG**</span></span>

<span data-ttu-id="06cfe-112">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="06cfe-112">Currently unused.</span></span> <span data-ttu-id="06cfe-113">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="06cfe-113">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="06cfe-114">*pWiaTransferCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06cfe-114">*pWiaTransferCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06cfe-115">Tipo: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _</span><span class="sxs-lookup"><span data-stu-id="06cfe-115">Type: \**[**IWiaTransferCallback**](-wia-iwiatransfercallback.md)\** _</span></span>

<span data-ttu-id="06cfe-116">Especifica um ponteiro para a interface [_ *IWiaTransferCallback* \*](-wia-iwiatransfercallback.md) do aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="06cfe-116">Specifies a pointer to the calling application's [_ *IWiaTransferCallback*\*](-wia-iwiatransfercallback.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06cfe-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06cfe-117">Return value</span></span>

<span data-ttu-id="06cfe-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="06cfe-118">Type: **HRESULT**</span></span>

<span data-ttu-id="06cfe-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="06cfe-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06cfe-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06cfe-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="06cfe-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="06cfe-121">Remarks</span></span>

<span data-ttu-id="06cfe-122">Um aplicativo deve chamar **IWiaPreview:: GetNewPreview** antes de chamar [**IWiaPreview::D etectregions**](-wia-iwiapreview-detectregions.md).</span><span class="sxs-lookup"><span data-stu-id="06cfe-122">An application must call **IWiaPreview::GetNewPreview** before it calls [**IWiaPreview::DetectRegions**](-wia-iwiapreview-detectregions.md).</span></span>

<span data-ttu-id="06cfe-123">**IWiaPreview:: GetNewPreview** define a propriedade de [**\_ \_ visualização do DPS do WIA**](-wia-wiaitempropscannerdevice.md) (e a redefine antes de retornar, a menos que tenha sido definido antes).</span><span class="sxs-lookup"><span data-stu-id="06cfe-123">**IWiaPreview::GetNewPreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="06cfe-124">Isso permite que o driver e o hardware, bem como o filtro de processamento de imagens, saibam que o item é uma verificação de visualização.</span><span class="sxs-lookup"><span data-stu-id="06cfe-124">This lets the driver and hardware, as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="06cfe-125">Internamente, o componente de versão prévia do WIA (Windows Image Acquisition) 2,0 cria uma instância do filtro de processamento de imagem do driver chamando [**GetExtension**](-wia-iwiaitem2-getextension.md) em *pWiaItem2*.</span><span class="sxs-lookup"><span data-stu-id="06cfe-125">Internally, the Windows Image Acquisition (WIA) 2.0 preview component creates an instance of the driver's image processing filter by calling [**GetExtension**](-wia-iwiaitem2-getextension.md) on *pWiaItem2*.</span></span> <span data-ttu-id="06cfe-126">O componente de visualização do WIA 2,0 faz isso quando o aplicativo chama **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="06cfe-126">The WIA 2.0 preview component does this when the application calls **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="06cfe-127">O componente de visualização do WIA 2,0 também Inicializa o filtro em **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="06cfe-127">The WIA 2.0 preview component also initializes the filter in **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="06cfe-128">A mesma instância de filtro é usada pelo componente de visualização do WIA 2,0 durante uma chamada para [**IWiaPreview:: UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span><span class="sxs-lookup"><span data-stu-id="06cfe-128">The same filter instance is used by the WIA 2.0 preview component during a call to [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md).</span></span>

<span data-ttu-id="06cfe-129">Antes de chamar o componente de visualização do WIA 2,0, um aplicativo deve chamar [**CheckExtension**](-wia-iwiaitem2-checkextension.md) para certificar-se de que o driver vem com um filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="06cfe-129">Before calling into the WIA 2.0 preview component, an application should call [**CheckExtension**](-wia-iwiaitem2-checkextension.md) to make sure that the driver comes with an image processing filter.</span></span> <span data-ttu-id="06cfe-130">Ele deve chamar **CheckExtension** no item que ele passaria para **IWiaPreview:: GetNewPreview**.</span><span class="sxs-lookup"><span data-stu-id="06cfe-130">It should call **CheckExtension** on the item that it would pass to **IWiaPreview::GetNewPreview**.</span></span> <span data-ttu-id="06cfe-131">É inútil fornecer visualizações dinâmicas sem um filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="06cfe-131">It is useless to provide live previews without an image processing filter.</span></span> <span data-ttu-id="06cfe-132">Se um aplicativo chamar **IWiaPreview:: GetNewPreview** para um driver sem um filtro de processamento de imagem, a chamada falhará.</span><span class="sxs-lookup"><span data-stu-id="06cfe-132">If an application calls **IWiaPreview::GetNewPreview** for a driver without an image processing filter, the call will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="06cfe-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="06cfe-133">Examples</span></span>

<span data-ttu-id="06cfe-134">CheckImgFilter verifica se o driver tem um filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="06cfe-134">CheckImgFilter checks if the driver has an image processing filter.</span></span> <span data-ttu-id="06cfe-135">Antes de chamar o componente de visualização, um aplicativo deve garantir que o driver tenha um filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="06cfe-135">Before calling into the preview component, an application should ensure that the driver has an image processing filter.</span></span>


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



<span data-ttu-id="06cfe-136">O DownloadPreviewImage baixa dados de imagem do scanner chamando o método **IWiaPreview:: GetNewPreview** do componente de visualização.</span><span class="sxs-lookup"><span data-stu-id="06cfe-136">DownloadPreviewImage downloads image data from the scanner by calling the preview component's **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="06cfe-137">Em seguida, ele chama DetectSubregions se o usuário do aplicativo quiser invocar o filtro de segmentação, que cria um item filho em pWiaItem2 para cada região detectada.</span><span class="sxs-lookup"><span data-stu-id="06cfe-137">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="06cfe-138">Consulte [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) para o método DetectSubregions usado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="06cfe-138">See [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="06cfe-139">Neste exemplo, o usuário do aplicativo define `m_bUseSegmentationFilter` clicando em uma caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="06cfe-139">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="06cfe-140">Se o aplicativo der suporte a isso, primeiro verifique se o driver tem um filtro de segmentação chamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="06cfe-140">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="06cfe-141">Consulte **IWiaPreview:: GetNewPreview** para obter o exemplo do método CheckImgFilter que mostra como isso pode ser feito.</span><span class="sxs-lookup"><span data-stu-id="06cfe-141">See **IWiaPreview::GetNewPreview** for the CheckImgFilter method example that shows how this can be done.</span></span>


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="06cfe-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06cfe-142">Requirements</span></span>



| <span data-ttu-id="06cfe-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="06cfe-143">Requirement</span></span> | <span data-ttu-id="06cfe-144">Valor</span><span class="sxs-lookup"><span data-stu-id="06cfe-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06cfe-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06cfe-145">Minimum supported client</span></span><br/> | <span data-ttu-id="06cfe-146">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="06cfe-146">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="06cfe-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="06cfe-147">Minimum supported server</span></span><br/> | <span data-ttu-id="06cfe-148">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="06cfe-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="06cfe-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06cfe-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="06cfe-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="06cfe-150"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="06cfe-151">INSERI</span><span class="sxs-lookup"><span data-stu-id="06cfe-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06cfe-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="06cfe-152"><dt>Wia.idl</dt></span></span> </dl> |



 

 




