---
description: 'Saiba mais sobre: função JetGetBookmark'
title: Função JetGetBookmark
TOCTitle: JetGetBookmark Function
ms:assetid: 35bb481d-44a0-45d5-97e0-f36cbcc6aaab
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269221(v=EXCHG.10)
ms:contentKeyID: 32765524
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b75e40205dc25d467a010499ef0083c7ad87c47
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477962"
---
# <a name="jetgetbookmark-function"></a>Função JetGetBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetbookmark-function"></a>Função JetGetBookmark

A função **JetGetBookmark** recupera o indicador para o registro que está associado à entrada de índice na posição atual de um cursor. Esse indicador pode então ser usado para reposicionar esse cursor de volta para o mesmo registro usando [JetGoToBookmark](./jetgotobookmark-function.md).

```cpp
    JET_ERR JET_API JetGetBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvBookmark,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvBookmark*

O buffer de saída que recebe o indicador.

*cbMax*

O tamanho máximo, em bytes, do buffer de saída.

*pcbActual*

O tamanho real, em bytes, do indicador.

Se esse parâmetro for **nulo** , o tamanho real do indicador não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real do indicador ainda será retornado. Isso significa que esse número será maior do que o tamanho do buffer de saída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber o indicador inteiro. O buffer de saída foi preenchido com a maior parte do indicador que couber. O tamanho real do indicador também foi retornado, se solicitado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>A operação não pode ser concluída porque toda a atividade da instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>A operação não pode ser concluída porque a instância associada à sessão encontrou um erro fatal que requer que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong> esses valores de retorno são introduzidos no Windows XP.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado após o último registro no índice atual.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>A operação não pode ser concluída porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong> esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância associada à sessão está sendo desligada.</p> | 



Se essa função for realizada com sucesso, o indicador do registro associado à entrada de índice na posição atual de um cursor será retornado no buffer de saída. Nenhuma alteração no estado do banco de dados ocorrerá.

Se essa função falhar, o estado do buffer de saída e o tamanho real do indicador serão indefinidos, a menos que JET_errBufferTooSmall seja retornado. No caso em que JET_errBufferTooSmall for retornado, o buffer de saída conterá a maior parte do indicador que se ajustará no espaço fornecido e o tamanho real do indicador será preciso. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Os indicadores geralmente devem ser tratados como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as seguintes condições são verdadeiras de todos os indicadores de ESENT:

  - Um indicador identifica exclusivamente um registro em uma determinada tabela.

  - O indicador de um registro não será alterado durante o tempo de vida desse registro.

  - O indicador de um registro é o mesmo que a chave desse registro no índice primário na tabela que contém esse registro. Se nenhum índice primário for definido nessa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.

  - Os indicadores podem ser comparados entre si usando a função [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário na tabela dos registros de origem. Se nenhum índice primário for definido nessa tabela, não será significativo usar a ordenação relativa de indicadores dessa tabela.

  - Não há sentido comparar indicadores de registros de tabelas diferentes entre si.

  - um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento, antes do Windows Vista.
    
**Windows Vista:** no Windows Vista e versões posteriores, os indicadores podem ser maiores do que JET_cbBookmarkMost (256) bytes. O tamanho máximo de um indicador é igual ao valor atual de JET_paramKeyMost + 1.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGoToBookmark](./jetgotobookmark-function.md)  
[JetStopService](./jetstopservice-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
