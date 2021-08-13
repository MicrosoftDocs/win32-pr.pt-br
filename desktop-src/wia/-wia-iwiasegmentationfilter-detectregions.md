---
description: Determina as sub-regiões de uma imagem colocada na placa de flatbed para que cada sub-região possa ser adquirida em um item de imagem separado.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: Método IWiaSegmentationFilter::D etectRegions (Wia.h)
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
ms.openlocfilehash: 46496360d7b54bed837ba287d604233a9fac98ee13807744b4adbfb52e9934d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450256"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>Método IWiaSegmentationFilter::D etectRegions

Determina as sub-regiões de uma imagem colocada na placa de flatbed para que cada sub-região possa ser adquirida em um item de imagem separado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Atualmente não éusado. Deve ser definido como zero.

</dd> <dt>

*pInputStream* \[ Em\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Especifica um ponteiro para a imagem de [visualização do IStream.](/windows/win32/api/objidl/nn-objidl-istream)

</dd> <dt>

*pWiaItem2* \[ Em\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica um ponteiro para o item [**IWiaItem2**](-wia-iwiaitem2.md) para o qual *pInputStream* foi adquirido. O filtro de segmentação cria itens filho para este item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Esse método determina as sub-regiões da imagem representada por pInputStream. Para cada sub-região detectada, ele cria um item filho para o item [**IWiaItem2**](-wia-iwiaitem2.md) especificado no parâmetro *pWiaItem2.* Para cada item filho, o filtro de segmentação deve definir valores para o retângulo delimitar da área a ser digitalizada, usando as seguintes Constantes de Propriedade de [**Item WIA do Scanner**](-wia-wiaitempropscanneritem.md).

-   [**WIA \_ IPS \_ XPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YEXTENT**](-wia-wiaitempropscanneritem.md)

Um filtro mais avançado também pode exigir outras Constantes de Propriedade de [**Item WIA**](-wia-wiaitempropscanneritem.md) do Scanner, como **WIA \_ IPS \_ DESKEW \_ X** e **WIA \_ IPS \_ DESKEW \_ Y,** se o driver for compatível com a desfiada.

Se o aplicativo chamar **IWiaSegmentationFilter::D etectRegions** mais de uma vez, o aplicativo deverá primeiro excluir os itens filho criados pela última chamada para **IWiaSegmentationFilter::D etectRegions**.

Se um aplicativo altera qualquer propriedade para *pWiaItem2*, entre adquirir a imagem em *pInputStream* e sua chamada para **IWiaSegmentationFilter::D etectRegions**, as propriedades originais (ou seja, as propriedades que o item tinha quando o fluxo foi adquirido) devem ser restauradas. Isso pode ser feito por [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) e [**SetPropertyStream.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)

O aplicativo deverá redefinir [o IStream](/windows/win32/api/objidl/nn-objidl-istream) se sua chamada passar o mesmo fluxo para o filtro de segmentação mais de uma vez. O aplicativo também deve redefinir o fluxo após o download inicial e antes de chamar **IWiaSegmentationFilter::D etectRegions**.

## <a name="examples"></a>Exemplos

A segmentação executa a detecção de região no fluxo ( `pImageStream` ) passado para DetectSubregions. Consulte o [**método GetExtension**](-wia-iwiaitem2-getextension.md) para CreateSegmentationFilter usado neste exemplo.


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



DownloadPreviewImage baixa dados de imagem do scanner chamando o método [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) do componente de visualização. Em seguida, ele chamará DetectSubregions se o usuário do aplicativo quiser invocar o filtro de segmentação, que cria um item filho em pWiaItem2 para cada região detectada. Consulte **IWiaSegmentationFilter::D etectRegions para** o método DetectSubregions usado neste exemplo.

Neste exemplo, o usuário do aplicativo define `m_bUseSegmentationFilter` clicando em uma caixa de seleção. Se o aplicativo dá suporte a isso, ele deve primeiro verificar se o driver tem um filtro de segmentação chamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md). Consulte [**GetNewPreview para**](-wia-iwiapreview-getnewpreview.md) o exemplo de método CheckImgFilter que mostra como isso pode ser feito.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
