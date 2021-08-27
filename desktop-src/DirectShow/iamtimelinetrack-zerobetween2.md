---
description: O método ZeroBetween2 remove tudo da faixa entre os horários especificados. Esse método é equivalente a IAMTimelineTrack::ZeroBetween, mas aceita valores REFTIME.
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: Método IAMTimelineTrack::ZeroBetween2 (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72ea9d96be976f1b09e1cdc9721eb5eebe7adce2905d7a028d70a9ff50ff58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952775"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>Método IAMTimelineTrack::ZeroBetween2

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ZeroBetween2` método remove tudo da faixa entre os horários especificados. Esse método é equivalente a [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), mas aceita [**valores REFTIME.**](reftime.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtStart* 
</dt> <dd>

Início do intervalo a ser limpo, em segundos.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Fim do intervalo a ser limpo, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                             | Descrição                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | O intervalo de tempo vai além de tudo na faixa.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                             |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineTrack Interface**](iamtimelinetrack.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




