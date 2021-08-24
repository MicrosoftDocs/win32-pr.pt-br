---
description: Método IDelaydC::GetConversationStatistics – o método GetConversationStatistics recupera informações de sessão e estação sobre a captura atual.
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: Método IDelaydC::GetConversationStatistics (Netmon.h)
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
ms.openlocfilehash: 60fc768a1b93a752a91d431e79fb3e875416ac2b82b2bad5603e3d4cddaccbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910566"
---
# <a name="idelaydcgetconversationstatistics-method"></a>Método IDelaydC::GetConversationStatistics

O **método GetConversationStatistics** recupera informações [*de*](s.md) sessão e [*estação*](s.md) sobre a captura atual.

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

*nSessions* \[ out\]
</dt> <dd>

Ponteiro para um DWORD que contém o número de [*sessões registradas*](s.md) para a captura atual.

</dd> <dt>

*lpSessionStats* \[ out\]
</dt> <dd>

Ponteiro para uma [estrutura SESSIONSTATS.](sessionstats.md)

</dd> <dt>

*n Estações* \[ out\]
</dt> <dd>

Ponteiro para um DWORD que contém o número de [*estações registradas*](s.md) para a captura atual.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Ponteiro para uma [estrutura STATIONSTATS.](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ Em\]
</dt> <dd>

Sinalizador usado para Monitor de Rede limpar o armazenamento interno das estruturas [SESSIONSTATS](sessionstats.md) e [STATIONSTATS](stationstats.md) depois de recuperar as informações atuais.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                   | Descrição                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>          | O NPP não está conectado à rede. Chame [IDelaydC::Conexão](idelaydc-connect.md) para conectar o NPP à rede.<br/>                                                                                                  |
| <dl> <dt>**NMERR \_ NÃO CAPTURA \_**</dt> </dl>          | O NPP não está capturando dados. Chame [IDelaydC::Start](idelaydc-start.md) para iniciar a captura.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ NÃO \_ ATRASADO**</dt> </dl>            | O NPP está conectado à rede, mas não ao [método IDelaydC::Conexão.](idelaydc-connect.md)<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ SEM ESTATÍSTICAS DE \_ \_ CONVERSA**</dt> </dl> | A configuração dessa conexão está definida para não salvar estatísticas de conversa. Para salvar as estatísticas de conversa, pare a captura, de definir NoConversationStats = YES no BLOB de configuração e reinicie a captura.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método só pode ser chamado enquanto a captura de dados está em andamento; quando a captura atual estiver em pausa, as chamadas para esse método não serão bem-sucedidas. Para iniciar uma captura, chame o [método IDelaydC::Start.](idelaydc-start.md)

Para recuperar outros tipos de estatísticas, chame [IDelaydC::GetTotalStatistics.](idelaydc-gettotalstatistics.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conexão](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




