---
description: 'Saiba mais sobre: estrutura de JET_TUPLELIMITS'
title: Estrutura de JET_TUPLELIMITS
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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922844"
---
# <a name="jet_tuplelimits-structure"></a>Estrutura de JET_TUPLELIMITS


_**Aplica-se a:** Windows | Windows Server_

## <a name="jet_tuplelimits-structure"></a>Estrutura de JET_TUPLELIMITS

A estrutura de **JET_TUPLELIMITS** permite a personalização das características de índice de tupla em uma base por índice, em vez de uma base por instância, usando [JetSetSystemParameter](./jetsetsystemparameter-function.md).

**Windows Server 2003:** A estrutura de **JET_TUPLELIMITS** é introduzida no Windows Server 2003.

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

O comprimento máximo de uma cadeia de caracteres a ser indexada. Por exemplo, se uma coluna tiver 100 caracteres de comprimento e **chToIndexMax** for definido como 60, somente os primeiros 60 caracteres da coluna serão indexados. O valor padrão é 32767.

**cchIncrement**

Isso permite que o stride seja configurado em uma base por índice.

**Windows Vista:** O membro **cchIncrement** é introduzido no Windows Vista. Antes do Windows Vista, o valor para mudar a janela (o "Stride") era sempre 1, como é mostrado no exemplo na seção comentários.

**ichStart**

O deslocamento no valor para começar a recuperar tuplas do valor.

**Windows Vista:** O membro **ichStart** é introduzido no Windows Vista.

### <a name="remarks"></a>Comentários

Um índice de tupla percorre uma cadeia de caracteres e indexa todas as subcadeias de caracteres possíveis de **chLengthMax**. No final da cadeia de caracteres (ou na posição **chToIndexMax**, o que ocorrer primeiro), as subcadeias de pelo menos **chLengthMin** serão indexadas.

Um índice de tupla pode ser usado para pesquisar cadeias de caracteres com curingas à esquerda e à direita.

Supondo uma linha com um campo de texto de "chuva na Espanha \! ", se um índice de tupla for criado com os parâmetros **chLengthMin**= 2 e **chLengthMax**= 3, as seguintes entradas serão criadas no índice:

"RAI"  
Ain  
NO  
"N I"  
NO  
NO  
"N S"  
SP3  
AUTENTICAÇÃO  
"PAI"  
Ain  
"IN \! "  
"N \! "

Observe que "IN" ocorre duas vezes e que a última entrada ("N \! ") é menor que 3 (**chLengthMax**). Observe também que o algoritmo de divisão não está ciente de espaços ou palavras e trata todos os caracteres de forma idêntica.

**Windows XP:** O Windows XP dá suporte a índices de tupla, mas não tem **JET_TUPLELIMITS**. O mecanismo de banco de dados usará os valores padrão (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767). Ainda é possível alterar esses valores, mas eles são definidos em uma base por instância usando [JetSetSystemParameter](./jetsetsystemparameter-function.md) com [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)e [JET_paramIndexTuplesToIndexMax](./index-parameters.md).

### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JET_COLTYP](./jet-coltyp.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS]()  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
