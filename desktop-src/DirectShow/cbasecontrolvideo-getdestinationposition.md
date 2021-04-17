---
description: O método GetDestinationPosition recupera o retângulo de destino em uma operação atômica.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Método CBaseControlVideo. GetDestinationPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetDestinationPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86ed919af270df508eb8f76e32597b410dec56b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752727"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>Método CBaseControlVideo. GetDestinationPosition

O `GetDestinationPosition` método recupera o retângulo de destino em uma operação atômica.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDestinationPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pLeft* 
</dt> <dd>

Ponteiro para a coordenada esquerda do retângulo de destino.

</dd> <dt>

*pTop* 
</dt> <dd>

Ponteiro para a coordenada superior do retângulo de destino.

</dd> <dt>

*pWidth* 
</dt> <dd>

Ponteiro para a largura do retângulo de destino.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura do retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ falha**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**\_ponteiro E**</dt> </dl>             | Argumento de ponteiro **nulo** .<br/>                                            |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | A operação não pode ser executada porque os Pins não estão conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |



 

## <a name="remarks"></a>Comentários

Essa função de membro pode ser usada em vez de chamadas separadas para as funções de membro [**CBaseControlVideo:: get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo:: get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo:: get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)e [**CBaseControlVideo:: get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md) . Um aplicativo pode alterar os retângulos de origem e de destino para o vídeo por meio da interface [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for reproduzido. O retângulo de destino é relativo à área do cliente da janela na qual está sendo executada. O canto superior esquerdo da janela é coordenada (0, 0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




