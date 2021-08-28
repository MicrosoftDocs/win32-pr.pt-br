---
description: 'Saiba mais sobre: Função JetGetCurrentIndex'
title: Função JetGetCurrentIndex
TOCTitle: JetGetCurrentIndex Function
ms:assetid: 9db3b875-0b95-4027-9742-c36d2d7e64cf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294041(v=EXCHG.10)
ms:contentKeyID: 32765642
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetCurrentIndexW
- JetGetCurrentIndex
- JetGetCurrentIndexA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6f41114c74643d7165bc16363af3d1777828003b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987679"
---
# <a name="jetgetcurrentindex-function"></a>Função JetGetCurrentIndex


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetcurrentindex-function"></a>Função JetGetCurrentIndex

A **função JetGetCurrentIndex** determina o nome do índice atual de um determinado cursor. Esse nome também é usado para selecionar esse índice mais tarde como o índice atual usando [JetSetCurrentIndex.](./jetsetcurrentindex-function.md) Ele também pode ser usado para descobrir as propriedades desse índice usando [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

```cpp
    JET_ERR JET_API JetGetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_PSTR szIndexName,
      __in          unsigned long cchIndexName
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*szIndexName*

O buffer de saída que recebe o nome do índice atual do cursor.

*cchIndexName*

O tamanho máximo em caracteres do buffer de saída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber todo o nome do índice.</p><p>O buffer de saída foi preenchido com o máximo de nome do índice que caberia. Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres nesse buffer de saída será terminada em nulo.</p><p><strong>Observação  </strong> Esse erro não será retornado se cchIndexName for zero. Consulte a seção Comentários para obter mais informações.</p> | 



Em caso de êxito, o nome do índice atual do cursor determinado será retornado no buffer de saída. Se JET_wrnBufferTruncated for retornado, o buffer de saída conterá tanto do nome do índice quanto se ajustará ao espaço fornecido. Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres retornada nesse buffer será terminada em nulo. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o estado do buffer de saída será indefinido. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se não houver nenhum índice atual para o cursor, uma cadeia de caracteres vazia será retornada. Isso pode acontecer quando o cursor está no índice clusterado da tabela e nenhum índice primário foi definido. Esse índice é conhecido como o índice sequencial da tabela e não tem nenhuma definição. Em qualquer caso, definir o índice atual como uma cadeia de caracteres vazia usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md) selecionará o índice clustered, independentemente da presença de uma definição de índice primário.

Há um bug importante nessa função que está presente em todas as versões. Se o buffer de saída for muito pequeno para receber todo o nome do índice e o buffer de saída tiver pelo menos um caractere de comprimento, JET_wrnBufferTruncated NÃO será retornado. JET_errSuccess será retornado. Para evitar esse problema, o buffer de saída sempre deve ter pelo menos JET_cbNameMost + 1 (65) caracteres de comprimento.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetCurrentIndexW</strong> (Unicode) e <strong>JetGetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
