---
description: 'Método IRTC:: GetTotalStatistics – o método GetTotalStatistics recupera o total de estatísticas para a captura atual.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'Método IRTC:: GetTotalStatistics (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110684"
---
# <a name="irtcgettotalstatistics-method"></a>Método IRTC:: GetTotalStatistics

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

Ponteiro para uma estrutura de [estatísticas](statistics.md) que fornece o total de estatísticas para a captura. É responsabilidade dos chamadores alocar e liberar a memória usada pela estrutura de **estatísticas** .

</dd> <dt>

*fClearAfterReading* \[ no\]
</dt> <dd>

Sinalizador usado para informar Monitor de Rede como lidar com o armazenamento interno do total de estatísticas. Uma configuração de **true** informa monitor de rede para limpar o armazenamento interno do total de estatísticas depois que as informações atuais são recuperadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede. Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.<br/> |
| <dl> <dt>**NMERR \_ não está em \_ tempo real**</dt> </dl>  | O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .<br/>                     |
| <dl> <dt>**NMERR \_ não \_ capturando**</dt> </dl> | O NPP não está capturando dados. Chame [IRTC:: Start](irtc-start.md) para iniciar a captura de dados.<br/>                         |



 

## <a name="remarks"></a>Comentários

Esse método retorna dados somente enquanto uma captura está em andamento, incluindo enquanto a captura é pausada.

Monitor de Rede também armazena [*Estatísticas de conversa*](c.md). Para recuperar as estatísticas de conversa, chame o método [IRTC:: GetConversationStatistics](irtc-getconversationstatistics.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: conectar](irtc-connect.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC:: iniciar](irtc-start.md)
</dt> <dt>

[ESTATÍSTICA](statistics.md)
</dt> </dl>

 

 




