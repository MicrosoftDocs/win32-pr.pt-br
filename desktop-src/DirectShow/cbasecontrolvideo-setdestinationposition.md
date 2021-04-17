---
description: O método SetDestinationPosition define o retângulo de destino para o vídeo.
ms.assetid: 397e90ea-7535-4cac-9f47-7a93737b1e3a
title: Método CBaseControlVideo. SetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 798a65c44dd490587e3ad46fcae2c61a03986df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750709"
---
# <a name="cbasecontrolvideosetdestinationposition-method"></a>Método CBaseControlVideo. SetDestinationPosition

O `SetDestinationPosition` método define o retângulo de destino para o vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDestinationPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Mantida* 
</dt> <dd>

Nova coordenada esquerda.

</dd> <dt>

*Top* 
</dt> <dd>

Nova coordenada superior.

</dd> <dt>

*Largura* 
</dt> <dd>

Nova largura.

</dd> <dt>

*Altura* 
</dt> <dd>

Nova altura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argumento inválido.<br/>                                                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | A operação não pode ser executada porque os Pins não estão conectados.<br/> |



 

## <a name="remarks"></a>Comentários

Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido. O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada. O canto superior esquerdo da janela é coordenada (0, 0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




