---
description: 'Saiba mais sobre: Função JetRetrieveKey'
title: Função JetRetrieveKey
TOCTitle: JetRetrieveKey Function
ms:assetid: a96d0a7c-f1db-48bc-807d-4e6357aec726
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294051(v=EXCHG.10)
ms:contentKeyID: 32765650
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveKey
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 938cc8161326afaa9d0d5b3bf905bf976e850b40
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985589"
---
# <a name="jetretrievekey-function"></a>Função JetRetrieveKey


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetretrievekey-function"></a>Função JetRetrieveKey

A **função JetRetrieveKey** recupera a chave para a entrada de índice na posição atual de um cursor. Essas chaves são construídas por chamadas para [JetMakeKey.](./jetmakekey-function.md) A chave recuperada pode ser usada para retornar com eficiência esse cursor para a mesma entrada de índice por uma chamada para [JetSeek](./jetseek-function.md).

```cpp
    JET_ERR JET_API JetRetrieveKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out_opt     void* pvData,
      __in          unsigned long cbMax,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para essa chamada.

*Tableid*

O cursor a ser usado para essa chamada.

*Pvdata*

O buffer de saída que receberá a chave.

*cbMax*

O tamanho máximo em bytes do buffer de saída.

*pcbActual*

Recebe o tamanho real em bytes da chave.

Se esse parâmetro for NULL, o tamanho real da chave não será retornado.

Se o buffer de saída for muito pequeno, o tamanho real da chave ainda será retornado. Isso significa que esse número será maior que o tamanho do buffer de saída.

*grbit*

Um grupo de bits que contém as opções a serem usadas para essa chamada, que incluem zero ou mais dos seguintes.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Quando especificado, o mecanismo retornará a chave de pesquisa para o cursor. A chave de pesquisa é criada usando uma ou mais chamadas anteriores para <a href="gg269329(v=exchg.10).md">JetMakeKey</a> com a finalidade de buscar essa chave usando <a href="gg294103(v=exchg.10).md">JetSeek</a> ou definir um intervalo de índice usando <a href="gg294112(v=exchg.10).md">JetSetIndexRange</a>.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Não há nenhuma chave de pesquisa atual para o cursor. Isso ocorrerá para <strong>JetRetrieveKey</strong> se JET_bitRetrieveCopy for especificado e uma chave de pesquisa não tiver sido construída para esse cursor usando uma chamada anterior para <a href="gg269329(v=exchg.10).md">JetMakeKey</a>. A chave de pesquisa será excluída por uma chamada anterior a qualquer API de navegação no cursor diferente de <a href="gg294117(v=exchg.10).md">JetMove.</a></p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber toda a chave. O buffer de saída foi preenchido com a mesma parte da chave que caberia. O tamanho real da chave também foi retornado, se solicitado.</p><p><strong>Observação</strong>   Esse erro não será retornado se JET_bitRetrieveCopy for especificado. Consulte a seção Comentários para obter mais informações.</p> | 



Em caso de êxito, a chave para a entrada de índice na posição atual de um cursor será retornada no buffer de saída. Se JET_wrnBufferTruncated for retornado, o buffer de saída conterá a mesma parte da chave que caberá no espaço fornecido e o tamanho real da chave será preciso. Nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, o estado do buffer de saída e o tamanho real da chave serão indefinido. Nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

As chaves geralmente devem ser tratadas como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, as propriedades a seguir podem ser conhecidas sobre todas as chaves ESENT:

  - As chaves podem ser comparadas entre si usando a [função memcmp](https://msdn.microsoft.com/library/aa246467\(vs.60\).aspx) para estabelecer sua ordenação relativa no índice de origem na tabela das entradas de índice de origem.

  - Não faz sentido comparar chaves de entradas de índice de índices diferentes entre si.

  - Uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes Windows Vista. No Windows Vista e versões posteriores, as chaves podem ser maiores. O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.

Além das propriedades acima das chaves ESENT em geral, é importante observar que uma chave de pesquisa é diferente da chave para uma entrada de índice. Especificamente, uma chave de pesquisa pode ser maior que uma chave comum. Esse comprimento extra ocorre quando uma opção curinga é usada durante a construção da chave de pesquisa. Consulte [JetMakeKey](./jetmakekey-function.md) para obter mais informações.

Há um bug importante nessa API que está presente em todas as versões. Se a chave de pesquisa for solicitada usando o uso de JET_bitRetrieveCopy e o buffer de saída for muito pequeno para receber a chave inteira, JET_wrnBufferTruncated NÃO será retornado. JET_errSuccess será retornado. É importante verificar se o tamanho real da chave, conforme retornado usando *pcbActual,* é menor ou igual ao tamanho do buffer de saída. Se o tamanho real for maior que o tamanho do buffer de saída, o chamador **de JetRetrieveKey** deverá reagir como se JET_wrnBufferTruncated fosse retornado.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetMakeKey](./jetmakekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
