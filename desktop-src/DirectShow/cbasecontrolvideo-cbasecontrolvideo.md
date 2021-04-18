---
description: Método de construtor.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Construtor CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760099"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Construtor CBaseControlVideo. CBaseControlVideo

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o objeto de filtro de mídia proprietário.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Ponteiro para a seção crítica a ser usada para bloqueio.

</dd> <dt>

*pName* 
</dt> <dd>

Ponteiro para a descrição do objeto.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de controle, se o objeto fizer parte de uma agregação; caso contrário, deve ser **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor HRESULT que indica o êxito ou a falha do método de construtor.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto implementa a interface de controle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .

Todos os métodos de interface de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) que essa classe implementa exigem que o filtro esteja conectado corretamente. Por esse motivo, a classe recebe um PIN com o qual ele deve sincronizar. Sempre que um método de interface é chamado, o objeto determina que o PIN ainda está conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




