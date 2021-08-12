---
description: O método \_ get SourceWidth recupera a largura do retângulo de origem atual.
ms.assetid: e8e27f8f-57e5-489c-aae7-86493677b380
title: CBaseControlVideo.get_SourceWidth método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_SourceWidth
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79241f52f9d7b6cb32bd9022d6d022c880656780043e8c78481975c80907511d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661491"
---
# <a name="cbasecontrolvideoget_sourcewidth-method"></a>Método CBaseControlVideo.get \_ SourceWidth

O `get_SourceWidth` método recupera a largura do retângulo de origem atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SourceWidth(
   long *pSourceWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSourceWidth* 
</dt> <dd>

Ponteiro para a largura do retângulo de origem atual.

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

Essa função membro implementa o [**método IBasicVideo::get \_ SourceWidth.**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_sourcewidth)

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

 

 




