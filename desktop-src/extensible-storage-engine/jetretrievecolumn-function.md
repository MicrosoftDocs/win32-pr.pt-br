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
ms.openlocfilehash: f8a9ce96be028329dea18f32459fbde88b80b75f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985619"
---
# <a name="jetretrievecolumn-function"></a>Função JetRetrieveColumn


_**Aplica-se a:** Windows | Windows Servidor_

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


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Esse sinalizador faz com que a coluna de recuperação recupere o valor modificado em vez do valor original. Se o valor não tiver sido modificado, o valor original será recuperado. Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado durante a operação de inserção ou atualização de um registro.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Essa opção é usada para recuperar valores de coluna do índice, se possível, sem acessar o registro. Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice. Nos casos em que o valor da coluna original não puder ser recuperado do índice, devido a transformações irreversíveis ou truncamento de dados, o registro será acessado e os dados serão recuperados como normais. Essa é uma opção de desempenho e só deve ser especificada quando for provável que o valor da coluna possa ser recuperado do índice. Essa opção não deverá ser especificada se o índice atual for o índice clusterizado, já que as entradas de índice para o índice clusterizado ou primário são os próprios registros. Esse bit não poderá ser definido se JET_bitRetrieveFromPrimaryBookmark também for definido.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Essa opção é usada para recuperar valores de coluna do indicador de índice e pode ser diferente do valor de índice quando uma coluna aparece no índice primário e no índice atual. Essa opção não deverá ser especificada se o índice atual for o índice clusterizado ou primário. Esse bit não poderá ser definido se JET_bitRetrieveFromIndex também for definido.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Essa opção é usada para recuperar o número de sequência de um valor de coluna com valores múltiplos em pretinfo- &gt; itagSequence. Normalmente, o campo itagSequence é uma entrada para recuperar valores de coluna de vários valores de um registro. No entanto, ao recuperar valores de um índice, também é possível associar a entrada de índice a um número de sequência específico e recuperar esse número de sequência também. A recuperação do número de sequência pode ser uma operação dispendiosa e só deve ser feita se necessário.</p> | 
| <p>JET_bitRetrieveNull</p> | <p>Essa opção é usada para recuperar valores <strong>nulos</strong> de coluna de vários valores. Se essa opção não for especificada, os valores <strong>nulos</strong> da coluna com valores múltiplos serão automaticamente ignorados.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Essa opção afeta apenas as colunas com valores múltiplos e faz com que um valor <strong>nulo</strong> seja retornado quando o número de sequência solicitado é 1 e não há valores definidos para a coluna no registro.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</p> | 
| <p>JET_bitRetrieveTuple</p> | <p>Esse sinalizador permitirá a recuperação de um segmento de tupla do índice. Esse bit deve ser especificado com JET_bitRetrieveFromIndex.</p> | 



*pretinfo*

Se *pretinfo* for atribuído como **NULL** , a função se comporta como se um *ItagSequence* de 1 e um *ibLongValue* de 0 (zero) fossem fornecidos. Isso faz com que a recuperação de coluna recupere o primeiro valor de uma coluna com vários valores e recupere dados longos no deslocamento 0 (zero).

Esse parâmetro é usado para fornecer um ou mais dos seguintes itens:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>ibLongValue</p> | <p>Fornece um deslocamento binário em um valor de coluna longo ao recuperar uma parte de um valor de coluna.</p> | 
| <p>itagSequence</p> | <p>Fornece o número de sequência do valor de coluna com valores múltiplos desejado. Observe que esse campo só será definido se o JET_bitRetrieveTag for especificado. Caso contrário, ele não será modificado.</p> | 
| <p>columnidNextTagged</p> | <p>Retorna a ID de coluna do valor de coluna retornado ao recuperar todas as colunas marcadas, esparsas e com valores múltiplos usando a passagem de <em>columnid</em> de 0 (zero).</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBadColumnId</p> | <p>A ID de coluna fornecida está fora dos limites legais de uma ID de coluna.</p> | 
| <p>JET_errBadItagSequence</p> | <p>Um valor de número de sequência de coluna com valores múltiplos inválido foi passado em pretinfo- &gt; itagSequence. Os valores válidos para os números de sequência de valor de coluna com valores múltiplos são 1 ou mais. Um valor de 0 (zero) é inválido para esta função.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errColumnNotFound</p> | <p>A coluna descrita pelo <em>columnid</em> fornecido não existe na tabela.</p> | 
| <p>JET_errIndexTuplesCannotRetrieveFromIndex</p> | <p>As colunas indexadas como subcadeias de caracteres não podem ser recuperadas do índice, já que apenas uma pequena parte da coluna está normalmente presente em cada entrada de índice.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Em alguns casos, o buffer determinado para a coluna de recuperação deve ser dimensionado o suficiente para retornar qualquer quantidade do valor da coluna. Por exemplo, colunas atualizáveis de escrow são ajustadas para serem consistentes para o contexto transacional da sessão de chamada e esse ajuste requer o buffer fornecido pelo chamador. Se o espaço de buffer insuficiente for fornecido, JET_errInvalidBufferSize será retornado e nenhum dado de coluna será retornado.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um ou mais dos parâmetros determinados está incorreto. Isso poderá acontecer se o retinfo.cbStruct for menor que o tamanho <a href="gg294049(v=exchg.10).md">de JET_RETINFO</a>.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>As opções fornecidas são desconhecidas ou uma combinação ilegal de configurações de bits conhecidas.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>O cursor não está posicionado em um registro. Isso pode ocorrer por vários motivos diferentes. Por exemplo, isso ocorrerá se o cursor estiver posicionado no momento após o último registro no índice atual.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>A mesma sessão não pode ser usada para mais de um thread ao mesmo tempo.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>Não foi possível recuperar todo o valor da coluna porque o buffer determinado é menor que o tamanho da coluna.</p> | 
| <p>JET_wrnColumnNull</p> | <p>O valor da coluna recuperado é <strong>NULL.</strong></p> | 



Em caso de êxito, o valor da coluna para a coluna determinada é copiado para o buffer determinado. Menor que todo o valor da coluna é copiado com o aviso JET_wrnBufferTruncated é retornado. Se o *pcbActual* tiver sido dado, o tamanho real do valor da coluna será retornado. Observe que **os valores NULL** têm 0 (zero) de comprimento e, portanto, definirão o tamanho retornado como 0 (zero). Se a coluna recuperada for uma coluna com vários valores e o *pretinfo* tiver sido dado e JET_bitReturnTag tiver sido definido como uma opção, o número da sequência do valor da coluna será retornado em pretinfo- \> itagSequence.

Em caso de falha, o local do cursor permanece inalterado e nenhum dado é copiado para o buffer fornecido.

#### <a name="remarks"></a>Comentários

Essa chamada é usada apenas uma vez para recuperar dados de tamanho fixo ou conhecido para colunas sem valores múltiplos. No entanto, quando os dados de coluna são de tamanho desconhecido, essa chamada normalmente é usada duas vezes. Ele é chamado primeiro para determinar o tamanho dos dados para que possa alocar o espaço de armazenamento necessário. Em seguida, a mesma chamada é feita novamente para recuperar os dados da coluna. Quando o número real de valores é desconhecido, porque uma coluna tem vários valores, a chamada normalmente é usada três vezes. Primeiro, para obter o número de valores e, em seguida, mais duas vezes para alocar armazenamento e recuperar os dados reais.

Recuperar todos os valores de uma coluna com vários valores pode ser feito chamando repetidamente essa função com um valor pretinfo- itagSequence começando em 1 e aumentando em cada chamada \> subsequente. O valor da última coluna é conhecido por ser recuperado quando um JET_wrnColumnNull é retornado da função. Observe que esse método não poderá ser feito se a coluna de vários valores tiver valores **NULL** explícitos definidos em sua sequência de valor, pois esses valores seriam ignorados. Se um aplicativo desejar recuperar todos os valores de coluna com valores múltiplos, incluindo aqueles explicitamente definidos como **NULL,** [JetRetrieveColumns](./jetretrievecolumns-function.md) deverá ser usado em vez de **JetRetrieveColumn**. Observe que essa função não retorna o número de valores para uma função com vários valores quando um *valor itagSequence* de 0 (zero) é determinado. Somente [JetRetrieveColumns](./jetretrievecolumns-function.md) retornará o número de valores de um valor de coluna quando um *valor itagSequence* de 0 (zero) for passado.

Se essa função for chamada no nível da transação 0 (zero), por exemplo, a sessão de chamada não estiver em uma transação, uma transação será aberta e fechada dentro da função. A finalidade disso é retornar resultados consistentes no caso de um valor longo abranger páginas de banco de dados. Observe que a transação é liberada entre chamadas de função e uma série de chamadas para essa função quando a sessão não está em uma transação pode retornar dados atualizados após a primeira chamada para essa função.

O valor da coluna padrão será recuperado quando a coluna não tiver sido definida explicitamente como outro valor, a menos que JET_bitRetrieveIgnoreDefault opção seja definida.

Recuperar o valor da coluna de recremento automático do buffer de cópia antes da inserção é um meio comum de identificar um registro exclusivamente para vinculação ao inserir dados normalizados em várias tabelas. O valor de acremento automático é alocado quando a operação de inserção é iniciada e pode ser recuperado do buffer de cópia a qualquer momento até que a atualização seja concluída.

Ao recuperar todas as colunas marcadas, com valores múltiplos e esparsos, definindo *columnid* como 0 (zero), as colunas são recuperadas na ordem *columnid* do *columnid* mais baixo para o *columnid* mais alto. A mesma ordem de valores de coluna é retornada sempre que os valores de coluna são recuperados. A ordem é determinística.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RETINFO](./jet-retinfo-structure.md)  
[JetSetColumn](./jetretrievekey-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
