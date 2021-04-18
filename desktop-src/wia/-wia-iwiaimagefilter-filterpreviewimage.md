---
description: Filtra a imagem de visualização.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: 'Método IWiaImageFilter:: FilterPreviewImage (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 882aaf0d131ae6fe062c00c0181e2f913a0e1bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791450"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>Método IWiaImageFilter:: FilterPreviewImage

Filtra a imagem de visualização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Não usado. Defina como 0.

</dd> <dt>

*pWiaChildItem2* \[ no\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

O item que é processado.

</dd> <dt>

_InputImageExtents * \[ in\]
</dt> <dd>

Tipo: **Rect**

As coordenadas (na área de aquisição física) da imagem que o componente de visualização armazena em cache internamente.

</dd> <dt>

*pInputStream* \[ no\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Um ponteiro para a interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) para os dados de imagem armazenados em cache que são filtrados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Não chame esse método diretamente do seu aplicativo.

*pWiaChildItem2* deve ser um item filho do *pWiaItem2* que foi passado em [**IWiaImageFilter:: InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md).

*InputImageExtents* é necessário porque o filtro de processamento de imagem é responsável por recortar a área de imagem que o *pWiaChildItem2* representa dos dados de imagem passados por meio de *pInputStream*.

Um aplicativo deve garantir que *pWiaChildItem2* tenha o mesmo formato de imagem ( \_ formato WIA IPA \_ ), resolução (WIA \_ IPS \_ XRES e WIA \_ IPS \_ YRES) e profundidade de bits (profundidade de IPA WIA \_ \_ ) como *pWiaItem2* tinha quando transmitida para [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
