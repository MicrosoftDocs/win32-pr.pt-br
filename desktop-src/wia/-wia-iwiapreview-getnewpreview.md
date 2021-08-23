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
ms.openlocfilehash: 2200452fe586a4755a4560f0f68094e5f107e9e7d69a823bafac4d33bc1c6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965555"
---
# <a name="iwiapreviewgetnewpreview-method"></a>Método IWiaPreview:: GetNewPreview

Armazena internamente em cache a imagem não filtrada retornada do driver.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pWiaItem2* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica um ponteiro para o item [**IWiaItem2**](-wia-iwiaitem2.md) para a imagem.

</dd> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*pWiaTransferCallback* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Especifica um ponteiro para a interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) do aplicativo de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Um aplicativo deve chamar **IWiaPreview:: GetNewPreview** antes de chamar [**IWiaPreview::D etectregions**](-wia-iwiapreview-detectregions.md).

**IWiaPreview:: GetNewPreview** define a propriedade de [**\_ \_ visualização do DPS do WIA**](-wia-wiaitempropscannerdevice.md) (e a redefine antes de retornar, a menos que tenha sido definido antes). Isso permite que o driver e o hardware, bem como o filtro de processamento de imagens, saibam que o item é uma verificação de visualização.

internamente, o componente de visualização do WIA (Windows Image Acquisition) 2,0 cria uma instância do filtro de processamento de imagem do driver chamando [**getextension**](-wia-iwiaitem2-getextension.md) em *pWiaItem2*. O componente de visualização do WIA 2,0 faz isso quando o aplicativo chama **IWiaPreview:: GetNewPreview**. O componente de visualização do WIA 2,0 também Inicializa o filtro em **IWiaPreview:: GetNewPreview**. A mesma instância de filtro é usada pelo componente de visualização do WIA 2,0 durante uma chamada para [**IWiaPreview:: UpdatePreview**](-wia-iwiapreview-updatepreview.md).

Antes de chamar o componente de visualização do WIA 2,0, um aplicativo deve chamar [**CheckExtension**](-wia-iwiaitem2-checkextension.md) para certificar-se de que o driver vem com um filtro de processamento de imagem. Ele deve chamar **CheckExtension** no item que ele passaria para **IWiaPreview:: GetNewPreview**. É inútil fornecer visualizações dinâmicas sem um filtro de processamento de imagem. Se um aplicativo chamar **IWiaPreview:: GetNewPreview** para um driver sem um filtro de processamento de imagem, a chamada falhará.

## <a name="examples"></a>Exemplos

CheckImgFilter verifica se o driver tem um filtro de processamento de imagem. Antes de chamar o componente de visualização, um aplicativo deve garantir que o driver tenha um filtro de processamento de imagem.


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



O DownloadPreviewImage baixa dados de imagem do scanner chamando o método **IWiaPreview:: GetNewPreview** do componente de visualização. Em seguida, ele chama DetectSubregions se o usuário do aplicativo quiser invocar o filtro de segmentação, que cria um item filho em pWiaItem2 para cada região detectada. Consulte [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) para o método DetectSubregions usado neste exemplo.

Neste exemplo, o usuário do aplicativo define `m_bUseSegmentationFilter` clicando em uma caixa de seleção. Se o aplicativo der suporte a isso, primeiro verifique se o driver tem um filtro de segmentação chamando [**CheckExtension**](-wia-iwiaitem2-checkextension.md). Consulte **IWiaPreview:: GetNewPreview** para obter o exemplo do método CheckImgFilter que mostra como isso pode ser feito.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




