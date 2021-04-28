---
description: 'Método IDelaydC:: GetConversationStatistics – o método GetConversationStatistics recupera informações de sessão e de estação sobre a captura atual.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'Método IDelaydC:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d4d4c1bb1ad7ecb45b640c16322e297f9f640ef1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103804"
---
# <a name="idelaydcgetconversationstatistics-method"></a>Método IDelaydC:: GetConversationStatistics

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

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                   | Descrição                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>          | O NPP não está conectado à rede. Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.<br/>                                                                                                  |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>          | O NPP não está capturando dados. Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ não \_ atrasada**</dt> </dl>            | O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ sem \_ Estatísticas de conversa \_**</dt> </dl> | A configuração dessa conexão é definida para não salvar as estatísticas de conversa. Para salvar as estatísticas de conversa, pare a captura, defina NoConversationStats = YES no BLOB de configuração e reinicie a captura.<br/> |



 

## <a name="remarks"></a>Comentários

Este método só pode ser chamado quando a captura de dados está em andamento; Quando a captura atual for pausada, as chamadas para esse método não serão realizadas com sucesso. Para iniciar uma captura, chame o método [IDelaydC:: Start](idelaydc-start.md) .

Para recuperar outros tipos de estatísticas, chame [IDelaydC:: GetTotalStatistics](idelaydc-gettotalstatistics.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC:: iniciar](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




