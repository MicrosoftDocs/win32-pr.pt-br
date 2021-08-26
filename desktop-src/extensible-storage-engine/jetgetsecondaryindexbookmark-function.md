---
description: 'Saiba mais sobre: Função JetGetSecondaryIndexBookmark'
title: Função JetGetSecondaryIndexBookmark
TOCTitle: JetGetSecondaryIndexBookmark Function
ms:assetid: 6953eda4-9420-4814-80f4-eb9e3e5540d8
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269285(v=EXCHG.10)
ms:contentKeyID: 32765577
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a27d34b2622c5fe4ce2c72e3781394457e9cc20
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472513"
---
# <a name="jetgetsecondaryindexbookmark-function"></a>Função JetGetSecondaryIndexBookmark


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetsecondaryindexbookmark-function"></a>Função JetGetSecondaryIndexBookmark

A **função JetGetSecondaryIndexBookmark** recupera um indicador especial para a entrada de índice secundário na posição atual de um cursor. Esse indicador pode ser usado para reposicionar com eficiência esse cursor de volta para a mesma entrada de índice usando [JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md). Isso é mais útil ao reposicionar em um índice secundário que contém chaves duplicadas ou que contém várias entradas de índice para o mesmo registro.

**Windows XP: JetGetSecondaryIndexBookmark** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetGetSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKeyMax,
      __out_opt     unsigned long* pcbSecondaryKeyActual,
      __out_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmarkMax,
      __out_opt     unsigned long* pcbPrimaryKeyActual,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*pvSecondaryKey*

O buffer de saída que recebe a chave secundária.

*cbSecondaryKeyMax*

O tamanho máximo, em bytes, do buffer de saída para a chave secundária.

*pcbSecondaryKeyActual*

Recebe o tamanho real em bytes da chave secundária.

Se esse parâmetro for NULL, o tamanho real da chave secundária não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real da chave secundária ainda será retornado. Isso significa que esse número será maior que o tamanho do buffer de saída.

*pvPrimaryBookmark*

O buffer de saída que recebe o indicador de chave primária.

*cbPrimaryBookmarkMax*

O tamanho máximo, em bytes, do buffer de saída para o indicador de chave primária.

*pcbPrimaryKeyActual*

Recebe o tamanho real, em bytes, do indicador de chave primária.

Se esse parâmetro for NULL, o tamanho real do indicador de chave primária não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real do indicador de chave primária ainda será retornado. Isso significa que esse número será maior que o tamanho do buffer de saída.

*grbit*

Reservado para uso futuro.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>A operação foi concluída com êxito, mas um dos buffers de saída era muito pequeno para receber os dados solicitados.</p><p>O buffer de saída foi preenchido com o máximo de indicadores que caberia. O tamanho real do indicador também foi retornado, se solicitado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>O cursor não está atualmente em um índice secundário.</p><p>Não é significativo recuperar um indicador de índice secundário quando o cursor não está usando um índice secundário no momento. <a href="gg269221(v=exchg.10).md">JetGetBookmark</a> deve ser usado quando o cursor não está em um índice secundário.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está posicionado em um registro.</p><p>Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, o indicador de índice secundário para a entrada de índice na posição atual de um cursor será retornado nos buffers de saída. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o estado dos buffers de saída e o tamanho real do indicador de índice secundário serão indefinido, a menos que JET_errBufferTooSmall tenha sido retornado. No caso de JET_errBufferTooSmall retornado, os buffers de saída conterão a maior parte do indicador de índice secundário que se ajustará ao espaço fornecido e o tamanho real do indicador de índice secundário será preciso. Em qualquer caso, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Os indicadores geralmente devem ser tratados como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as propriedades a seguir podem ser conhecidas sobre todos os indicadores ESENT:

  - Um indicador identifica exclusivamente um registro em uma determinada tabela.

  - O indicador de um registro não será altere durante o tempo de vida desse registro.

  - O indicador de um registro é o mesmo que a chave desse registro no índice primário sobre a tabela que contém esse registro. Se nenhum índice primário for definido sobre essa tabela, o mecanismo de banco de dados criará seu próprio indicador para o registro.

  - Indicadores podem ser comparados uns com os outros usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice primário sobre a tabela dos registros de origem. Se nenhum índice primário for definido sobre essa tabela, a ordenação relativa de indicadores dessa tabela não será significativa.

  - Não faz sentido comparar indicadores de registros de tabelas diferentes entre si.

  - Um indicador é sempre menor ou igual a JET_cbBookmarkMost (256) bytes de comprimento antes do Windows Vista. No Windows Vista e versões posteriores, os indicadores podem ser maiores. O tamanho máximo de um indicador é igual ao valor atual de JET_paramKeyMost + 1.

As chaves geralmente devem ser tratadas como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as propriedades a seguir podem ser conhecidas sobre todas as chaves ESENT:

  - As chaves podem ser comparadas entre si usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice de origem na tabela das entradas do índice de origem.

  - Não faz sentido comparar chaves de entradas de índice de índices diferentes entre si.

  - Uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes Windows Vista. No Windows Vista e versões posteriores, as chaves podem ser maiores. O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetBookmark](./jetgetbookmark-function.md)  
[JetGotoSecondaryIndexBookmark](./jetgotosecondaryindexbookmark-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60))
