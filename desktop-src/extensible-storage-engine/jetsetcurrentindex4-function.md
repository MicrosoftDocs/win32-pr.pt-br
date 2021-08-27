---
description: 'Saiba mais sobre: função JetSetCurrentIndex4'
title: Função JetSetCurrentIndex4
TOCTitle: JetSetCurrentIndex4 Function
ms:assetid: 6076d02c-5701-4021-ba0a-da36bff166d1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269262(v=EXCHG.10)
ms:contentKeyID: 32765564
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetCurrentIndex4W
- JetSetCurrentIndex4A
- JetSetCurrentIndex4
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14ace8227df7064caff249b02ec381b6ff7cb751
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476342"
---
# <a name="jetsetcurrentindex4-function"></a>Função JetSetCurrentIndex4


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetcurrentindex4-function"></a>Função JetSetCurrentIndex4

A função **JetSetCurrentIndex4** é usada para definir o índice atual de um cursor. O índice atual de um cursor define quais registros em uma tabela são visíveis para esse cursor e a ordem na qual aparecem, selecionando o conjunto de entradas de índice a ser usado para expor esses registros.

```cpp
    JET_ERR JET_API JetSetCurrentIndex4(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      JET_PCSTR szIndexName,
      __in_opt      JET_INDEXID* pindexid,
      __in          JET_GRBIT grbit,
      __in          unsigned long itagSequence
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*szIndexName*

O nome do índice a ser selecionado para o cursor. Se esse parâmetro for nulo ou uma cadeia de caracteres vazia, o índice clusterizado será selecionado. Se um índice primário for definido para a tabela, esse índice será selecionado porque é o mesmo que o índice clusterizado. Se nenhum índice primário for definido para a tabela, o índice sequencial será selecionado. O índice sequencial não tem nenhuma definição de índice. Consulte [JetCreateIndex](./jetcreateindex-function.md) para obter mais informações.

Se *pIndexID* não for NULL, o nome do índice será ignorado e o índice será selecionado por sua ID de índice.

*pindexid*

A ID do índice a ser selecionado para o cursor.

A ID do índice é um identificador volátil e opaco que pode ser usado para selecionar rapidamente um índice. Essa ID pode ser recuperada usando JetGetIndexInfo ou JetGetTableIndexInfo usando a opção JET_IdxInfoIndexId.

Se *pIndexID* for NULL, o índice será selecionado pelo nome do índice e a ID do índice será ignorada.

Quando esse parâmetro não estiver presente, seu valor será presumido como nulo.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais das ações a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitMoveFirst</p> | <p>Essa opção indica que o cursor deve ser posicionado na primeira entrada do índice especificado. Se o índice clusterizado estiver sendo selecionado (índice primário ou índice sequencial) e o índice atual for um índice secundário, JET_bitMoveFirst será assumido. Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita.</p> | 
| <p>JET_bitNoMove</p> | <p>Essa opção indica que o cursor deve ser posicionado na entrada de índice do novo índice que corresponde ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</p><p>Se a definição do novo índice contiver pelo menos uma coluna de chave com valores múltiplos, a entrada do índice de destino será ambígua. Nesse caso, o <em>itagSequence</em> especificado é usado para selecionar qual múltiplo valor da coluna de chave com valores múltiplos mais significativos é usado para posicionar o cursor. Só é necessário passar um único <em>itagSequence</em> mesmo no caso de várias colunas de chave com valores múltiplos, pois o mecanismo expande apenas todos os valores para a coluna de chave com valores múltiplos mais significativos. Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obter mais detalhes.</p><p>Se JET_bitMoveFirst for especificado, essa opção será ignorada.</p><p>Se o índice atual estiver sendo selecionado, essa opção será ignorada e nenhuma alteração na posição do cursor será feita. Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitMoveFirst.</p> | 



*itagSequence*

Número de sequência do valor de coluna com valores múltiplos que será usado para posicionar o cursor no novo índice.

Esse parâmetro só é usado em conjunto com JET_bitNoMove. Consulte a descrição dessa opção para obter mais detalhes.

Quando esse parâmetro não estiver presente ou estiver definido como zero, seu valor será presumido como 1.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhum valor para a primeira coluna de chave com valores múltiplos na definição do novo índice que corresponde ao número de sequência especificado.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidIndexId</p> | <p>O conteúdo da ID de índice não era válido ou expirou e precisa ser atualizado. Isso pode ocorrer para <strong>JetSetCurrentIndex4</strong> quando:</p><ul><li><p>pindexid- &gt; cbStruct não tem o tamanho esperado (Windows Server 2003 e versões posteriores).</p></li><li><p>O mecanismo foi desligado porque a ID do índice foi buscada.</p></li><li><p>Todos os cursores que fazem referência à tabela que contém o índice correspondente à ID do índice foram fechados e o mecanismo removeu a definição do índice do cache de esquema.</p></li><li><p>A ID de índice está sendo usada com um cursor aberto na tabela incorreta.</p></li><li><p>O índice foi descartado ou ainda não está visível para a sessão.</p></li></ul> | 
| <p>JET_errInvalidName</p> | <p>Um dos nomes de objeto especificados era inválido. Todos os nomes de objeto devem estar em conformidade com o mesmo conjunto de regras. Essas regras são as seguintes:</p><ul><li><p>Os nomes de objeto devem ser compostos por caracteres ASCII.</p></li><li><p>Os nomes de objeto devem ter pelo menos um caractere de comprimento.</p></li><li><p>Os nomes de objeto não podem exceder JET_cbNameMost (64) caracteres de comprimento.</p></li><li><p>Os nomes de objeto não podem começar com um espaço.</p></li><li><p>Os nomes de objeto não podem conter caracteres de controle ASCII (0x00 a 0x1F).</p></li><li><p>Os nomes de objeto não podem conter um ponto de exclamação (!), período (.), colchete à esquerda ([) ou caractere de colchete direito (]).</p></li><li><p>Depois de validado, somente a parte da cadeia de caracteres até o primeiro espaço (se houver) será usada para o nome do objeto. Isso efetivamente significa que os nomes de objeto também não podem conter um espaço.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. isso pode ocorrer para <strong>JetSetCurrentIndex4</strong> quando <em>pindexid</em> não é nulo e pindexid- &gt; cbStruct não tem o tamanho esperado (Windows XP e versões anteriores).</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Um índice secundário está sendo selecionado com a opção JET_bitNoMove e não há nenhuma entrada de índice no novo índice que corresponda ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errOutOfCursors</p> | <p>O mecanismo esgotou seu pool de recursos usados para abrir cursores. O número máximo de cursores que podem ser abertos a qualquer momento é controlado usando <a href="gg269201(v=exchg.10).md">JET_paramMaxCursors</a>. Consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> para obter mais informações. Isso pode ocorrer para <strong>JetSetCurrentIndex4</strong> quando um índice secundário tiver sido selecionado e o mecanismo não puder abrir um cursor interno para usar esse índice.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p>esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, o índice atual do cursor é definido como o índice solicitado. As entradas de índice agora podem ser buscadas usando [JetSeek](./jetseek-function.md) de acordo com a definição de índice do índice solicitado. As entradas de índice também podem ser enumeradas usando [JetMove](./jetmove-function.md) na ordem especificada por essa definição de índice. A posição atual do cursor é definida como a primeira entrada de índice no índice (JET_bitMoveFirst) ou em uma entrada de índice específica que está relacionada à posição atual do cursor no índice antigo (JET_bitNoMove). Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o índice atual e a posição atual do cursor estão em um estado indefinido. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

Se a dica de ID de índice estiver obsoleta, a API simplesmente falhará. Não há nenhum fallback para o nome de texto do índice nesse caso, como pode esperar. Esse fallback deve ser feito manualmente pelo chamador da API.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetSetCurrentIndex4W</strong> (Unicode) e <strong>JetSetCurrentIndex4A</strong> (ANSI).</p> | 



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
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
