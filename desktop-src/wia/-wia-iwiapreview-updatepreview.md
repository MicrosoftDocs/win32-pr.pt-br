---
description: 'Obtém a imagem não filtrada armazenada em cache pelo método IWiaPreview:: GetNewPreview.'
ms.assetid: 121b6866-cca1-4170-9bdf-225491f942f5
title: 'Método IWiaPreview:: UpdatePreview (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.UpdatePreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 4a5d469179f341f3bad5d2b9b5ed25a5715be694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090505"
---
# <a name="iwiapreviewupdatepreview-method"></a><span data-ttu-id="96b68-103">Método IWiaPreview:: UpdatePreview</span><span class="sxs-lookup"><span data-stu-id="96b68-103">IWiaPreview::UpdatePreview method</span></span>

<span data-ttu-id="96b68-104">Obtém a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="96b68-104">Gets the unfiltered image cached by the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b68-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96b68-105">Syntax</span></span>


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a><span data-ttu-id="96b68-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96b68-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96b68-107">*lOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96b68-107">*lOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b68-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="96b68-108">Type: **LONG**</span></span>

<span data-ttu-id="96b68-109">Especifica se o aplicativo requer que o componente de visualização do WIA 2,0 passe uma sub-região da imagem armazenada em cache ou toda a imagem armazenada em cache para o filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="96b68-109">Specifies whether the application requires the WIA 2.0 Preview Component to pass a sub-region of the cached image or the entire cached image to the image processing filter.</span></span>

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span data-ttu-id="96b68-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span><span class="sxs-lookup"><span data-stu-id="96b68-110"><span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**</span></span>


</dt> <dd>

<span data-ttu-id="96b68-111">Passe toda a imagem armazenada em cache para o filtro de processamento de imagem.</span><span class="sxs-lookup"><span data-stu-id="96b68-111">Pass the entire cached image to the image processing filter.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="96b68-112">*pChildWiaItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96b68-112">*pChildWiaItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96b68-113">Tipo: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="96b68-113">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="96b68-114">Especifica um ponteiro para o [Item _ *IWiaItem2* \*](-wia-iwiaitem2.md) , que é um filho do item **IWiaItem2** especificado pelo parâmetro *pWiaItem2* do método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .</span><span class="sxs-lookup"><span data-stu-id="96b68-114">Specifies a pointer to the [_ *IWiaItem2*\*](-wia-iwiaitem2.md) item, which is a child of the **IWiaItem2** item specified by the *pWiaItem2* parameter of the [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) method.</span></span> <span data-ttu-id="96b68-115">Ou, se o aplicativo exigir uma visualização da mesa inteira, especificará um ponteiro para o parâmetro *pWiaItem2* do método **IWiaPreview:: GetNewPreview** .</span><span class="sxs-lookup"><span data-stu-id="96b68-115">Or, if the application requires a preview of the whole flatbed, specifies a pointer to the *pWiaItem2* parameter of the **IWiaPreview::GetNewPreview** method.</span></span> <span data-ttu-id="96b68-116">Quando *pChildWiaItem* é um filho do parâmetro *pWiaItem2* **IWiaPreview:: GetNewPreview**, esse item filho normalmente é criado pelo filtro de segmentação.</span><span class="sxs-lookup"><span data-stu-id="96b68-116">When *pChildWiaItem* is a child of **IWiaPreview::GetNewPreview**'s *pWiaItem2* parameter, this child item is typically created by the segmentation filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96b68-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96b68-117">Return value</span></span>

<span data-ttu-id="96b68-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="96b68-118">Type: **HRESULT**</span></span>

<span data-ttu-id="96b68-119">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="96b68-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96b68-120">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="96b68-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96b68-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="96b68-121">Remarks</span></span>

<span data-ttu-id="96b68-122">Esse método passa a imagem armazenada em cache e não filtrada por meio do filtro de processamento de imagem, que grava os dados filtrados no fluxo fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96b68-122">This method passes the cached, unfiltered image through the image processing filter, which then writes the filtered data to the application-provided stream.</span></span> <span data-ttu-id="96b68-123">O componente de visualização do WIA 2,0 recupera esse fluxo chamando o método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) do filtro de processamento de imagens, que chama a implementação **GetNextStream** do retorno de chamada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96b68-123">The WIA 2.0 Preview Component retrieves this stream by calling the image processing filter's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method, which then calls the application callback's **GetNextStream** implementation.</span></span> <span data-ttu-id="96b68-124">Antes de chamar **IWiaPreview:: UpdatePreview**, um aplicativo deve primeiro chamar [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para adquirir a imagem do scanner; caso contrário, o método retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="96b68-124">Before calling **IWiaPreview::UpdatePreview**, an application must first call [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) to acquire the image from the scanner; otherwise, the method returns an error.</span></span>

<span data-ttu-id="96b68-125">O componente de visualização do WIA 2,0 armazena a imagem não filtrada baixada do driver.</span><span class="sxs-lookup"><span data-stu-id="96b68-125">The WIA 2.0 Preview Component stores the unfiltered image downloaded from the driver.</span></span> <span data-ttu-id="96b68-126">É possível que o item 2,0 do WIA passado para **IWiaPreview:: UpdatePreview** represente apenas uma pequena região da imagem baixada do driver.</span><span class="sxs-lookup"><span data-stu-id="96b68-126">It is possible that the WIA 2.0 item passed into **IWiaPreview::UpdatePreview** represents only a small region of the image downloaded from the driver.</span></span> <span data-ttu-id="96b68-127">Se esse for o caso, o componente de visualização WIA 2,0 recortará essa região da imagem armazenada em cache antes de passá-la para o filtro de processamento de imagem, que, por sua vez, passa os dados de imagem filtrados de volta para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96b68-127">If this is the case the WIA 2.0 Preview Component actually cuts out this region from the cached image before it passes it to the image processing filter, which in turn passes the filtered image data back to the application.</span></span>

<span data-ttu-id="96b68-128">Para que um aplicativo transmita toda a imagem armazenada em cache para o filtro de processamento de imagens (que por sua vez passa para o aplicativo), ele deve definir *lOptions* como **WiaPreviewReturnOriginalImage** ao chamar **IWiaPreview:: UpdatePreview**.</span><span class="sxs-lookup"><span data-stu-id="96b68-128">For an application to pass the entire cached image to the image processing filter (which in turn passes it to the application), it must set the *lOptions* to **WiaPreviewReturnOriginalImage** when calling **IWiaPreview::UpdatePreview**.</span></span> <span data-ttu-id="96b68-129">Ao definir *lOptions* como **WiaPreviewReturnOriginalImage**, o aplicativo deve garantir que as configurações de extensão ([**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YEXTENT**) do item passado para **IWiaPreview:: UpdatePreview** corresponda à imagem em cache completo.</span><span class="sxs-lookup"><span data-stu-id="96b68-129">When setting *lOptions* to **WiaPreviewReturnOriginalImage**, the application must ensure that the extent settings ([**WIA\_IPS\_XEXTENT**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YEXTENT**) of the item passed into **IWiaPreview::UpdatePreview** matches the full-cached image.</span></span> <span data-ttu-id="96b68-130">O filtro de processamento de imagens não precisa fazer nada diferente nesse caso; Ele simplesmente filtra a imagem, com base nas propriedades de *pChildWiaItem* (normalmente, nesse caso, *pChildWiaItem* é o mesmo item que foi passado para [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span><span class="sxs-lookup"><span data-stu-id="96b68-130">The image processing filter need not do anything different in this case; it simply filters the image, based on the properties of *pChildWiaItem* (typically in this case *pChildWiaItem* is the same item that was passed to [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md)).</span></span> <span data-ttu-id="96b68-131">As diferentes subregiãos são ignoradas e toda a imagem é filtrada usando as mesmas configurações.</span><span class="sxs-lookup"><span data-stu-id="96b68-131">The different sub-regions are ignored and the whole image is filtered using the same settings.</span></span> <span data-ttu-id="96b68-132">Há algumas razões pelas quais um aplicativo faria isso.</span><span class="sxs-lookup"><span data-stu-id="96b68-132">There are a couple of reasons why an application would do this.</span></span>

1.  <span data-ttu-id="96b68-133">O aplicativo pode não dar suporte à alteração das configurações (como o [**\_ \_ brilho de IPS WIA**](-wia-wiaitempropscanneritem.md) e o **\_ \_ contraste de IPS WIA**) individualmente para cada região detectada pelo filtro de segmentação (ou talvez nem mesmo queira usar o filtro de segmentação).</span><span class="sxs-lookup"><span data-stu-id="96b68-133">The application may not support changing the settings (like [**WIA\_IPS\_BRIGHTNESS**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_CONTRAST**) individually for each region that the segmentation filter detects (or it may not even want to use the segmentation filter).</span></span> <span data-ttu-id="96b68-134">É mais fácil para o aplicativo chamar **IWiaPreview:: UpdatePreview** com **WiaPreviewReturnOriginalImage** para que ele sempre receba a imagem completa do componente de visualização do WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="96b68-134">It is easier for the application to call **IWiaPreview::UpdatePreview** with **WiaPreviewReturnOriginalImage** so that it always receives the full image from the WIA 2.0 Preview Component.</span></span>
2.  <span data-ttu-id="96b68-135">O componente de visualização do WIA 2,0 não oferece suporte ao formato de imagem da imagem de visualização; nesse caso, ele não pode executar as ações para recortar a região desejada.</span><span class="sxs-lookup"><span data-stu-id="96b68-135">The WIA 2.0 Preview Component does not support the image format of the preview image, in which case it cannot perform the actions to cut out the desired region.</span></span> <span data-ttu-id="96b68-136">O suporte ao formato de imagem do componente de visualização do WIA 2,0 é limitado a formatos para os quais há codificadores e decodificadores Windows GDI+ 1,1.</span><span class="sxs-lookup"><span data-stu-id="96b68-136">The WIA 2.0 Preview Component's image format support is limited to formats for which there are Windows GDI+ 1.1 encoders and decoders.</span></span> <span data-ttu-id="96b68-137">Esses formatos são bitmap (BMP) (um bitmap que inclui o BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, PNG (Portable Network Graphics) e TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="96b68-137">These formats are bitmap (BMP) (a bitmap that includes the BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG), and Tagged Image File Format (TIFF).</span></span>

<span data-ttu-id="96b68-138">Observe que, se o aplicativo passar **WiaPreviewReturnOriginalImage** para **IWiaPreview:: UpdatePreview**, o componente de visualização WIA 2,0 poderá dar suporte a qualquer formato de imagem ou pixel.</span><span class="sxs-lookup"><span data-stu-id="96b68-138">Note that if the application passes **WiaPreviewReturnOriginalImage** into **IWiaPreview::UpdatePreview**, the WIA 2.0 Preview Component can support any image or pixel format.</span></span>

<span data-ttu-id="96b68-139">**IWiaPreview:: UpdatePreview** define a propriedade de [**\_ \_ visualização do DPS do WIA**](-wia-wiaitempropscannerdevice.md) (e a redefine antes de retornar, a menos que tenha sido definido antes).</span><span class="sxs-lookup"><span data-stu-id="96b68-139">**IWiaPreview::UpdatePreview** sets the [**WIA\_DPS\_PREVIEW**](-wia-wiaitempropscannerdevice.md) property (and resets it before it returns, unless it was set before).</span></span> <span data-ttu-id="96b68-140">Isso permite que o driver (e o hardware), bem como o filtro de processamento de imagens, saibam que o item é uma verificação de visualização.</span><span class="sxs-lookup"><span data-stu-id="96b68-140">This lets the driver (and hardware) as well as the image processing filter, know that the item is a preview scan.</span></span>

<span data-ttu-id="96b68-141">Um aplicativo deve garantir que *pChildWiaItem* tenha o mesmo formato de imagem [**( \_ \_ formato WIA IPA**](-wia-wiaitempropcommonitem.md)) e resolução [**(WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YRES**) que *pWiaItem* tinha quando ele foi passado para [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span><span class="sxs-lookup"><span data-stu-id="96b68-141">An application must ensure that *pChildWiaItem* has the same image format ([**WIA\_IPA\_FORMAT**](-wia-wiaitempropcommonitem.md)) and resolution ([**WIA\_IPS\_XRES**](-wia-wiaitempropscanneritem.md) and **WIA\_IPS\_YRES**) as *pWiaItem* had when it was passed into [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md).</span></span> <span data-ttu-id="96b68-142">O formato do item filho deve corresponder ao formato da imagem armazenada em cache do componente de visualização do WIA 2,0 (o componente de visualização do WIA 2,0 não executa nenhuma conversão de imagem).</span><span class="sxs-lookup"><span data-stu-id="96b68-142">The format of the child item must correspond to the format of the WIA 2.0 Preview Component's cached image (the WIA 2.0 Preview Component performs no image conversion).</span></span>

## <a name="examples"></a><span data-ttu-id="96b68-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="96b68-143">Examples</span></span>

<span data-ttu-id="96b68-144">UpdateRegion deve ser chamado cada vez que um usuário muda, por exemplo, o brilho ou contraste para o item filho representado por `dwRegionNumber` .</span><span class="sxs-lookup"><span data-stu-id="96b68-144">UpdateRegion should be called each time a user changes, for example, the brightness or contrast for the child item represented by `dwRegionNumber`.</span></span> <span data-ttu-id="96b68-145">Este item filho foi criado anteriormente pelo filtro de segmentação ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span><span class="sxs-lookup"><span data-stu-id="96b68-145">This child item has previously been created by the segmentation filter ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md).</span></span> <span data-ttu-id="96b68-146">A imagem gravada no [IStream](/windows/win32/api/objidl/nn-objidl-istream) é retornada pelo método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) da interface de retorno de chamada de transferência.</span><span class="sxs-lookup"><span data-stu-id="96b68-146">The image written to the [IStream](/windows/win32/api/objidl/nn-objidl-istream) is returned by the transfer callback interface's [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) method.</span></span> <span data-ttu-id="96b68-147">O código para GetSubRegionItem é omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="96b68-147">The code for GetSubRegionItem is omitted in this example.</span></span>

<span data-ttu-id="96b68-148">Depois que essa função for chamada, um aplicativo normalmente redesenharia a região na tela.</span><span class="sxs-lookup"><span data-stu-id="96b68-148">After this function has been called, an application would typically redraw the region on the screen.</span></span>


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a><span data-ttu-id="96b68-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96b68-149">Requirements</span></span>



| <span data-ttu-id="96b68-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="96b68-150">Requirement</span></span> | <span data-ttu-id="96b68-151">Valor</span><span class="sxs-lookup"><span data-stu-id="96b68-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96b68-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96b68-152">Minimum supported client</span></span><br/> | <span data-ttu-id="96b68-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96b68-153">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="96b68-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96b68-154">Minimum supported server</span></span><br/> | <span data-ttu-id="96b68-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96b68-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="96b68-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96b68-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="96b68-157"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="96b68-157"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="96b68-158">INSERI</span><span class="sxs-lookup"><span data-stu-id="96b68-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96b68-159"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96b68-159"><dt>Wia.idl</dt></span></span> </dl> |



 

 
