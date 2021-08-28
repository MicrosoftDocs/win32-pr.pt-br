---
description: O método NotifyMediaType informa o objeto do tipo de mídia atual.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Método CImageAllocator.NotifyMediaType (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de8630d4189ccbbf0d90b402ebeda6b785192c098aaa1e6d29c8c2a2dac2a3d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688316"
---
# <a name="cimageallocatornotifymediatype-method"></a>Método CImageAllocator.NotifyMediaType

O `NotifyMediaType` método informa o objeto do tipo de mídia atual.

## <a name="syntax"></a>Sintaxe


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMediaType* 
</dt> <dd>

Ponteiro para um [**objeto CMediaType**](cmediatype.md) ou **NULL** para limpar o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O filtro de propriedade deve chamar esse método sempre que o tipo de mídia mudar. Normalmente, isso ocorre quando o pino se conecta pela primeira vez e após uma alteração de formato dinâmico. O alocador usa o tipo de mídia para validar as propriedades do alocador propostas e também quando cria exemplos de mídia.

O **objeto CImageAllocator** armazena o *ponteiro pMediaType* na **variável de membro m \_ pMediaType.** Portanto, se o chamador precisar liberar o objeto **CMediaType,** ele deverá atualizar o alocador chamando esse método novamente, com um novo ponteiro ou com um **valor NULL.** Caso contrário, um erro poderá ocorrer quando o alocador tentar referenciar o ponteiro antigo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




