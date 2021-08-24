---
description: Método IStats::GetTotalStatistics – o método GetTotalStatistics recupera as estatísticas totais da captura atual.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: Método IStats::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7c98d947ad81dd1f2dc3e0dd19de144729ea8a069aefc12a820548aaeac4d15d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742656"
---
# <a name="istatsgettotalstatistics-method"></a>Método IStats::GetTotalStatistics

O **método GetTotalStatistics** recupera as [*estatísticas totais*](t.md) da captura [*atual.*](c.md)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Ponteiro para uma [estrutura STATISTICS](statistics.md)que fornece as estatísticas totais para a captura. É responsabilidade do chamador alocar e liberar a memória usada pela **estrutura STATISTICS.**

</dd> <dt>

*fClearAfterReading* \[ Em\]
</dt> <dd>

Sinalizador usado para Monitor de Rede como lidar com o armazenamento interno das estatísticas totais. Uma configuração de TRUE Monitor de Rede limpar o armazenamento interno das estatísticas totais depois que as informações atuais são recuperadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NÃO \_ CONECTADO**</dt> </dl>   | O NPP não está conectado à rede. Chame o [método IStats::Conexão](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ NÃO \_ APENAS \_ ESTATÍSTICAS**</dt> </dl> | O NPP está conectado à rede, mas não ao método [IStats::Conexão.](istats-connect.md)<br/>                                |
| <dl> <dt>**NMERR \_ NÃO CAPTURA \_**</dt> </dl>   | O NPP não está capturando dados. Chame o [método IStats::Start](istats-start.md) para iniciar a captura de dados.<br/>                         |



 

## <a name="remarks"></a>Comentários

Esse método retorna dados somente enquanto uma captura está em andamento, incluindo enquanto a captura está em pausa.

Monitor de Rede também armazena [*estatísticas*](c.md)de conversa , que podem ser recuperadas chamando o método [IStats::GetConversationStatistics.](istats-getconversationstatistics.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats::Conexão](istats-connect.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats::Start,](istats-start.md)
</dt> <dt>

[Estatísticas](statistics.md)
</dt> </dl>

 

 




