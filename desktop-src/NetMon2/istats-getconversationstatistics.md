---
description: Recupera as informações de sessão e de estação sobre a captura atual.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: 'Método IStats:: GetConversationStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 030fafb4ccf041c2804179f8adf0088ca3fba845
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775674"
---
# <a name="istatsgetconversationstatistics-method"></a>Método IStats:: GetConversationStatistics

O método **GetConversationStatistics** recupera informações de sessão e de estação sobre a captura atual.

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

Um ponteiro para um DWORD que contém o número de [*sessões*](s.md) registradas para a captura atual.

</dd> <dt>

*lpSessionStats* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**SESSIONSTATS**](sessionstats.md) .

</dd> <dt>

*nStations* \[ fora\]
</dt> <dd>

Um ponteiro para um DWORD que contém o número de [*estações*](s.md) registradas para a captura atual.

</dd> <dt>

*lpStationStats* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**STATIONSTATS**](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ no\]
</dt> <dd>

Sinalizador usado para instruir Monitor de Rede a limpar o armazenamento interno das estruturas [**SESSIONSTATS**](sessionstats.md) e [**STATIONSTATS**](stationstats.md) depois que os dados atuais forem recuperados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                   | Descrição                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>          | O NPP não está conectado à rede. Chame [**IStats:: Connect**](istats-connect.md) para conectar o NPP à rede.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>          | O NPP não está capturando dados. Chame [**IStats:: Start**](istats-start.md) para iniciar a captura.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl>        | O NPP está conectado à rede, mas não com o método [**IStats:: Connect**](istats-connect.md) .<br/>                                                                                                                         |
| <dl> <dt>**NMERR \_ sem \_ Estatísticas de conversa \_**</dt> </dl> | A configuração dessa conexão é definida para não salvar as estatísticas de conversa. Para salvar as estatísticas de conversa, pare a captura, defina **NoConversationStats = Yes** no blob de configuração e reinicie a captura.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado somente enquanto a captura de dados está em andamento; Quando a captura atual for pausada, uma chamada para esse método não terá sucesso.

Para iniciar uma captura, chame o método [**IStats:: Start**](istats-start.md) . Para recuperar outros tipos de estatísticas, chame [**IStats:: GetTotalStatistics**](istats-gettotalstatistics.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats:: iniciar**](istats-start.md)
</dt> <dt>

[**IStats:: conectar**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 




