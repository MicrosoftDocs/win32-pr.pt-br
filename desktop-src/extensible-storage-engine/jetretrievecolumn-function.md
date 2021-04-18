---
description: 'Saiba mais sobre: função JetRetrieveColumn'
title: Função JetRetrieveColumn
TOCTitle: JetRetrieveColumn Function
ms:assetid: 1e55063f-6033-4416-a9a6-894032fed069
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269198(v=EXCHG.10)
ms:contentKeyID: 32765501
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRetrieveColumn
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 074fb2471733afac40f76dcae1a4ce3ff38edc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763325"
---
# <a name="jetretrievecolumn-function"></a>Função JetRetrieveColumn


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetretrievecolumn-function"></a>Função JetRetrieveColumn

A função **JetRetrieveColumn** recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual. Além de recuperar o valor real da coluna, **JetRetrieveColumn** também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.

```cpp
    JET_ERR JET_API JetRetrieveColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __out_opt     void* pvData,
      __in          unsigned long cbData,
      __out_opt     unsigned long* pcbActual,
      __in          JET_GRBIT grbit,
      __in_out_opt  JET_RETINFO* pretinfo
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

*TableID*

O cursor a ser usado para esta chamada.

*columnid*

A [JET_COLUMNID](./jet-columnid.md) da coluna a ser recuperada.

Um valor de *columnid* de 0 (zero) pode ser fornecido, o que não se refere a nenhuma coluna individual. Quando *columnid* 0 (zero) é fornecido, todas as colunas marcadas, esparsas e colunas com valores múltiplos são tratadas como uma única coluna. Isso facilita a recuperação de todas as colunas esparsas que estão presentes em um registro.

*pvData*

O buffer de saída que recebe o valor da coluna.

*cbData*

O tamanho máximo, em bytes, do buffer de saída.

*pcbActual*

Recebe o tamanho real, em bytes, do valor da coluna.

Se esse parâmetro for **NULL**, o tamanho real do valor da coluna não será retornado.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitRetrieveCopy</p></td>
<td><p>Esse sinalizador faz com que a coluna de recuperação recupere o valor modificado em vez do valor original. Se o valor não tiver sido modificado, o valor original será recuperado. Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado durante a operação de inserção ou atualização de um registro.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveFromIndex</p></td>
<td><p>Essa opção é usada para recuperar valores de coluna do índice, se possível, sem acessar o registro. Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice. Nos casos em que o valor da coluna original não puder ser recuperado do índice, devido a transformações irreversíveis ou truncamento de dados, o registro será acessado e os dados serão recuperados como normais. Essa é uma opção de desempenho e só deve ser especificada quando for provável que o valor da coluna possa ser recuperado do índice. Essa opção não deverá ser especificada se o índice atual for o índice clusterizado, já que as entradas de índice para o índice clusterizado ou primário são os próprios registros. Esse bit não poderá ser definido se JET_bitRetrieveFromPrimaryBookmark também for definido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveFromPrimaryBookmark</p></td>
<td><p>Essa opção é usada para recuperar valores de coluna do indicador de índice e pode ser diferente do valor de índice quando uma coluna aparece no índice primário e no índice atual. Essa opção não deverá ser especificada se o índice atual for o índice clusterizado ou primário. Esse bit não poderá ser definido se JET_bitRetrieveFromIndex também for definido.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveTag</p></td>
<td><p>Essa opção é usada para recuperar o número de sequência de um valor de coluna com valores múltiplos em pretinfo- &gt; itagSequence. Normalmente, o campo itagSequence é uma entrada para recuperar valores de coluna de vários valores de um registro. No entanto, ao recuperar valores de um índice, também é possível associar a entrada de índice a um número de sequência específico e recuperar esse número de sequência também. A recuperação do número de sequência pode ser uma operação dispendiosa e só deve ser feita se necessário.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveNull</p></td>
<td><p>Essa opção é usada para recuperar valores <strong>nulos</strong> de coluna de vários valores. Se essa opção não for especificada, os valores <strong>nulos</strong> da coluna com valores múltiplos serão automaticamente ignorados.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveIgnoreDefault</p></td>
<td><p>Essa opção afeta apenas as colunas com valores múltiplos e faz com que um valor <strong>nulo</strong> seja retornado quando o número de sequência solicitado é 1 e não há valores definidos para a coluna no registro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveLongId</p></td>
<td><p>Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRetrieveLongValueRefCount</p></td>
<td><p>Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRetrieveTuple</p></td>
<td><p>Esse sinalizador permitirá a recuperação de um segmento de tupla do índice. Esse bit deve ser especificado com JET_bitRetrieveFromIndex.</p></td>
</tr>
</tbody>
</table>


*pretinfo*

Se *pretinfo* for atribuído como **NULL** , a função se comporta como se um *ItagSequence* de 1 e um *ibLongValue* de 0 (zero) fossem fornecidos. Isso faz com que a recuperação de coluna recupere o primeiro valor de uma coluna com vários valores e recupere dados longos no deslocamento 0 (zero).

Esse parâmetro é usado para fornecer um ou mais dos seguintes itens:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ibLongValue</p></td>
<td><p>Fornece um deslocamento binário em um valor de coluna longo ao recuperar uma parte de um valor de coluna.</p></td>
</tr>
<tr class="even">
<td><p>itagSequence</p></td>
<td><p>Fornece o número de sequência do valor de coluna com valores múltiplos desejado. Observe que esse campo só será definido se o JET_bitRetrieveTag for especificado. Caso contrário, ele não será modificado.</p></td>
</tr>
<tr class="odd">
<td><p>columnidNextTagged</p></td>
<td><p>Retorna a ID de coluna do valor de coluna retornado ao recuperar todas as colunas marcadas, esparsas e com valores múltiplos usando a passagem de <em>columnid</em> de 0 (zero).</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBadColumnId</p></td>
<td><p>A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errBadItagSequence</p></td>
<td><p>Um valor de número de sequência de coluna com valores múltiplos inválido foi passado em pretinfo- &gt; itagSequence. Os valores válidos para os números de sequência de valor de coluna com valores múltiplos são 1 ou mais. Um valor de 0 (zero) é inválido para esta função.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesCannotRetrieveFromIndex</p></td>
<td><p>As colunas indexadas como subcadeias de caracteres não podem ser recuperadas do índice, já que apenas uma pequena parte da coluna está normalmente presente em cada entrada de índice.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Em alguns casos, o buffer fornecido para a coluna de recuperação deve ser suficientemente dimensionado para retornar qualquer valor do valor da coluna. Por exemplo, colunas atualizáveis de caução são ajustadas para serem consistentes para o contexto transacional da sessão de chamada e esse ajuste requer o buffer fornecido pelo chamador. Se espaço de buffer insuficiente for fornecido, JET_errInvalidBufferSize será retornado e nenhum dado de coluna será retornado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um ou mais dos parâmetros fornecidos estão incorretos. Isso pode acontecer se o retinfo. cbStruct for menor que o tamanho de <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bit conhecido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>O valor da coluna inteira não pôde ser recuperado porque o buffer fornecido é menor do que o tamanho da coluna.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnColumnNull</p></td>
<td><p>O valor da coluna recuperado é <strong>nulo</strong>.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o valor da coluna para a coluna especificada é copiado para o buffer especificado. Menor que todo o valor da coluna é copiado com o aviso JET_wrnBufferTruncated é retornado. Se o *pcbActual* foi fornecido, o tamanho real do valor da coluna será retornado. Observe que os valores **nulos** têm comprimento 0 (zero) e, portanto, definirão o tamanho retornado como 0 (zero). Se a coluna recuperada tiver sido uma coluna com vários valores e *pretinfo* tiver sido definida, e JET_bitReturnTag for definido como uma opção, o número de sequência do valor da coluna será retornado em pretinfo- \> itagSequence.

Em caso de falha, o local do cursor permanece inalterado e nenhum dado é copiado no buffer fornecido.

#### <a name="remarks"></a>Comentários

Essa chamada é usada apenas uma vez para recuperar dados de tamanho fixo ou conhecido para colunas sem vários valores. No entanto, quando os dados da coluna são de tamanho desconhecido, essa chamada normalmente é usada duas vezes. Ele é chamado primeiro para determinar o tamanho dos dados para que ele possa alocar o espaço de armazenamento necessário. Em seguida, a mesma chamada é feita novamente para recuperar os dados da coluna. Quando o número real de valores é desconhecido, como uma coluna tem vários valores, a chamada normalmente é usada três vezes. Primeiro, para obter o número de valores e duas vezes mais para alocar o armazenamento e recuperar os dados reais.

A recuperação de todos os valores de uma coluna com vários valores pode ser feita chamando repetidamente essa função com um valor de pretinfo- \> itagSequence começando em 1 e aumentando em cada chamada subsequente. O último valor de coluna é conhecido por ser recuperado quando um JET_wrnColumnNull é retornado da função. Observe que esse método não poderá ser feito se a coluna de vários valores tiver valores **nulos** explícitos definidos em sua sequência de valores, pois esses valores seriam ignorados. Se um aplicativo desejar recuperar todos os valores de coluna com vários valores, incluindo aqueles explicitamente definidos como **NULL**, [JetRetrieveColumns](./jetretrievecolumns-function.md) deverá ser usado em vez de **JetRetrieveColumn**. Observe que essa função não retorna o número de valores para uma função com valores múltiplos quando um valor de *itagSequence* de 0 (zero) é fornecido. Somente [JetRetrieveColumns](./jetretrievecolumns-function.md) retornará o número de valores de um valor de coluna quando um valor de *itagSequence* de 0 (zero) for passado.

Se essa função for chamada no nível de transação 0 (zero), por exemplo, a sessão de chamada não está em uma transação, então uma transação é aberta e fechada dentro da função. A finalidade disso é retornar resultados consistentes no caso de um valor longo abranger páginas de banco de dados. Observe que a transação é liberada entre chamadas de função e uma série de chamadas para essa função quando a sessão não está em uma transação pode retornar dados atualizados após a primeira chamada para essa função.

O valor padrão da coluna será recuperado quando a coluna não tiver sido definida explicitamente para outro valor, a menos que a opção JET_bitRetrieveIgnoreDefault esteja definida.

Recuperar o valor da coluna AutoIncrement do buffer de cópia antes da inserção é um meio comum de identificar um registro exclusivamente para vinculação ao inserir dados normalizados em várias tabelas. O valor de incremento automático é alocado quando a operação de inserção é iniciada e pode ser recuperada do buffer de cópia a qualquer momento até que a atualização seja concluída.

Ao recuperar todas as colunas marcadas, com valores múltiplos e esparsos, ao definir *columnid* como 0 (zero), as colunas são recuperadas na ordem *columnid* do menor *columnid* para a *columnid* mais alta. A mesma ordem dos valores de coluna é retornada cada vez que os valores de coluna são recuperados. A ordem é determinística.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
