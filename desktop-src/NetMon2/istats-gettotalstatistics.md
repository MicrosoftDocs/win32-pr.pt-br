---
description: O método GetTotalStatistics recupera o total de estatísticas para a captura atual.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'Método IStats:: GetTotalStatistics (Netmon. h)'
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
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770143"
---
# <a name="istatsgettotalstatistics-method"></a>Método IStats:: GetTotalStatistics

O método **GetTotalStatistics** recupera o [*total de estatísticas*](t.md) para a [*captura*](c.md)atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpStats* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura de [estatísticas](statistics.md)que fornece o total de estatísticas para a captura. É responsabilidade do chamador alocar e liberar a memória usada pela estrutura de **estatísticas** .

</dd> <dt>

*fClearAfterReading* \[ no\]
</dt> <dd>

Sinalizador usado para informar Monitor de Rede como lidar com o armazenamento interno do total de estatísticas. Uma configuração de TRUE informa Monitor de Rede para limpar o armazenamento interno do total de estatísticas depois que as informações atuais são recuperadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>   | O NPP não está conectado à rede. Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ \_ somente não estatísticas \_**</dt> </dl> | O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .<br/>                                |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl>   | O NPP não está capturando dados. Chame o método [IStats:: Start](istats-start.md) para iniciar a captura de dados.<br/>                         |



 

## <a name="remarks"></a>Comentários

Esse método retorna dados somente enquanto uma captura está em andamento, incluindo enquanto a captura é pausada.

Monitor de Rede também armazena [*Estatísticas de conversa*](c.md), que podem ser recuperadas chamando o método [IStats:: GetConversationStatistics](istats-getconversationstatistics.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats:: conectar](istats-connect.md)
</dt> <dt>

[IStats::GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStats:: Iniciar,](istats-start.md)
</dt> <dt>

[ESTATÍSTICA](statistics.md)
</dt> </dl>

 

 




