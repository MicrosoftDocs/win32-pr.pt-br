---
description: O método GetCurrentFormat recupera o formato de mídia do fluxo atual.
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'Método ITFormatControl:: GetCurrentFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50d261cd88a9aac4998f15d871a20408aecb367b793b78b7f9fcaeff452273a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140329"
---
# <a name="itformatcontrolgetcurrentformat-method"></a>Método ITFormatControl:: GetCurrentFormat

\[esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **GetCurrentFormat** recupera o formato de mídia do fluxo atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppMediaType* \[ fora\]
</dt> <dd>

Ponteiro para um descritor de **\_ \_ tipo de mídia am** do formato de terminal. Para obter mais informações sobre o **\_ \_ tipo de mídia am**, consulte a documentação do DirectX.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> </dl>

 

 




