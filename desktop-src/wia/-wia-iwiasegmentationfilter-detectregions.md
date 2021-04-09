---
description: Determina as subregiãos de uma imagem disposta no cilindro de mesa para que cada sub-região possa ser adquirida em um item de imagem separado.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: 'IWiaSegmentationFilter: método etectRegions de:D (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090504"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a><span data-ttu-id="1a15e-103">IWiaSegmentationFilter: método etectRegions de:D</span><span class="sxs-lookup"><span data-stu-id="1a15e-103">IWiaSegmentationFilter::DetectRegions method</span></span>

<span data-ttu-id="1a15e-104">Determina as subregiãos de uma imagem disposta no cilindro de mesa para que cada sub-região possa ser adquirida em um item de imagem separado.</span><span class="sxs-lookup"><span data-stu-id="1a15e-104">Determines the sub-regions of an image laid out on the flatbed platen so that each of sub-region can be acquired into a separate image item.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a15e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a15e-105">Syntax</span></span>


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="1a15e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a15e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a15e-107">*lFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a15e-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a15e-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="1a15e-108">Type: **LONG**</span></span>

<span data-ttu-id="1a15e-109">Atualmente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="1a15e-109">Currently unused.</span></span> <span data-ttu-id="1a15e-110">Deve ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="1a15e-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="1a15e-111">*pInputStream* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a15e-111">*pInputStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a15e-112">Tipo: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="1a15e-112">Type: \**[IStream](/windows/win32/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="1a15e-113">Especifica um ponteiro para a imagem de visualização de [IStream](/windows/win32/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="1a15e-113">Specifies a pointer to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) preview image.</span></span>

</dd> <dt>

<span data-ttu-id="1a15e-114">_pWiaItem2 \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1a15e-114">_pWiaItem2\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a15e-115">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="1a15e-115">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="1a15e-116">Especifica um ponteiro para o item [_ *IWiaItem2* \*](-wia-iwiaitem2.md) para o qual *pInputStream* foi adquirido.</span><span class="sxs-lookup"><span data-stu-id="1a15e-116">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item for which *pInputStream* was acquired.</span></span> <span data-ttu-id="1a15e-117">O filtro de segmentação cria itens filho para este item.</span><span class="sxs-lookup"><span data-stu-id="1a15e-117">The segmentation filter creates child items for this item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a15e-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a15e-118">Return value</span></span>

<span data-ttu-id="1a15e-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1a15e-119">Type: **HRESULT**</span></span>

<span data-ttu-id="1a15e-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a15e-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a15e-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a15e-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a15e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a15e-122">Remarks</span></span>

<span data-ttu-id="1a15e-123">Esse método determina as subregiãos da imagem representadas por pInputStream.</span><span class="sxs-lookup"><span data-stu-id="1a15e-123">This method determines the sub-regions of the image represented by pInputStream.</span></span> <span data-ttu-id="1a15e-124">Para cada sub-região detectada, ela cria um item filho para o item [**IWiaItem2**](-wia-iwiaitem2.md) especificado no parâmetro *pWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="1a15e-124">For each sub-region that it detects, it creates a child item for the [**IWiaItem2**](-wia-iwiaitem2.md) item specified in the *pWiaItem2* parameter.</span></span> <span data-ttu-id="1a15e-125">Para cada item filho, o filtro de segmentação deve definir valores para o retângulo delimitador da área a ser verificada, usando as seguintes [**constantes de propriedade de item WIA do scanner**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="1a15e-125">For each child item, the segmentation filter must set values for the bounding rectangle of the area to scan, using the following [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

-   [<span data-ttu-id="1a15e-126">**\_XPos IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="1a15e-126">**WIA\_IPS\_XPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="1a15e-127">**\_YPos IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="1a15e-127">**WIA\_IPS\_YPOS**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="1a15e-128">**\_XEXTENT IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="1a15e-128">**WIA\_IPS\_XEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)
-   [<span data-ttu-id="1a15e-129">**\_YEXTENT IPS \_ WIA**</span><span class="sxs-lookup"><span data-stu-id="1a15e-129">**WIA\_IPS\_YEXTENT**</span></span>](-wia-wiaitempropscanneritem.md)

<span data-ttu-id="1a15e-130">Um filtro mais avançado também pode exigir outras [**constantes de propriedade de item WIA do scanner**](-wia-wiaitempropscanneritem.md) , como os **IPS WIA \_ distorção \_ \_ X** e **WIA \_ IPS de \_ istorção \_ Y**, se o driver oferecer suporte a distorção.</span><span class="sxs-lookup"><span data-stu-id="1a15e-130">A more advanced filter may also require other [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md) such as **WIA\_IPS\_DESKEW\_X** and **WIA\_IPS\_DESKEW\_Y**, if the driver supports de-skewing.</span></span>

<span data-ttu-id="1a15e-131">Se o aplicativo chamar **IWiaSegmentationFilter::D etectregions** mais de uma vez, o aplicativo deverá primeiro excluir os itens filho criados pela última chamada para **IWiaSegmentationFilter::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="1a15e-131">If the application calls **IWiaSegmentationFilter::DetectRegions** more than once, the application must first delete the child items created by the last call to **IWiaSegmentationFilter::DetectRegions**.</span></span>

<span data-ttu-id="1a15e-132">Se um aplicativo alterar as propriedades para *pWiaItem2*, entre adquirir a imagem em *pInputStream* e sua chamada para **IWiaSegmentationFilter::D etectregions**, as propriedades originais (ou seja, as propriedades que o item tinha quando o fluxo foi adquirido) devem ser restauradas.</span><span class="sxs-lookup"><span data-stu-id="1a15e-132">If an application changes any properties into *pWiaItem2*, between acquiring the image into *pInputStream* and its call to **IWiaSegmentationFilter::DetectRegions**, the original properties (that is, the properties the item had when the stream was acquired) must be restored.</span></span> <span data-ttu-id="1a15e-133">Isso pode ser feito por [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span><span class="sxs-lookup"><span data-stu-id="1a15e-133">This can be done by [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) and [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream).</span></span>

<span data-ttu-id="1a15e-134">O aplicativo deverá redefinir o [IStream](/windows/win32/api/objidl/nn-objidl-istream) se sua chamada passar o mesmo fluxo para o filtro de segmentação mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="1a15e-134">The application must reset the [IStream](/windows/win32/api/objidl/nn-objidl-istream) if its call passes the same stream into the segmentation filter more than once.</span></span> <span data-ttu-id="1a15e-135">O aplicativo também deve redefinir o fluxo após o download inicial e antes de chamar **IWiaSegmentationFilter::D etectregions**.</span><span class="sxs-lookup"><span data-stu-id="1a15e-135">The application must also reset the stream after the initial download and before calling **IWiaSegmentationFilter::DetectRegions**.</span></span>

## <a name="examples"></a><span data-ttu-id="1a15e-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a15e-136">Examples</span></span>

<span data-ttu-id="1a15e-137">A segmentação executa a detecção de região no fluxo ( `pImageStream` ) passado para DetectSubregions.</span><span class="sxs-lookup"><span data-stu-id="1a15e-137">The segmentation performs region detection on the stream (`pImageStream`) passed into DetectSubregions.</span></span> <span data-ttu-id="1a15e-138">Consulte o método [**GetExtension**](-wia-iwiaitem2-getextension.md) para CreateSegmentationFilter usado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="1a15e-138">See the [**GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter method used in this example.</span></span>


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



<span data-ttu-id="1a15e-139">O DownloadPreviewImage baixa dados de imagem do scanner chamando o método [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) do componente de visualização.</span><span class="sxs-lookup"><span data-stu-id="1a15e-139">DownloadPreviewImage downloads image data from the scanner by calling the preview component's [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="1a15e-140">Em seguida, ele chama DetectSubregions se o usuário do aplicativo quiser invocar o filtro de segmentação, que cria um item filho em pWiaItem2 para cada região detectada.</span><span class="sxs-lookup"><span data-stu-id="1a15e-140">It then calls DetectSubregions if the application user wants to invoke the segmentation filter, which creates a child item under pWiaItem2 for each region it detects.</span></span> <span data-ttu-id="1a15e-141">Consulte **IWiaSegmentationFilter::D etectregions** para o método DetectSubregions usado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="1a15e-141">See **IWiaSegmentationFilter::DetectRegions** for the DetectSubregions method used in this example.</span></span>

<span data-ttu-id="1a15e-142">Neste exemplo, o usuário do aplicativo define `m_bUseSegmentationFilter` clicando em uma caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="1a15e-142">In this example, the application user sets `m_bUseSegmentationFilter` by clicking a check box.</span></span> <span data-ttu-id="1a15e-143">Se o aplicativo der suporte a isso, primeiro verifique se o driver tem um filtro de segmentação chamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span><span class="sxs-lookup"><span data-stu-id="1a15e-143">If the application supports this, it should first check that the driver has a segmentation filter by calling [**CheckExtension**](-wia-iwiaitem2-checkextension.md).</span></span> <span data-ttu-id="1a15e-144">Consulte [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para o exemplo do método CheckImgFilter que mostra como isso pode ser feito.</span><span class="sxs-lookup"><span data-stu-id="1a15e-144">See [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) for the CheckImgFilter method example that shows how this can be done.</span></span>


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
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
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
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="1a15e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a15e-145">Requirements</span></span>



| <span data-ttu-id="1a15e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a15e-146">Requirement</span></span> | <span data-ttu-id="1a15e-147">Valor</span><span class="sxs-lookup"><span data-stu-id="1a15e-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a15e-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a15e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="1a15e-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a15e-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1a15e-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a15e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="1a15e-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a15e-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1a15e-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a15e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a15e-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a15e-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1a15e-154">INSERI</span><span class="sxs-lookup"><span data-stu-id="1a15e-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a15e-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a15e-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 
