---
description: 'Saiba mais sobre: função JetGetCurrentIndex'
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
ms.openlocfilehash: 82f24afb4d8e36d95d6e3be480f32358c1c5dba2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468303"
---
# <a name="jetgetcurrentindex-function"></a>Função JetGetCurrentIndex


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetcurrentindex-function"></a>Função JetGetCurrentIndex

A função **JetGetCurrentIndex** determina o nome do índice atual de um determinado cursor. Esse nome também é usado posteriormente para selecionar novamente esse índice como o índice atual usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md). Ele também pode ser usado para descobrir as propriedades desse índice usando [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).

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

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*szIndexName*

O buffer de saída que recebe o nome do índice atual do cursor.

*cchIndexName*

O tamanho máximo em caracteres do buffer de saída.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber o nome inteiro do índice.</p><p>O buffer de saída foi preenchido com a maior parte do nome do índice que se ajustaria. Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres nesse buffer de saída será terminada em nulo.</p><p><strong>Observação  </strong> Esse erro não será retornado se cchIndexName for zero. Consulte a seção comentários para obter mais informações.</p> | 



Em caso de sucesso, o nome do índice atual do cursor fornecido será retornado no buffer de saída. Se JET_wrnBufferTruncated for retornado, o buffer de saída conterá a maior parte do nome do índice que se ajustará no espaço fornecido. Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres retornada nesse buffer será terminada em nulo. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o estado do buffer de saída será indefinido. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se não houver um índice atual para o cursor, uma cadeia de caracteres vazia será retornada. Isso pode acontecer quando o cursor está no índice clusterizado da tabela e nenhum índice primário foi definido. Esse índice é conhecido como o índice sequencial da tabela e não tem definição. Em qualquer caso, definir o índice atual como uma cadeia de caracteres vazia usando [JetSetCurrentIndex](./jetsetcurrentindex-function.md) selecionará o índice clusterizado, independentemente da presença de uma definição de índice primário.

Há um bug importante nessa função que está presente em todas as versões. Se o buffer de saída for muito pequeno para receber o nome inteiro do índice e o buffer de saída tiver pelo menos um caractere de comprimento, JET_wrnBufferTruncated não será retornado. JET_errSuccess será retornado em seu lugar. Para evitar esse problema, o buffer de saída deve ser sempre pelo menos JET_cbNameMost + 1 (65) caracteres de comprimento.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetCurrentIndexW</strong> (Unicode) e <strong>JetGetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetSetCurrentIndex](./jetsetcurrentindex-function.md)
