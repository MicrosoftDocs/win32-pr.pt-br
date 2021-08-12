---
description: O método Skip ignora um número especificado de tipos de mídia. Esse método implementa o método IEnumMediaTypes::Skip.
ms.assetid: a01fb084-b227-4ca6-b5ca-c57d56e8b1aa
title: Método CEnumMediaTypes.Skip (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a9930472b5c8a2873ca0a7f3280565bd41ac6b0aac7e1e33303464d3a2c1ca3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656441"
---
# <a name="cenummediatypesskip-method"></a>Método CEnumMediaTypes.Skip

O `Skip` método ignora um número especificado de tipos de mídia. Esse método implementa o [**método IEnumMediaTypes::Skip.**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-skip)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
   ULONG cMediaTypes
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cMediaTypes* 
</dt> <dd>

Número de tipos de mídia a ignorar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                                                | Descrição                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Ignorado após o final da sequência.<br/>                                    |
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                                                                 |
| <dl> <dt>**VFW \_ \_ ENUM \_ FORA DE \_ \_ SINCRONIA**</dt> </dl> | O estado do pino foi alterado e agora está inconsistente com o enumerador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CEnumMediaTypes**](cenummediatypes.md)
</dt> </dl>

 

 




