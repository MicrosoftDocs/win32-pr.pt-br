---
description: A função FreeMediaType exclui o bloco de formato em uma \_ estrutura de tipo de mídia am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Função FreeMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758523"
---
# <a name="freemediatype-function"></a>Função FreeMediaType

A função **FreeMediaType** exclui o bloco de formato em uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

## <a name="syntax"></a>Sintaxe


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MT* \[ referência\]
</dt> <dd>

Uma referência a uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

O bloco de formato é alocado no heap. O membro **pbFormat** do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) aponta para o bloco de formato. Use essa função para liberar apenas o bloco de formato. Para excluir uma estrutura **de \_ \_ tipo de mídia am** alocada, chame [**DeleteMediaType**](deletemediatype.md).

Essa função é definida na biblioteca de [classes base do DirectShow](directshow-base-classes.md) . Se preferir não vincular à biblioteca de classes base, você pode usar o seguinte código:


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**Funções de tipo de mídia**](media-type-functions.md)
</dt> </dl>

 

 




