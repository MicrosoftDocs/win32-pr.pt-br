---
description: 'Saiba mais sobre: estrutura JET_CONDITIONALCOLUMN dados'
title: estrutura JET_CONDITIONALCOLUMN de dados
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
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
ms.openlocfilehash: dacaff181b40af870bd01bf9d287683c3d3d63a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469473"
---
# <a name="jet_conditionalcolumn-structure"></a>estrutura JET_CONDITIONALCOLUMN de dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_conditionalcolumn-structure"></a>estrutura JET_CONDITIONALCOLUMN de dados

A **JET_CONDITIONALCOLUMN** estrutura define como a indexação condicional é executada para um determinado índice. Um índice condicional contém uma entrada de índice apenas para as linhas que corresponderem à condição especificada. No entanto, a coluna condicional não faz parte da chave do índice, ela controla apenas a presença da entrada de índice.

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a>Membros

**Cbstruct**

Esse campo deve ser inicializado para sizeof( JET_CONDITIONALCOLUMN ), em bytes.

**szColumnName**

O nome da coluna que contém os dados nos quais o mecanismo de banco de dados está indexando condicionalmente a linha.

**grbit** Um grupo de bits que fornece as opções para o índice condicional. A passagem de zero ou valores **or** or ed logicamente não é válida para **JET_CONDITIONALCOLUMN**. O campo de bits deve ser exatamente um dos seguintes:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitIndexColumnMustBeNull</p> | <p>A coluna especificada pelo parâmetro <em>szColumnName</em> deve ser NULL para uma entrada de índice para uma determinada linha aparecer nesse índice.</p> | 
| <p>JET_bitIndexColumnMustBeNonNull</p> | <p>A coluna especificada pelo parâmetro <em>szColumnName</em> deve ser não NULL para uma entrada de índice para que uma determinada linha apareça nesse índice.</p> | 



### <a name="remarks"></a>Comentários

Um índice condicional contém uma entrada de índice apenas para as linhas que corresponderem à condição especificada. Por exemplo, uma coluna pode ser nomeada como "Marcada" e, quando uma linha é marcada, a coluna é definida como um valor não NULL. Um JET_bitIndexColumnMustBeNonNull condicional nesta coluna mostrará todas as linhas marcadas e um JET_bitIndexColumnMustBeNull condicional mostrará linhas que não estão marcadas. Essa também é uma maneira conveniente de executar um índice de exclusão de sinalizador e coleta de lixo.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) <strong>e JET_CONDITIONALCOLUMN_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Consulte Também

[JET_GRBIT](./jet-grbit.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)
