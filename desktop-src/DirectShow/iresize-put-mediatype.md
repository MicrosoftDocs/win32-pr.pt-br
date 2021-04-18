---
description: O \_ método Put MediaType define o tipo de mídia de saída no filtro redimensionador.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: 'IResize: método de ut_MediaType de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aedaced5033c229131f548e298217e3c77ff70c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810217"
---
# <a name="iresizeput_mediatype-method"></a>Método IResize::p UT \_ MediaType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_MediaType` método define o tipo de mídia de saída no filtro de redimensionador.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PGTO* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O DES chama esse método antes de conectar o PIN de saída do filtro. Use o tipo de mídia como o tipo de mídia do pino de saída. Retorne esse tipo de mídia no método [**CTransformFilter:: GetMediaType**](ctransformfilter-getmediatype.md) e marque agsint deste tipo no método [**CTransformFilter:: CheckTransform**](ctransformfilter-checktransform.md) . O DES nunca chama esse método depois que o pino de saída é conectado.

Atualmente, o DES sempre define o tipo de mídia de saída como um formato RGB descompactado com um bloco de formato **VIDEOINFOHEADER** (tipo de formato igual a VIDEOINFO de formato \_ ). O subtipo pode ser MEDIASUBTYPE \_ ARGB32, que indica o RGB de 32 bits com um canal alfa.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9,0 ou posterior<br/>                                                         |
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**Interface IResize**](iresize.md)
</dt> </dl>

 

 




