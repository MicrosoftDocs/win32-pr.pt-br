---
description: O \_ método Get streamtype recupera o GUID (identificador global exclusivo) para o tipo de mídia do fluxo atual.
ms.assetid: 2f61b3fe-c041-4031-9211-2f5fc189542b
title: 'Método IMediaDet:: get_StreamType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5834183229580c1aadbcbe80e54a30e9b9b60c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780051"
---
# <a name="imediadetget_streamtype-method"></a>Método streamtype de IMediaDet:: get \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_StreamType` método recupera o GUID (identificador global exclusivo) para o tipo de mídia do fluxo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_StreamType(
  [out, retval] GUID *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o GUID de tipo principal para o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método recupera o membro **majortype** da estrutura [**do \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . A estrutura do **\_ \_ tipo de mídia am** descreve o formato do fluxo, e o membro **majortype** é um GUID que indica a categoria geral, como áudio ou vídeo. Para um fluxo de vídeo, o GUID é \_ vídeo de MediaType. Para áudio, é áudio de MEDIATYPE \_ . Para recuperar toda a estrutura do **\_ \_ tipo de mídia am** , chame o método [**IMediaDet:: get \_ StreamMediaType**](imediadet-get-streammediatype.md) .

Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG. Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




