---
description: O \_ método Get DestinationLeft recupera a coordenada esquerda do retângulo de destino atual.
ms.assetid: f1c6d784-7ec3-4d44-a3fb-c1e3b988e392
title: Método de CBaseControlVideo.get_DestinationLeft (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_DestinationLeft
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ec35cc3fa831218fb7c5c4810643d58b9c9d303a9501d10969d847649c2efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661512"
---
# <a name="cbasecontrolvideoget_destinationleft-method"></a>CBaseControlVideo. obter \_ método DestinationLeft

O `get_DestinationLeft` método recupera a coordenada esquerda do retângulo de destino atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_DestinationLeft(
   long *pDestinationLeft
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDestinationLeft* 
</dt> <dd>

Ponteiro para a coordenada esquerda do retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | A operação não pode ser executada porque os Pins não estão conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |



 

## <a name="remarks"></a>Comentários

Essa função de membro implementa o método [**IBasicVideo:: get \_ DestinationLeft**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_destinationleft) .

Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido. O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada. O canto superior esquerdo da janela é coordenada (0, 0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




