---
description: 'Saiba mais sobre: função JetMakeKey'
title: Função JetMakeKey
TOCTitle: JetMakeKey Function
ms:assetid: 8c1cff2f-2f24-4990-a9d8-fb4f822e50b1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269329(v=EXCHG.10)
ms:contentKeyID: 32765619
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetMakeKey
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b0a7300a312bf5f34c2a60cc6ed3b3c95879dde
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983399"
---
# <a name="jetmakekey-function"></a>Função JetMakeKey


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetmakekey-function"></a>Função JetMakeKey

A função **JetMakeKey** constrói chaves de pesquisa que podem ser usadas para localizar um conjunto de entradas em um índice por alguns critérios de pesquisa simples em seus valores de coluna de chave. Uma chave de pesquisa também é uma das propriedades intrínsecas de um cursor e é usada pelas operações [JetSeek](./jetseek-function.md) e [JetSetIndexRange](./jetsetindexrange-function.md) para localizar entradas de índice correspondentes a esses critérios de pesquisa no índice atual desse cursor. Uma chave de pesquisa completa é criada em uma série de chamadas **JetMakeKey** em que cada chamada é usada para carregar o valor da coluna para a próxima coluna de chave do índice atual de um cursor. Também é possível carregar uma chave de pesquisa construída anteriormente que foi recuperada do cursor usando [JetRetrieveKey](./jetretrievekey-function.md).

```cpp
    JET_ERR JET_API JetMakeKey(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in_opt      const void* pvData,
      __in          unsigned long cbData,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*pvData*

O buffer de entrada que contém os dados da coluna para a coluna de chave atual do índice atual do cursor para o qual a chave de pesquisa está sendo construída.

O tipo de dados dos dados da coluna no buffer de entrada deve corresponder exatamente ao tipo de dados e a outras propriedades da definição de coluna da coluna de chave atual. Nenhuma coerção de tipo é executada nos dados da coluna.

Se JET_bitNormalizedKey for especificado no parâmetro *grbit* , o buffer de entrada deverá conter uma chave de pesquisa construída anteriormente. Essas chaves são obtidas usando uma chamada para [JetRetrieveKey](./jetretrievekey-function.md).

*cbData*

O tamanho em bytes dos dados da coluna fornecidos no buffer de entrada.

Se JET_bitNormalizedKey for especificado no parâmetro *grbit* , esse será o tamanho da chave de pesquisa fornecida no buffer de entrada.

Se o tamanho dos dados da coluna for zero, o conteúdo do buffer de entrada será ignorado. Se JET_bitKeyDataZeroLength for especificado no parâmetro *grbit* e a coluna de chave atual do índice atual do cursor for uma coluna de comprimento variável, os dados da coluna de entrada serão presumidos como um valor de comprimento zero. Caso contrário, os dados da coluna de entrada presumem ser um valor nulo.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitFullColumnEndLimit</p> | <p>A chave de pesquisa deve ser construída de forma que as colunas de chave que vierem após a coluna de chave atual sejam consideradas curingas. Isso significa que a chave de pesquisa construída pode ser usada para corresponder as entradas de índice que têm o seguinte:</p><ul><li><p>Os valores de coluna exatos fornecidos para essa coluna de chave e todas as colunas de chave anteriores.</p></li><li><p>Quaisquer valores de coluna necessários para colunas de chave subsequentes.</p></li></ul><p>Essa opção deve ser usada ao criar chaves de pesquisa curinga a serem usadas para localizar entradas de índice mais próximas ao final de um índice. O final do índice é a entrada de índice que é encontrada ao mover para o último registro nesse índice. O final do índice não é o mesmo que o alto fim do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</p><p>essa opção só está disponível no Windows XP e versões posteriores.</p> | 
| <p>JETbitFullColumnStartLimit</p> | <p>A chave de pesquisa deve ser construída de modo que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas. Isso significa que a chave de pesquisa construída pode ser usada para corresponder as entradas de índice que têm o seguinte:</p><ul><li><p>Os valores de coluna exatos fornecidos para essa coluna de chave e todas as colunas de chave anteriores.</p></li><li><p>Quaisquer valores de coluna necessários para colunas de chave subsequentes.</p></li></ul><p>Essa opção deve ser usada ao criar chaves de pesquisa curinga a serem usadas para localizar entradas de índice mais próximas ao início de um índice. O início do índice é a entrada de índice que é encontrada ao mover para o primeiro registro nesse índice. O início do índice não é o mesmo que o low end do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</p><p>essa opção só está disponível no Windows XP e versões posteriores.</p> | 
| <p>JET_bitKeyDataZeroLength</p> | <p>Se o tamanho do buffer de entrada for zero e a coluna de chave atual for uma coluna de comprimento variável, essa opção indicará que o buffer de entrada contém um valor de comprimento zero. Caso contrário, um tamanho de buffer de entrada igual a zero indicaria um valor nulo.</p> | 
| <p>JET_bitNewKey</p> | <p>Uma nova chave de pesquisa deve ser construída. Qualquer chave de pesquisa existente anteriormente é descartada.</p> | 
| <p>JET_bitNormalizedKey</p> | <p>Quando essa opção é especificada, todas as outras opções são ignoradas, qualquer chave de pesquisa existente anteriormente é descartada e o conteúdo do buffer de entrada é carregado como a nova chave de pesquisa.</p> | 
| <p>JET_bitPartialColumnEndLimit</p> | <p>A chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas. Isso significa que a chave de pesquisa construída pode ser usada para corresponder as entradas de índice que têm o seguinte:</p><ul><li><p>Os valores de coluna exatos fornecidos para essa coluna de chave e todas as colunas de chave anteriores.</p></li><li><p>Quaisquer valores de coluna necessários para colunas de chave subsequentes.</p></li></ul><p>Essa opção deve ser usada ao criar chaves de pesquisa curinga a serem usadas para localizar entradas de índice mais próximas ao final de um índice. O final do índice é a entrada de índice que é encontrada ao mover para o último registro nesse índice. O final do índice não é o mesmo que o alto fim do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</p><p>Esta opção não pode ser usada quando a coluna de chave atual não é uma coluna de texto ou uma coluna binária variável. A operação falhará com JET_errInvalidgrbit se for tentada.</p><p>essa opção só está disponível no Windows XP e versões posteriores.</p> | 
| <p>JET_bitPartialColumnStartLimit</p> | <p>Essa opção indica que a chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas. Isso significa que a chave de pesquisa construída pode ser usada para corresponder as entradas de índice que têm o seguinte:</p><ul><li><p>Os valores de coluna exatos fornecidos para essa coluna de chave e todas as colunas de chave anteriores.</p></li><li><p>Quaisquer valores de coluna necessários para colunas de chave subsequentes.</p></li></ul><p>Essa opção deve ser usada ao criar chaves de pesquisa curinga a serem usadas para localizar entradas de índice mais próximas ao início de um índice. O início do índice é a entrada de índice que é encontrada ao mover para o primeiro registro nesse índice. O início do índice não é o mesmo que o low end do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</p><p>Esta opção não pode ser usada quando a coluna de chave atual não é uma coluna de texto ou uma coluna binária variável. A operação falhará com JET_errInvalidgrbit se for tentada.</p><p>essa opção só está disponível no Windows XP e versões posteriores.</p> | 
| <p>JET_bitStrLimit</p> | <p>Essa opção indica que a chave de pesquisa deve ser construída de modo que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas. Isso significa que a chave de pesquisa construída pode ser usada para corresponder as entradas de índice que têm o seguinte:</p><ul><li><p>Os valores de coluna exatos fornecidos para essa coluna de chave e todas as colunas de chave anteriores.</p></li><li><p>Quaisquer valores de coluna necessários para colunas de chave subsequentes.</p></li></ul><p>Essa opção deve ser usada ao criar chaves de pesquisa curinga a serem usadas para localizar entradas de índice mais próximas ao final de um índice. O final do índice é a entrada de índice que é encontrada ao mover para o último registro nesse índice. O final do índice não é o mesmo que o alto fim do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</p><p>Quando essa opção é especificada em combinação com JET_bitSubStrLimit e a coluna de chave atual é uma coluna de texto, essa opção será ignorada. Esse comportamento destina-se a permitir que o tipo da coluna de chave atual seja inferido ao criar a chave de pesquisa.</p><p>Se você quiser criar uma chave de pesquisa semelhante para o início de um índice, uma chamada semelhante a <strong>JetMakeKey</strong> deve ser feita para a última coluna de chave que não seja um curinga, mas sem opções de curinga especificadas. A chave de pesquisa é, em seguida, um estado apropriado para ser usado para essa pesquisa. Isso é análogo ao uso de JET_bitFullColumnStartLimit, exceto que a chave de pesquisa não é concluída de forma limpa, pois é após o uso de uma opção curinga.</p><p>essa opção foi preterida para Windows XP e versões posteriores para resolver essa semântica estranha. JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit devem ser usados em vez disso, sempre que possível.</p> | 
| <p>JET_bitSubStrLimit</p> | <p>Essa opção indica que a chave de pesquisa deve ser construída de modo que a coluna de chave atual seja considerada um curinga de prefixo e que as colunas de chave que vierem após a coluna de chave atual devam ser consideradas curingas. Isso significa que a chave de pesquisa construída pode ser usada para corresponder as entradas de índice que têm o seguinte:</p><ul><li><p>Os valores de coluna exatos fornecidos para todas as colunas de chave anteriores.</p></li><li><p>Os dados de coluna especificados como um prefixo de seu valor de coluna para a coluna de chave atual.</p></li><li><p>Quaisquer valores de coluna para colunas de chave subsequentes.</p></li></ul><p>Essa opção deve ser usada ao criar chaves de pesquisa curinga a serem usadas para localizar entradas de índice mais próximas ao final de um índice. O final do índice é a entrada de índice que é encontrada ao mover para o último registro nesse índice. O final do índice não é o mesmo que o alto fim do índice, que pode ser alterado dependendo da ordem de classificação das colunas de chave no índice.</p><p>Quando essa opção é especificada em combinação com JET_bitStrLimit e a coluna de chave atual é uma coluna de texto, essa opção terá precedência. Essa opção é ignorada quando a coluna de chave atual não é uma coluna de texto. Esse comportamento destina-se a permitir que o tipo da coluna de chave atual seja inferido ao criar a chave de pesquisa.</p><p>Se você quiser criar uma chave de pesquisa semelhante para o início de um índice, uma chamada semelhante a <strong>JetMakeKey</strong> deverá ser feita para a coluna de chave que deve ser o curinga de prefixo, mas com essa opção sem opções de curinga especificada. A chave de pesquisa é, em seguida, um estado apropriado para ser usado para essa pesquisa. Isso é análogo ao uso de JET_bitPartialColumnStartLimit, exceto que a chave de pesquisa não é concluída de forma limpa, pois é após o uso de uma opção curinga.</p><p>essa opção foi preterida para Windows XP e versões posteriores para resolver essa semântica estranha. JET_bitPartialColumnStartLimit e JET_bitPartialColumnEndLimit devem ser usados em vez disso, quando possível.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexTuplesKeyTooSmall</p> | <p>Os dados de coluna fornecidos eram muito pequenos para criar uma chave válida para o índice atual porque esse índice é um índice de tupla e o tamanho mínimo da tupla era maior do que os dados de coluna fornecidos. Consulte <a href="gg294099(v=exchg.10).md">JetCreateIndex</a> para obter mais informações sobre índices de tupla. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Os dados de coluna fornecidos não correspondem ao tamanho exigido pela definição de coluna. Isso pode acontecer se o tipo de dados da coluna for intrinsecamente determinado tamanho. Isso também pode acontecer se o tipo de dados da coluna não for intrinsecamente um determinado tamanho, mas a definição da coluna declará-la para ter comprimento fixo. Uma exceção a isso é que esse erro não ocorrerá quando poucos dados forem fornecidos para uma coluna de texto de comprimento fixo porque os dados ausentes serão preenchidos automaticamente com espaços. Uma segunda exceção a isso é que esse erro não ocorrerá quando poucos dados forem fornecidos para uma coluna binária de comprimento fixo, pois quaisquer dados ausentes serão preenchidos automaticamente com zeros.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Uma das opções solicitadas era inválida, usada de maneira ilegal ou não implementada. Isso pode ocorrer para <strong>JetMakeKey</strong> quando:</p><ul><li><p>JET_bitPartialColumnStartLimit ou JET_bitPartialColumnEndLimit são especificados e a coluna de chave correspondente não é uma coluna de texto e não é uma coluna binária de comprimento variável. esse caso ocorre apenas no Windows XP e versões posteriores.</p></li><li><p>É feita uma tentativa de usar mais de uma das seguintes opções juntas: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit. esse caso ocorre apenas no Windows XP e versões posteriores.</p></li><li><p>É feita uma tentativa de usar JET_bitStrLimit ou JET_bitSubStrLimit quando uma das seguintes opções é usada: JET_bitPartialColumnStartLimit, JET_bitPartialColumnEndLimit, JET_bitFullColumnStartLimit e JET_bitFullColumnEndLimit. esse caso ocorre apenas no Windows XP e versões posteriores.</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</p><p>Isso pode ocorrer para <strong>JetMakeKey</strong> quando JET_bitNormalizedKey foi especificado e o valor fornecido no buffer de entrada era muito grande para ser uma chave de pesquisa válida.</p> | 
| <p>JET_errKeyIsMade</p> | <p>Os dados da coluna fornecidos para <strong>JetMakeKey</strong> foram rejeitados porque os dados da coluna já foram fornecidos para todas as colunas de chave no índice atual. Isso pode acontecer de três maneiras. A primeira maneira é se os dados da coluna forem fornecidos para cada coluna de chave no índice atual. A segunda maneira é se os dados da coluna tiverem sido fornecidos para pelo menos uma coluna de chave e uma opção de curinga foi escolhida para a última chamada. A terceira maneira é se uma chave de pesquisa construída anteriormente foi fornecida usando JET_bitNormalizedKey, que abrange todas as colunas de chave.</p> | 
| <p>JET_errKeyNotMade</p> | <p>Não há uma chave de pesquisa atual para o cursor. Isso ocorrerá para <strong>JetMakeKey</strong> se JET_bitNewKey não for especificado e uma chave de pesquisa não tiver sido construída para este cursor usando uma chamada anterior para <strong>JetMakeKey</strong>. A chave de pesquisa será excluída por uma chamada anterior para qualquer API de navegação no cursor que não seja <a href="gg294117(v=exchg.10).md">JetMove</a>.</p> | 
| <p>JET_errNoCurrentIndex</p> | <p>Não há índice atual para o cursor. Isso ocorrerá para <strong>JetMakeKey</strong> se o cursor estiver no índice clusterizado de uma tabela, um índice primário não tiver sido definido e JET_bitNormalizedKey não tiver sido especificado. Não é possível construir uma chave de pesquisa se o cursor estiver em um índice que não tem nenhuma coluna de chave, a menos que uma chave de pesquisa construída anteriormente seja fornecida.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 



Em caso de sucesso, se JET_bitNormalizedKey e JET_bitNewKey não forem especificados, a chave de pesquisa terá sido criada pelos critérios de pesquisa para mais uma coluna de chave no índice atual. Se JET_bitNormalizedKey não tiver sido especificado e JET_bitNewKey tiver sido especificado, qualquer chave de pesquisa existente anteriormente será descartada e um novo terá sido criado pelos critérios de pesquisa para a primeira coluna de chave no índice atual. Se JET_bitNormalizedKey foi especificado, qualquer chave de pesquisa existente anteriormente foi descartada e uma nova foi carregada a partir do buffer de entrada. De qualquer forma, nenhuma alteração no estado do banco de dados ocorrerá.

Em caso de falha, se JET_bitNormalizedKey ou JET_bitNewKey tiver sido especificado, o estado da chave de pesquisa será indefinido. Se nem JET_bitNormalizedKey nem JET_bitNewKey foram especificadas, nenhuma alteração no estado da chave de pesquisa ocorrerá. De qualquer forma, nenhuma alteração no estado do banco de dados ocorrerá.

#### <a name="remarks"></a>Comentários

As chaves devem ser tratadas como partes opacas de dados. Nenhuma tentativa deve ser feita para explorar a estrutura interna desses dados. No entanto, o seguinte é conhecido sobre todas as chaves de ESENT:

  - As chaves podem ser comparadas entre si usando [memcmp](/previous-versions/visualstudio/visual-studio-6.0/aa246467(v=vs.60)) para estabelecer sua ordenação relativa no índice de origem sobre a tabela das entradas de índice de origem.

  - Não há sentido para comparar chaves de entradas de índice de índices diferentes entre si.

  - uma chave é sempre menor ou igual a JET_cbKeyMost (255) bytes de comprimento antes de Windows Vista. no Windows Vista e versões posteriores, as chaves podem ser maiores. O tamanho máximo de uma chave é igual ao valor atual de JET_paramKeyMost.

As chaves de pesquisa podem ser um byte mais longas se uma opção curinga tiver sido usada. nesse caso, a chave de pesquisa será de até JET_cbLimitKeyMost (256) bytes de versões anteriores ao Windows vista e JET_paramKeyMost + 1 bytes para Windows Vista e versões posteriores.

Há uma ramificação muito importante para esse tamanho máximo de chave. Sempre que houver uma entrada de índice com valores de coluna grandes o suficiente para fazer com que uma chave seja gerada para esse índice que, de outra forma, seria maior do que esse tamanho máximo, essa chave será silenciosamente truncada no tamanho máximo. Isso causa dois efeitos:

  - Para entradas em um índice exclusivo, isso causará entradas que, de outra forma, seriam exclusivas para serem declaradas como duplicatas.

  - Para entradas em todos os índices, o truncamento de chave causará entradas de índice que, caso contrário, não corresponderia aos critérios de pesquisa de uma determinada chave de pesquisa a ser declarada como correspondências.

Os aplicativos devem prever esse truncamento e evitá-lo ou compensar seus efeitos. no Windows Vista, um novo sinalizador de índice, JET_bitIndexDisallowTruncation, foi adicionado para tornar mais fácil para os aplicativos evitarem truncamentos de chave. Consulte a estrutura [JET_INDEXCREATE](./jet-indexcreate-structure.md) para obter mais informações sobre essa opção de indexação.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetCreateIndex](./jetcreateindex-function.md)  
[JetRetrieveKey](./jetretrievekey-function.md)  
[JetSeek](./jetseek-function.md)  
[JetSetIndexRange](./jetsetindexrange-function.md)
