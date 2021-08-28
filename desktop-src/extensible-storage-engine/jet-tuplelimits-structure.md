---
description: 'Saiba mais sobre: estrutura JET_TUPLELIMITS dados'
title: estrutura JET_TUPLELIMITS dados
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
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
ms.openlocfilehash: dc5a71328681e1ce415b1a34e9c8f718b460e7f0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471772"
---
# <a name="jet_tuplelimits-structure"></a>estrutura JET_TUPLELIMITS dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_tuplelimits-structure"></a>estrutura JET_TUPLELIMITS dados

A **JET_TUPLELIMITS** permite a personalização das características do índice de tupla por índice, em vez de uma base por instância, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** A **JET_TUPLELIMITS** é introduzida no Windows Server 2003.

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a>Membros

**chLengthMin**

O comprimento mínimo de uma tupla. O valor padrão é 3.

**chLengthMax**

O comprimento máximo de uma tupla. O valor padrão é 10.

**chToIndexMax**

O comprimento máximo de uma cadeia de caracteres a ser indexado. Por exemplo, se uma coluna tiver 100 caracteres e **chToIndexMax** estiver definida como 60, somente os primeiros 60 caracteres da coluna serão indexados. O valor padrão é 32767.

**cchIncrement**

Isso permite que o passo a passo seja configurado por índice.

**Windows Vista:** O **membro cchIncrement** é introduzido no Windows Vista. Antes de Windows Vista, o valor para deslocar a janela (o "stride") sempre era 1, como é mostrado no exemplo na seção de comentários.

**ichStart**

O deslocamento no valor para começar a recuperar tuplas do valor.

**Windows Vista:** O **membro ichStart** é introduzido no Windows Vista.

### <a name="remarks"></a>Comentários

Um índice de tupla percorre uma cadeia de caracteres e indexa todas as suas substrings possíveis **de chLengthMax.** No final da cadeia de caracteres (ou na posição **chToIndexMax**, o que ocorrer primeiro), as substrings de pelo menos **chLengthMin** serão indexadas.

Um índice de tupla pode ser usado para pesquisar cadeias de caracteres com curingas à frente e à frente.

Supondo uma linha com um campo de texto "RAIN IN SPAIN", se um índice de tupla for criado com os \! parâmetros **chLengthMin**=2 e **chLengthMax**=3, as seguintes entradas serão criadas no índice:

"RG"  
"VOU"  
"IN"  
"N I"  
"IN"  
"IN"  
"N S"  
" SP"  
"SPA"  
"PAI"  
"VOU"  
\!"IN"  
\!"N"

Observe que "IN" ocorre duas vezes e que a última entrada ("N ") é menor \! que 3 (**chLengthMax**). Observe também que o algoritmo de divisão não está ciente de espaços ou palavras e trata todos os caracteres de forma idêntica.

**Windows XP:** Windows XP dá suporte a índices de tupla, mas não tem **JET_TUPLELIMITS**. O mecanismo de banco de dados utilizará os valores padrão (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767). Ainda é possível alterar esses valores, mas eles são definidos por instância usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)e [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
