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
ms.openlocfilehash: b5f48462d926d96acebf4a74f0a843d82f9cd97190585b954565d5da649ff9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549686"
---
# <a name="iwiapreviewupdatepreview-method"></a>Método IWiaPreview:: UpdatePreview

Obtém a imagem não filtrada armazenada em cache pelo método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UpdatePreview(
  [in] LONG      lOptions,
  [in] IWiaItem2 *pChildWiaItem
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lOptions* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica se o aplicativo requer que o componente de visualização do WIA 2,0 passe uma sub-região da imagem armazenada em cache ou toda a imagem armazenada em cache para o filtro de processamento de imagem.

<dt>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>

<span id="WiaPreviewReturnOriginalImage"></span><span id="wiapreviewreturnoriginalimage"></span><span id="WIAPREVIEWRETURNORIGINALIMAGE"></span>**WiaPreviewReturnOriginalImage**


</dt> <dd>

Passe toda a imagem armazenada em cache para o filtro de processamento de imagem.

</dd> </dl> </dd> <dt>

*pChildWiaItem* \[ no\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica um ponteiro para o item [**IWiaItem2**](-wia-iwiaitem2.md) , que é um filho do item **IWiaItem2** especificado pelo parâmetro *pWiaItem2* do método [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Ou, se o aplicativo exigir uma visualização da mesa inteira, especificará um ponteiro para o parâmetro *pWiaItem2* do método **IWiaPreview:: GetNewPreview** . Quando *pChildWiaItem* é um filho do parâmetro *pWiaItem2* **IWiaPreview:: GetNewPreview**, esse item filho normalmente é criado pelo filtro de segmentação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método passa a imagem armazenada em cache e não filtrada por meio do filtro de processamento de imagem, que grava os dados filtrados no fluxo fornecido pelo aplicativo. O componente de visualização do WIA 2,0 recupera esse fluxo chamando o método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) do filtro de processamento de imagens, que chama a implementação **GetNextStream** do retorno de chamada do aplicativo. Antes de chamar **IWiaPreview:: UpdatePreview**, um aplicativo deve primeiro chamar [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para adquirir a imagem do scanner; caso contrário, o método retornará um erro.

O componente de visualização do WIA 2,0 armazena a imagem não filtrada baixada do driver. É possível que o item 2,0 do WIA passado para **IWiaPreview:: UpdatePreview** represente apenas uma pequena região da imagem baixada do driver. Se esse for o caso, o componente de visualização WIA 2,0 recortará essa região da imagem armazenada em cache antes de passá-la para o filtro de processamento de imagem, que, por sua vez, passa os dados de imagem filtrados de volta para o aplicativo.

Para que um aplicativo transmita toda a imagem armazenada em cache para o filtro de processamento de imagens (que por sua vez passa para o aplicativo), ele deve definir *lOptions* como **WiaPreviewReturnOriginalImage** ao chamar **IWiaPreview:: UpdatePreview**. Ao definir *lOptions* como **WiaPreviewReturnOriginalImage**, o aplicativo deve garantir que as configurações de extensão ([**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YEXTENT**) do item passado para **IWiaPreview:: UpdatePreview** corresponda à imagem em cache completo. O filtro de processamento de imagens não precisa fazer nada diferente nesse caso; Ele simplesmente filtra a imagem, com base nas propriedades de *pChildWiaItem* (normalmente, nesse caso, *pChildWiaItem* é o mesmo item que foi passado para [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md)). As diferentes subregiãos são ignoradas e toda a imagem é filtrada usando as mesmas configurações. Há algumas razões pelas quais um aplicativo faria isso.

1.  O aplicativo pode não dar suporte à alteração das configurações (como o [**\_ \_ brilho de IPS WIA**](-wia-wiaitempropscanneritem.md) e o **\_ \_ contraste de IPS WIA**) individualmente para cada região detectada pelo filtro de segmentação (ou talvez nem mesmo queira usar o filtro de segmentação). É mais fácil para o aplicativo chamar **IWiaPreview:: UpdatePreview** com **WiaPreviewReturnOriginalImage** para que ele sempre receba a imagem completa do componente de visualização do WIA 2,0.
2.  O componente de visualização do WIA 2,0 não oferece suporte ao formato de imagem da imagem de visualização; nesse caso, ele não pode executar as ações para recortar a região desejada. o suporte ao formato de imagem do componente de visualização do WIA 2,0 é limitado a formatos para os quais há Windows GDI+ de codificadores e decodificadores 1,1. Esses formatos são bitmap (BMP) (um bitmap que inclui o BITMAPFILEHEADER), Graphics Interchange Format (GIF), JPEG, PNG (Portable Network Graphics) e TIFF (Tagged Image File Format).

Observe que, se o aplicativo passar **WiaPreviewReturnOriginalImage** para **IWiaPreview:: UpdatePreview**, o componente de visualização WIA 2,0 poderá dar suporte a qualquer formato de imagem ou pixel.

**IWiaPreview:: UpdatePreview** define a propriedade de [**\_ \_ visualização do DPS do WIA**](-wia-wiaitempropscannerdevice.md) (e a redefine antes de retornar, a menos que tenha sido definido antes). Isso permite que o driver (e o hardware), bem como o filtro de processamento de imagens, saibam que o item é uma verificação de visualização.

Um aplicativo deve garantir que *pChildWiaItem* tenha o mesmo formato de imagem [**( \_ \_ formato WIA IPA**](-wia-wiaitempropcommonitem.md)) e resolução [**(WIA \_ IPS \_ XRES**](-wia-wiaitempropscanneritem.md) e **WIA \_ IPS \_ YRES**) que *pWiaItem* tinha quando ele foi passado para [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). O formato do item filho deve corresponder ao formato da imagem armazenada em cache do componente de visualização do WIA 2,0 (o componente de visualização do WIA 2,0 não executa nenhuma conversão de imagem).

## <a name="examples"></a>Exemplos

UpdateRegion deve ser chamado cada vez que um usuário muda, por exemplo, o brilho ou contraste para o item filho representado por `dwRegionNumber` . Este item filho foi criado anteriormente pelo filtro de segmentação ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md). A imagem gravada no [IStream](/windows/win32/api/objidl/nn-objidl-istream) é retornada pelo método [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) da interface de retorno de chamada de transferência. O código para GetSubRegionItem é omitido neste exemplo.

Depois que essa função for chamada, um aplicativo normalmente redesenharia a região na tela.


```C++
HRESULT
UpdateRegion(
   IN  DWORD dwRegionNumber)
{
   IWiaItem2 *pSubRegion = GetSubRegionItem(dwRegionNumber);

   return m_pWiaPreview->UpdatePreview(0,pSubRegion);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
