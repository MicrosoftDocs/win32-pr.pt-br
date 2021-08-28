---
description: 'Saiba mais sobre: estrutura de JET_COLUMNDEF'
title: Estrutura JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: fccf3b076b71e8923366a95810d1f3009d4fe1c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471132"
---
# <a name="jet_columndef-structure"></a>Estrutura JET_COLUMNDEF


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_columndef-structure"></a>Estrutura JET_COLUMNDEF

A estrutura de **JET_COLUMNDEF** define os dados que podem ser armazenados em uma coluna.

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a>Membros

**cbStruct**

O tamanho da estrutura, em bytes. Ele deve ser definido como sizeof (JET_COLUMNDEF).

**columnid**

Reservado. **columnid** deve ser definido como 0 (zero).

**coltyp**

O tipo da coluna (por exemplo, texto, binário ou numérico). Para obter mais informações, consulte [JET_COLTYP](./jet-coltyp.md).

**wCountry**

Reservado. **wCountry** deve ser definido como 0 (zero).

**langid**

Obsoleto. **LangID** deve ser definido como 0 (zero).

**cp**

A página de código da coluna. Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200). Um valor de zero significa que o padrão será usado (Inglês, 1252). Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.

**wCollate**

Reservado. **wCollate** deve ser definido como 0 (zero).

**cbMax**

O comprimento máximo, em bytes, de uma coluna de comprimento variável ou o comprimento de uma coluna de comprimento fixo.

**grbit**

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitColumnFixed</p> | <p>A coluna será corrigida. Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que está sendo armazenada na coluna. JET_bitColumnFixed não pode ser usada com JET_bitColumnTagged. Esse bit não pode ser usado com valores longos ( <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>).</p> | 
| <p>JET_bitColumnTagged</p> | <p>A coluna será marcada. As colunas marcadas não ocupam nenhum espaço no banco de dados se não contiverem. Esse bit não pode ser usado com JET_bitColumnFixed.</p> | 
| <p>JET_bitColumnNotNULL</p> | <p>A coluna nunca deve ser definida como um valor nulo.</p> | 
| <p>JET_bitColumnVersion</p> | <p>A coluna é uma coluna de versão que especifica a versão da linha. O valor desta coluna começa em zero e será incrementado automaticamente para cada atualização na linha.</p><p>Esse bit só pode ser aplicado a <strong>JET_coltypLong</strong> colunas. Esse bit não pode ser usado com JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate ou JET_bitColumnTagged.</p> | 
| <p>JET_bitColumnAutoincrement</p> | <p>A coluna será incrementada automaticamente. O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela. No entanto, os números podem não ser contínuos. Por exemplo, se cinco linhas forem inseridas em uma tabela, a coluna "incremento automático" poderá conter os valores {1, 2, 6, 7, 8}. Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</p><p><strong>Windows 2000:</strong> no Windows 2000, esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong>.</p> | 
| <p>JET_bitColumnUpdatable</p> | <p>Esse bit é válido somente em chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</p> | 
| <p>JET_bitColumnTTKey</p> | <p>Esse bit é válido somente em chamadas para <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</p> | 
| <p>JET_bitColumnTTDescending</p> | <p>Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</p> | 
| <p>JET_bitColumnMultiValued</p> | <p>A coluna pode ter valores múltiplos. Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela. Os vários valores em uma coluna com valores múltiplos são identificados por um número chamado membro <strong>itagSequence</strong> , que pertence a várias estruturas, incluindo: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>e <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>. Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ter colunas de comprimento fixo ou de comprimento variável.</p> | 
| <p>JET_bitColumnEscrowUpdate</p> | <p>Especifica que uma coluna é uma coluna de atualização de caução. Uma coluna de atualização de caução pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manterá a consistência transacional. Uma coluna de atualização de caução também deve atender às seguintes condições:</p><ul><li><p>Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</p></li></ul><ul><li><p>Uma coluna de atualização de caução deve ser do tipo <strong>JET_coltypLong</strong>.</p></li></ul><ul><li><p>Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</p></li></ul><ul><li><p>JET_bitColumnEscrowUpdate não pode ser usado em conjunto com JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</p></li></ul> | 
| <p>JET_bitColumnUnversioned</p> | <p>A coluna será criada em uma sem informações de versão. Isso significa que outras transações que tentam adicionar uma coluna com o mesmo nome falharão. Esse bit só é útil com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>. Ele não pode ser usado em uma transação.</p> | 
| <p>JET_bitColumnMaybeNull</p> | <p>Reservado para uso futuro.</p> | 
| <p>JET_bitColumnFinalize</p> | <p>Use JET_bitColumnDeleteOnZero em vez de JET_bitColumnFinalize. JET_bitColumnFinalize que uma coluna pode ser finalizada. Quando uma coluna que pode ser finalizada tem uma coluna de atualização de caução que chega a zero, a linha será excluída. Versões futuras podem invocar uma função de chamada de retorno (para obter mais informações, consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>). Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução. JET_bitColumnFinalize não pode ser usada com JET_bitColumnUserDefinedDefault.</p> | 
| <p>JET_bitColumnUserDefinedDefault</p> | <p>O valor padrão de uma coluna será fornecido por uma função de retorno de chamada. Consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>. Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada. Especificar JET_bitColumnUserDefinedDefault significa que <strong>pvDefault</strong> deve apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve ser definido como sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</p><ul><li><p>JET_bitColumnUserDefinedDefault não pode ser usado em conjunto com JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</p></li></ul> | 
| <p>JET_bitColumnDeleteOnZero</p> | <p>A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído. Um uso comum para uma coluna que pode ser finalizada é usá-la como um campo de contagem de referência e quando o campo atinge zero, o registro é excluído. JET_bitColumnDeleteOnZero está relacionado a JET_bitColumnFinalize. Uma coluna Delete-on-zero deve ser uma coluna de atualização de escrow. JET_bitColumnDeleteOnZero pode ser usado com JET_bitColumnFinalize. JET_bitColumnDeleteOnZero pode ser usado com colunas padrão definidas pelo usuário.</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_COLTYP](./jet-coltyp.md)  
[JET_COLUMNCREATE](./jet-columncreate-structure.md)  
[JET_COLUMNID](./jet-columnid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md)  
[JetAddColumn](./jetaddcolumn-function.md)  
[JetEscrowUpdate](./jetescrowupdate-function.md)  
[JetGetTableColumnInfo](./jetgettablecolumninfo-function.md)  
[JetOpenTempTable](./jetopentemptable-function.md)  
[JetOpenTempTable2](./jetopentemptable2-function.md)  
[JetOpenTempTable3](./jetopentemptable3-function.md)  
[JetRenameColumn](./jetrenamecolumn-function.md)
