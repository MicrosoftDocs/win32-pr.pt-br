---
description: 'Saiba mais sobre: Função JetSetColumns'
title: Função JetSetColumns
TOCTitle: JetSetColumns Function
ms:assetid: a5b011dc-0da6-44bf-aaf5-352d8a57e5bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294050(v=EXCHG.10)
ms:contentKeyID: 32765649
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumns
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a62c3fee0b961268c11974e0a6064f091474d34
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984339"
---
# <a name="jetsetcolumns-function"></a>Função JetSetColumns


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetcolumns-function"></a>Função JetSetColumns

A **função JetSetColumns** é semelhante em comportamento a [JetSetColumn,](./jetsetcolumn-function.md) mas permite que um aplicativo de definir vários valores de coluna em uma única operação. Uma matriz de [JET_SETCOLUMN](./jet-setcolumn-structure.md) estruturas é usada para descrever o conjunto de valores de coluna a serem definidos e para descrever buffers de entrada para cada valor de coluna a ser definido.

```cpp
    JET_ERR JET_API JetSetColumns(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_out_opt  JET_SETCOLUMN* psetcolumn,
      __in          unsigned long csetcolumn
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*psetcolumn*

Um ponteiro para uma matriz de uma ou mais [JET_SETCOLUMN](./jet-setcolumn-structure.md) estruturas. Cada estrutura inclui descrições de qual valor de coluna definir e de onde obter dados de coluna a definir.

*csetcolumn*

O número de [JET_SETCOLUMN](./jet-setcolumn-structure.md) estruturas na matriz fornecidas por *psetcolumn*.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errBadColumnId</p> | <p>A ID da coluna determinada está fora dos limites legais de uma ID de coluna.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnIllegalNull</p> | <p>O mesmo que JET_errNullInvalid.</p> | 
| <p>JET_errColumnNotFound</p> | <p>A coluna descrita pelo <em>columnid</em> determinado não existe na tabela.</p> | 
| <p>JET_errColumnNotUpdatable</p> | <p>Foi feita uma tentativa ilegal de atualizar um valor longo durante uma operação de exclusão de cópia de inserção original.</p> | 
| <p>JET_errColumnTooBig</p> | <p>Os dados de valor de coluna determinados no buffer de entrada excedem a limitação de tamanho natural para uma coluna de comprimento fixo ou configurados para texto de comprimento fixo ou colunas binárias. Esse erro também é retornado ao passar mais de 1024 bytes de dados para uma coluna longa e definir o sinalizador JET_bitSetIntrinsicLV dados.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>O tamanho dos dados de valor de coluna determinado não corresponderá ao que é natural para o tipo de dados de comprimento fixo.</p> | 
| <p>JET_errInvalidColumnType</p> | <p>Foi feita uma tentativa ilegal de atualizar uma coluna de incremento automático durante uma operação de inserção ou atualização ou para atualizar uma coluna de versão durante uma operação de substituição.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bits conhecidas.</p> | 
| <p>JET_errInvalidParameter</p> | <p>O &gt; psetinfo-cbStruct determinado não é um tamanho válido para a <a href="gg294090(v=exchg.10).md">estrutura JET_SETINFO</a> dados.</p> | 
| <p>JET_errMultiValuedDuplicate</p> | <p>A operação definir coluna tentou criar um valor duplicado e especificou JET_bitSetUniqueMultiValues ou JET_bitSetUniqueNormalizedMultiValues.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errNotInTransaction</p> | <p>Foi feita uma tentativa ilegal de atualizar um valor de coluna longo quando a sessão de chamada não estava em uma transação.</p> | 
| <p>JET_errNullInvalid</p> | <p>Foi feita uma tentativa ilegal de definir uma coluna não NULL como NULL.</p> | 
| <p>JET_errRecordTooBig</p> | <p>O valor da coluna não pôde ser definido como o valor no buffer de entrada porque ele teria feito com que o registro excedesse sua limitação de tamanho relacionado ao tamanho da página. Colunas do tipo <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a> <a href="gg269213(v=exchg.10).md">ou JET_coltypLongBinary</a> podem ser armazenadas separadamente dos dados de registro restantes. No entanto, outras colunas devem ser armazenadas com o registro e podem fazer com que a limitação de tamanho do registro seja excedida. Até mesmo colunas longas exigem 5 bytes de espaço dentro do registro como uma vinculação e isso também pode levar a JET_errRecordTooBig ser retornado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errUpdateNotPrepared</p> | <p>O cursor não está atualmente no processo de inserir um novo registro ou atualizar um registro existente.</p> | 
| <p>JET_wrnColumnMaxTruncated</p> | <p>O valor da coluna no buffer de entrada excedeu o comprimento máximo configurado para uma coluna de comprimento variável e foi truncado.</p> | 



Em caso de sucesso, para cada coluna descrita nas psetcolumns, a parte desejada do valor da coluna é definida com os dados copiados do buffer de entrada. O conjunto de dados de coluna pode ter sido truncado se excedeu o comprimento máximo especificado para uma coluna de comprimento variável.

Em caso de falha, o local do cursor permanece inalterado e nenhum dado de valor de coluna é atualizado no buffer de cópia.

#### <a name="remarks"></a>Comentários

Se qualquer operação de coluna de conjunto individual retornar um erro, toda a **operação JetSetColumns** retornará um erro. Avisos, em geral, são retornados no erro psetcolumns- e não no \> código de retorno dessa função. No entanto, se o último conjunto de colunas tiver um aviso, esse aviso será retornado do **próprio JetSetColumns.**

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SETCOLUMN](./jet-setcolumn-structure.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)  
[JetSetColumn](./jetsetcolumn-function.md)
