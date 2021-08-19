---
description: O método \_ put DestinationHeight define a altura do retângulo de destino.
ms.assetid: 2cb7af2b-69dc-4e86-b2cf-34223c9e5a1b
title: CBaseControlVideo.put_DestinationHeight método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.put_DestinationHeight
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed1b8c43b835b1996f2f6dcb512b741f130235b86905b90fc0886c9cc0f7fd9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017424"
---
# <a name="cbasecontrolvideoput_destinationheight-method"></a>Método CBaseControlVideo.put \_ DestinationHeight

O `put_DestinationHeight` método define a altura do retângulo de destino.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_DestinationHeight(
   long DestinationHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DestinationHeight* 
</dt> <dd>

Nova altura de destino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT** que depende da implementação; pode ser um dos valores a seguir ou outros valores não listados.



| Código de retorno                                                                                           | Descrição                                                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>                | Falha.<br/>                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Argumento inválido.<br/>                                                     |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>             | Argumento de ponteiro **NULL.**<br/>                                            |
| <dl> <dt>**NOERROR**</dt> </dl>                | Êxito.<br/>                                                              |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | A operação não pode ser executada porque os pinos não estão conectados.<br/> |



 

## <a name="remarks"></a>Comentários

Um aplicativo pode alterar os retângulos de origem e de destino do vídeo por meio da interface [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo) O retângulo de origem afeta qual seção da fonte de vídeo nativa será exibida na exibição; o retângulo de destino afeta o local em que o vídeo será exibido quando for exibido. O retângulo de destino é relativo à área do cliente da janela na qual ele está sendo a reprodução. O canto superior esquerdo da janela é coordenado (0,0).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




