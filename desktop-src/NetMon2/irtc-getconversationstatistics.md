---
description: O método GetConversationStatistics recupera informações de sessão e de estação sobre a captura atual.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'Método IRTC:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827865"
---
# <a name="irtcgetconversationstatistics-method"></a>Método IRTC:: GetConversationStatistics

O método **GetConversationStatistics** recupera informações de [*sessão*](s.md) e de [*estação*](s.md) sobre a captura atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nSessions* \[ fora\]
</dt> <dd>

Ponteiro para um DWORD que contém o número de [*sessões*](s.md) registradas para a captura atual.

</dd> <dt>

*lpSessionStats* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura [SESSIONSTATS](sessionstats.md) .

</dd> <dt>

*nStations* \[ fora\]
</dt> <dd>

Ponteiro para um DWORD que contém o número de [*estações*](s.md) registradas para a captura atual.

</dd> <dt>

*lpStationStats* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura [STATIONSTATS](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ no\]
</dt> <dd>

Sinalizador usado para informar Monitor de Rede para limpar o armazenamento interno das estruturas [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) depois de recuperar as informações atuais.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                   | Descrição                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>          | O NPP não está conectado à rede. Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>          | O NPP não está capturando dados. Chame [IRTC:: Start](irtc-start.md) para iniciar a captura.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>           | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ sem \_ Estatísticas de conversa \_**</dt> </dl> | A configuração dessa conexão é definida para não salvar as estatísticas de conversa. Para salvar as estatísticas de conversa, pare a captura, defina NoConversationStats = YES no BLOB de configuração e reinicie a captura.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método só pode ser chamado enquanto você estiver capturando dados; Se você chamar esse método enquanto a captura atual estiver pausada, o método não terá sucesso. Para iniciar uma captura, chame o método [IRTC:: Start](irtc-start.md) .

Para recuperar outros tipos de estatísticas, chame o método [IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC:: iniciar](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




