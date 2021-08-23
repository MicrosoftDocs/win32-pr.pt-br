---
description: O \_ método Get TransportProtocol Obtém o protocolo de transporte.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'Método ITMedia:: get_TransportProtocol (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7927469ff00caab36ab45af12939c6f2f6518a415d4a764c3d04f9c715db75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682766"
---
# <a name="itmediaget_transportprotocol-method"></a>Método ITMedia:: get \_ TransportProtocol

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ TransportProtocol** Obtém o protocolo de transporte. Isso é especificado além do formato de mídia para que o mesmo formato de mídia padrão possa ser transportado por protocolos de transporte diferentes, mesmo quando o protocolo de rede for o mesmo, como com áudio PCM de IVA e áudio RTP PCM.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppProtocol* \[ fora\]
</dt> <dd>

Ponteiro para a representação **BSTR** do protocolo de transporte.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *ppProtocol* não é um ponteiro válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                  |



 

## <a name="remarks"></a>Comentários

O aplicativo deve usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppProtocol* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| Cabeçalho<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::p UT \_ TransportProtocol**](itmedia-put-transportprotocol.md)
</dt> </dl>

 

