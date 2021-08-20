---
description: 'Saiba mais sobre: Função JetSetCurrentIndex'
title: Função JetSetCurrentIndex
TOCTitle: JetSetCurrentIndex Function
ms:assetid: a2a15eab-b8bf-4a67-a63a-830ed1fdb3d9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294046(v=EXCHG.10)
ms:contentKeyID: 32765645
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex
- JetSetCurrentIndexA
- JetSetCurrentIndexW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0418665851bc1f4cf5d8e7df6b7c696d4458b869
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481242"
---
# <a name="jetsetcurrentindex-function"></a>Função JetSetCurrentIndex


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetcurrentindex-function"></a>Função JetSetCurrentIndex

A **função JetSetCurrentIndex** pode ser usada para definir o índice atual de um cursor. O índice atual de um cursor define quais registros em uma tabela são visíveis para esse cursor e a ordem na qual eles aparecem selecionando o conjunto de entradas de índice a ser usado para expor esses registros.

```cpp
    JET_ERR JET_API JetSetCurrentIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const tchar* szIndexName
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*szIndexName*

O nome do índice a ser selecionado para o cursor.

Se esse parâmetro for NULL ou uma cadeia de caracteres vazia, o índice clustered será selecionado. Se um índice primário for definido para a tabela, esse índice será selecionado porque é o mesmo que o índice cluster. Se nenhum índice primário for definido para a tabela, o índice sequencial será selecionado. O índice sequencial não tem nenhuma definição de índice. Consulte [JetCreateIndex para](./jetcreateindex-function.md) obter mais informações.

Se *pindexid* não for NULL, o nome do índice será ignorado e o índice será selecionado por sua ID de índice.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhum valor para a primeira coluna de chave com valor múltiplo na definição do novo índice que corresponda ao número de sequência especificado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInvalidIndexId</p> | <p>O conteúdo da ID do índice não era válido ou expirou e precisa ser atualizado. Isso pode acontecer para <strong>JetSetCurrentIndex</strong> quando:</p><ul><li><p>pindexid- cbStruct não é do tamanho esperado &gt; (Windows Server 2003 e versões posteriores).</p></li><li><p>O mecanismo foi desligado desde que a ID do índice foi buscada.</p></li><li><p>Todos os cursores que referenciam a tabela que contém o índice correspondente à ID do índice foram fechados e o mecanismo ressaltou a definição desse índice do cache de esquema.</p></li><li><p>A ID do índice está sendo usada com um cursor aberto na tabela errada.</p></li><li><p>O índice foi descartado ou ainda não está visível para a sessão.</p></li></ul> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidName</p> | <p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p><ul><li><p>Os nomes de objeto devem ser compostos de caracteres ASCII.</p></li><li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li><li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li><li><p>Os nomes de objeto podem não começar com um espaço.</p></li><li><p>Os nomes de objeto podem não conter caracteres de controle ASCII (0x00 por meio 0x1F).</p></li><li><p>Os nomes de objeto podem não conter um ponto de exclamação (!), ponto (.), colchete esquerdo ([) ou um caractere de colchete direito (]).</p></li><li><p>Depois de validada, somente a parte da cadeia de caracteres até o primeiro espaço (se algum) será usada para o nome do objeto. Isso significa efetivamente que os nomes de objeto também podem não conter um espaço.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetSetCurrentIndex</strong> quando <em>pindexid</em> não é NULL e pindexid- cbStruct não é do tamanho esperado (Windows XP e &gt; versões anteriores).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhuma entrada de índice no novo índice que corresponda ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfCursors</p> | <p>O mecanismo esgota seu pool de recursos usados para abrir cursores. O número máximo de cursores que podem ser abertos a qualquer momento é controlado usando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obter mais informações. Isso pode acontecer para <strong>JetSetCurrentIndex</strong> quando um índice secundário tiver sido selecionado e o mecanismo não puder abrir um cursor interno para usar esse índice.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 



Em caso de êxito, o índice atual do cursor é definido como o índice solicitado. As entradas de índice agora podem ser procuradas [usando JetSeek](./jetseek-function.md) de acordo com a definição de índice do índice solicitado. Entradas de índice também podem ser enumeradas [usando JetMove](./jetmove-function.md) na ordem especificada por essa definição de índice. A posição atual do cursor é definida como a primeira entrada de índice no índice (JET_bitMoveFirst) ou para uma entrada de índice específica relacionada à posição atual do cursor no índice antigo (JET_bitNoMove). Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o índice atual e a posição atual do cursor estão em um estado indefinido. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se a dica de ID de índice estiver desleilada, a API simplesmente falhará. Não há nenhum fallback para o nome de texto do índice, nesse caso, como se pode esperar. Esse fallback deve ser feito manualmente pelo chamador da API.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetSetCurrentIndexW</strong> (Unicode) e <strong>JetSetCurrentIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXID](./jet-indexid-structure.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetGetCurrentIndex](./jetgetcurrentindex-function.md)  
[JetGetIndexInfo](./jetgetindexinfo-function.md)  
[JetGetTableIndexInfo](./jetgettableindexinfo-function.md)  
[JetMove](./jetmove-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetCurrentIndex]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)
