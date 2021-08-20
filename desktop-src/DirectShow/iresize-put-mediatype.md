---
description: O método \_ put MediaType define o tipo de mídia de saída no filtro do resizer.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: Método IResize::p ut_MediaType (Qedit.h)
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
ms.openlocfilehash: 6c26878af6f091efd3c3f321cb073ce51a8e6236d4bafa326ab99f85f39e1a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818197"
---
# <a name="iresizeput_mediatype-method"></a>Método MediaType IResize::p ut \_

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `put_MediaType` método define o tipo de mídia de saída no filtro do resizer.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pmt* \[ Em\]
</dt> <dd>

Ponteiro para uma [**estrutura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) que contém o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O DES chama esse método antes de conectar o pino de saída do filtro. Use o tipo de mídia como o tipo de mídia do pino de saída. Retorne esse tipo de mídia no método [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) e verifique agsint esse tipo no [**método CTransformFilter::CheckTransform.**](ctransformfilter-checktransform.md) O DES nunca chama esse método depois que o pino de saída é conectado.

Atualmente, o DES sempre define o tipo de mídia de saída para um formato RGB descompactado com um bloco de formato **VIDEOINFOHEADER** (o tipo de formato é igual a FORMAT \_ VideoInfo). O subtipo pode ser MEDIASUBTYPE ARGB32, que indica RGB de \_ 32 bits com um canal alfa.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | DirectX 9.0 ou posterior<br/>                                                         |
| Cabeçalho<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> <dt>

[**IResize Interface**](iresize.md)
</dt> </dl>

 

 




