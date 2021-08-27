---
description: 'Saiba mais sobre: EnumerateColumnsGrbit enumeration'
title: EnumerateColumnsGrbit enumeration
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c1e6f768d2f8a837416540bcd3ca31f8984e55ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466803"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>EnumerateColumnsGrbit enumeration

Opções para JetEnumerateColumns.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Membros


|  | Nome do membro | Descrição | 
|--|-------------|-------------|
|  | Nenhum | Opções padrão. | 
|  | EnumerateCompressOutput | Ao enumerar valores de coluna, todas as colunas para as quais estamos recuperando todos os valores e que têm apenas um valor de coluna não NULL podem ser retornadas em um formato compactado. O status dessas colunas será definido como <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> e o tamanho do valor da coluna e a memória que contém o valor da coluna será retornada diretamente na estrutura <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN.</a> Não há garantia de que todas as colunas qualificadas sejam compactadas dessa maneira. Consulte <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> para obter mais informações. | 
|  | EnumerateCopy | Essa opção indica que os valores de coluna modificados do registro devem ser enumerados em vez dos valores de coluna originais. Se um valor de coluna não tiver sido modificado, o valor da coluna original será enumerado. Dessa forma, um valor de coluna que ainda não foi inserido ou atualizado pode ser enumerado ao inserir ou atualizar um registro.<p>Essa opção é idêntica a <a href="hh578120(v=exchg.10).md">RetrieveCopy.</a></p> | 
|  | EnumerateIgnoreDefault | Se uma determinada coluna não estiver presente no registro, nenhum valor de coluna será retornado. Normalmente, o valor padrão da coluna, se algum, seria retornado nesse caso. É garantido que, se a coluna for definida como um valor diferente do valor padrão, esse valor diferente será retornado (ou seja, se uma coluna com um valor padrão for definida explicitamente como NULL, um NULL será retornado como o valor dessa coluna). Mesmo que essa opção seja solicitada, ainda é possível ver um valor de coluna que é igual ao valor padrão. Não é feito nenhum esforço para remover valores de coluna que corresponderem aos seus valores padrão. É importante lembrar que essa opção afeta a saída de <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> quando usada com EnumeratePresenceOnly ou EnumerateTaggedOnly. | 
|  | EnumeratePresenceOnly | Se existir um valor não NULL para o valor de coluna ou coluna solicitado, os dados associados não serão retornados. Em vez disso, o status associado para essa coluna ou valor de coluna será definido como <a href="hh557250(v=exchg.10).md">ColumnPresent.</a> Se o valor da coluna ou da coluna for NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> será retornado como de costume. | 
|  | EnumerateTaggedOnly | Ao enumerar todos os valores de coluna no registro (por exemplo, quando numColumnids é zero), somente os valores de coluna marcados serão retornados. Essa opção não é permitida ao enumerar uma matriz específica de IDs de coluna. | 



## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
