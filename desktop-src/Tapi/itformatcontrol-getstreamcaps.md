---
description: O método GetStreamCaps recupera os recursos associados a um determinado índice de formato.
ms.assetid: 4c375369-51d9-44ac-a8f0-c2a96fc10805
title: 'Método ITFormatControl:: GetStreamCaps (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1ccaf825912e53eafb5112f14ed369f999959a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782912"
---
# <a name="itformatcontrolgetstreamcaps-method"></a>Método ITFormatControl:: GetStreamCaps

\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **GetStreamCaps** recupera os recursos associados a um determinado índice de formato.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStreamCaps(
  [in]  DWORD                   dwIndex,
  [out] AM_MEDIA_TYPE           **ppMediaType,
  [out] TAPI_STREAM_CONFIG_CAPS *pStreamConfigCaps,
  [out] BOOL                    *pfEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ no\]
</dt> <dd>

Índice do formato que está sendo investigado.

</dd> <dt>

*ppMediaType* \[ fora\]
</dt> <dd>

Ponteiro para um descritor de **\_ \_ tipo de mídia am** do formato de terminal. Para obter mais informações sobre o **\_ \_ tipo de mídia am**, consulte a documentação do DirectX.

</dd> <dt>

*pStreamConfigCaps* \[ fora\]
</dt> <dd>

Uma [**estrutura \_ \_ \_ Caps de configuração de fluxo TAPI**](tapi-stream-config-caps.md) que fornece informações detalhadas sobre os recursos de fluxo.

</dd> <dt>

*pfEnabled* \[ fora\]
</dt> <dd>

Indica se o formato associado ao índice atual está habilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**\_limites de \_ configuração de fluxo TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




