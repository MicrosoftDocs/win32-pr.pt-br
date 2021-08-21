---
description: 'Saiba mais sobre: parâmetros de retorno de chamada'
title: Parâmetros de retorno de chamada
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7b904c090852ea3990ac78e37a7ca851e152968
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465213"
---
# <a name="callback-parameters"></a>Parâmetros de retorno de chamada


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="callback-parameters"></a>Parâmetros de retorno de chamada

Este tópico contém parâmetros que são usados para retornos de chamada.

*JET_paramDisableCallbacks*  
65  

Esse parâmetro desabilita todos os retornos de chamada do mecanismo de banco de dados para as funções fornecidas pelo aplicativo. Ele destina-se principalmente a dar suporte aos utilitários do mecanismo de banco de dados e não deve ser usado em seu aplicativo.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

Esse parâmetro habilita o uso de retornos de chamada persistentes no banco de dados. em versões anteriores ao Windows Vista, o uso de retornos de chamada persistentes foi habilitado por padrão. Agora, os aplicativos devem habilitar explicitamente o uso de retornos de chamada persistentes em tempo de execução usando esse parâmetro. Se esse parâmetro não for definido, qualquer operação de banco de dados que exija a invocação de um retorno de chamada falhará com JET_errCallbackFailed. Esse parâmetro não afeta nenhum retorno de chamada especificado em tempo de execução com os seguintes mecanismos: JET_paramRuntimeCallback, [JetRegisterCallback](./jetregistercallback-function.md)ou um parâmetro de retorno de chamada explícito para uma API do Jet. Ainda é possível criar elementos de esquema que contenham retornos de chamada persistentes mesmo quando o uso desses retornos de chamada persistentes não é permitido. Quando esse parâmetro é definido como false, ele substitui JET_paramDisableCallbacks.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e versões posteriores</p> | 



*JET_paramRuntimeCallback*  
73  

Esse parâmetro configura o mecanismo com uma função de retorno de chamada de tempo de execução implementando a interface [JET_CALLBACK](./jet-callback-callback-function.md) . Esse retorno de chamada pode ser chamado pelos seguintes motivos: [JET_cbtypFreeCursorLS](./jet-cbtyp.md), [JET_cbtypFreeTableLS](./jet-cbtyp.md)ou [JET_cbtypNull](./jet-cbtyp.md). Consulte [JetSetLS](./jetsetls-function.md) para obter mais informações.


| | | <p>Valor padrão:</p> | <p>NULO</p> | | <p>Tipo:</p> | <p>Ponteiro de função (JET_API_PTR)</p> | | <p>Intervalo válido:</p> | <p>NULL, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
