---
description: O método GetDestinationPosition recupera o retângulo de destino em uma operação atômica.
ms.assetid: 780cbcb5-1db5-4087-8c51-350183cfca31
title: Método CBaseControlVideo.GetDestinationPosition (Ctlutil.h)
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
ms.openlocfilehash: 3b077548e6a427e70d098cbece93cdc033972cf48a664dd85cd0dfab747d88c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661132"
---
# <a name="cbasecontrolvideogetdestinationposition-method"></a>Método CBaseControlVideo.GetDestinationPosition

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

*Pwidth* 
</dt> <dd>

Ponteiro para a largura do retângulo de destino.

</dd> <dt>

*pHeight* 
</dt> <dd>

Ponteiro para a altura do retângulo de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | Argumento de ponteiro **NULL.**<br/>                                            |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | A operação não pode ser executada porque os pinos não estão conectados.<br/> |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |



 

## <a name="remarks"></a>Comentários

Essa função membro pode ser usada no lugar de chamadas separadas para as funções [**membro CBaseControlVideo::get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md), [**CBaseControlVideo::get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md), [**CBaseControlVideo::get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)e [**CBaseControlVideo::get \_ DestinationHeight.**](cbasecontrolvideo-get-destinationheight.md) Um aplicativo pode alterar os retângulos de origem e de destino do vídeo por meio da interface [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for exibido. O retângulo de destino é relativo à área do cliente da janela na qual ele está sendo a reprodução. O canto superior esquerdo da janela é coordenado (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




