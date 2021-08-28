---
description: 'Saiba mais sobre: estrutura de JET_RETRIEVECOLUMN'
title: Estrutura JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN Structure
ms:assetid: 8e23bed5-5279-4733-b787-a073a0e8d5a5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269334(v=EXCHG.10)
ms:contentKeyID: 32765623
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52b8a36946776ad43120f13e85d9ef7678594337
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983129"
---
# <a name="jet_retrievecolumn-structure"></a>Estrutura JET_RETRIEVECOLUMN


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_retrievecolumn-structure"></a>Estrutura JET_RETRIEVECOLUMN

A estrutura de **JET_RETRIEVECOLUMN** contém parâmetros de entrada e saída para [JetRetrieveColumns](./jetretrievecolumns-function.md). Os campos na estrutura descrevem o valor da coluna a ser recuperado, como recuperá-lo e onde salvar os resultados.

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      void* pvData;
      unsigned long cbData;
      unsigned long cbActual;
      JET_GRBIT grbit;
      unsigned long ibLongValue;
      unsigned long itagSequence;
      JET_COLUMNID columnidNextTagged;
      JET_ERR err;
    } JET_RETRIEVECOLUMN;
```

### <a name="members"></a>Membros

**columnid**

O identificador de coluna para a coluna a ser recuperada.

**pvData**

Um ponteiro para começar a armazenar dados recuperados do valor da coluna.

**cbData**

O tamanho da alocação que começa em **pvData**, em bytes. A operação de recuperação de coluna não armazenará mais dados em **pvData** do que **cbData**.

**cbActual**

O tamanho, em bytes, dos dados recuperados por uma operação de recuperação de coluna.

**grbit**

Um grupo de bits que contém as opções de recuperação de coluna, que incluem zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitRetrieveCopy</p> | <p>Recupera o valor modificado em vez do valor original. Se o valor não tiver sido modificado, o valor original será recuperado. Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado quando um registro é inserido ou atualizado.</p> | 
| <p>JET_bitRetrieveFromIndex</p> | <p>Recupera valores de coluna do índice sem acessar o registro, se possível. Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice. Nos casos em que o valor da coluna original não puder ser recuperado do índice, devido a transformações irreversíveis ou truncamento de dados, o registro será acessado e os dados serão recuperados como normais. Essa é uma opção de desempenho e só deve ser especificada quando for provável que o valor da coluna possa ser recuperado do índice. Essa opção não deverá ser especificada se o índice atual for o índice clusterizado, já que as entradas de índice para o índice clusterizado ou primário são os próprios registros. Esse bit não poderá ser definido se JET_bitRetrieveFromPrimaryBookmark também for definido.</p> | 
| <p>JET_bitRetrieveFromPrimaryBookmark</p> | <p>Recupera valores de coluna do indicador de índice e pode diferir do valor de índice quando uma coluna aparece no índice primário e no índice atual. Essa opção não deverá ser especificada se o índice atual for o índice clusterizado ou primário. Esse bit não poderá ser definido se JET_bitRetrieveFromIndex também for definido.</p> | 
| <p>JET_bitRetrieveTag</p> | <p>Recupera o número de sequência de um valor de coluna com valores múltiplos em pretinfo- &gt; itagSequence. O campo itagSequence geralmente é usado como uma entrada para recuperar valores de coluna de vários valores de um registro. No entanto, ao recuperar valores de um índice, também é possível associar a entrada de índice a um número de sequência específico e recuperar esse número de sequência também. A recuperação do número de sequência pode ser uma operação dispendiosa e só deve ser feita se necessário.</p> | 
| <p>JET_ bitRetrieveNull</p> | <p>Recupera valores nulos da coluna de valores múltiplos. Se essa opção não for especificada, os valores nulos da coluna com valores múltiplos serão automaticamente ignorados.</p> | 
| <p>JET_bitRetrieveIgnoreDefault</p> | <p>Faz com que um valor nulo seja retornado quando o número de sequência solicitado é 1 e não há valores definidos para a coluna no registro. Essa opção afeta apenas as colunas com valores múltiplos.</p> | 
| <p>JET_bitRetrieveLongId</p> | <p>Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</p> | 
| <p>JET_bitRetrieveLongValueRefCount</p> | <p>Esse sinalizador é somente para uso interno e não se destina a ser usado em seu aplicativo.</p> | 



**ibLongValue**

O deslocamento para o primeiro byte a ser recuperado de uma coluna do tipo [JET_coltypLongBinary](./jet-coltyp.md) ou [JET_coltypLongText](./jet-coltyp.md).

**itagSequence**

O número de sequência dos valores contidos em uma coluna com valores múltiplos. **itagSequence** aqui na **JET_RETRIEVECOLUMN** pode ser 0. Se **itagSequence** for 0, o número de instâncias de uma coluna com vários valores será retornado em vez de quaisquer dados de coluna. Um valor de **itagSequence** de 0 não pode ser usado em chamadas para [JetRetrieveColumn](./jetretrievecolumn-function.md).

**columnidNextTagged**

O **columnid** da coluna marcada, com vários valores ou esparsos quando todas as colunas marcadas são recuperadas passando 0 como **columnid** para [JetRetrieveColumn](./jetretrievecolumn-function.md).

**erra**

Códigos de erro e avisos retornados da recuperação da coluna.

### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_RETRIEVECOLUMN]()  
[JetRetrieveColumn](./jetretrievecolumn-function.md)  
[JetRetrieveColumns](./jetretrievecolumns-function.md)
