---
description: O \_ método Get SessionVersion Obtém o valor de 32 bits (ideal protocolo NTP ou NTP) que serve como a versão da sessão.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'Método ITSdp:: get_SessionVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7661fb5f133d214748991510d56387991872fa69243353b5144623a1ef19f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476586"
---
# <a name="itsdpget_sessionversion-method"></a>Método ITSdp:: get \_ SessionVersion

\[os controles e as interfaces de conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get \_ SessionVersion** Obtém o valor de 32 bits (ideal protocolo NTP ou NTP) que serve como a versão da sessão. Embora isso seja gerado automaticamente quando a sessão é criada, o usuário é responsável por alterá-lo quando o SDP é modificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSessionVersion* \[ fora\]
</dt> <dd>

Ponteiro para o identificador de versão da sessão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *pSessionVersion* não é válido.<br/>           |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | O parâmetro *pSessionVersion* não é um ponteiro válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/>    |
| <dl> <dt>**E \_ falha**</dt> </dl>        | Erro não especificado.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método ainda não foi implementado.<br/>                     |



 

## <a name="remarks"></a>Comentários

o valor de retorno desse método pode ser **ULONG**, mas Visual Basic não dá suporte ao tipo **ULONG** . Um **Double** é o próximo menor tipo que abrange todo o intervalo de valores necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::p UT \_ SessionVersion**](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




