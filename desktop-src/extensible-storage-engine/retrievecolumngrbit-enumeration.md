---
description: 'Saiba mais sobre: Enumeração RetrieveColumnGrbit'
title: Enumeração RetrieveColumnGrbit
TOCTitle: RetrieveColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.retrievecolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39511391
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromIndex
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveCopy
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveNull
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.None
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveFromPrimaryBookmark
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveIgnoreDefault
- Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit.RetrieveTag
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7bd59f610b2ff1423b82539c61eff3d9d770a03d6f8291a1bae53b372fff318f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890664"
---
# <a name="retrievecolumngrbit-enumeration"></a>Enumeração RetrieveColumnGrbit

Opções para JetRetrieveColumn.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RetrieveColumnGrbit
'Usage
Dim instance As RetrieveColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum RetrieveColumnGrbit
```

## <a name="members"></a>Membros

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome do membro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Nenhum</td>
<td>Opções padrão.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveCopy</td>
<td>Esse sinalizador faz com que a coluna de recuperação recupere o valor modificado em vez do valor original. Se o valor não tiver sido modificado, o valor original será recuperado. Dessa forma, um valor que ainda não foi inserido ou atualizado pode ser recuperado durante a operação de inserção ou atualização de um registro.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveFromIndex</td>
<td>Essa opção é usada para recuperar valores de coluna do índice, se possível, sem acessar o registro. Dessa forma, o carregamento desnecessário de registros pode ser evitado quando os dados necessários estão disponíveis nas próprias entradas de índice.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveFromPrimaryBookmark</td>
<td>Essa opção é usada para recuperar valores de coluna do indicador de índice e pode ser diferente do valor do índice quando uma coluna aparece no índice primário e no índice atual. Essa opção não deve ser especificada se o índice atual for o índice cluster ou primário. Esse bit não poderá ser definido se RetrieveFromIndex também estiver definido.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveTag</td>
<td>Essa opção é usada para recuperar o número de sequência de um valor de coluna com vários valores em JET_RETINFO.itagSequence. A recuperação do número de sequência pode ser uma operação cara e só deve ser feita se necessário.</td>
</tr>
<tr class="even">
<td></td>
<td>RetrieveNull</td>
<td>Essa opção é usada para recuperar valores NULL de coluna com vários valores. Se essa opção não for especificada, os valores NULL da coluna com valores múltiplos serão ignorados automaticamente.</td>
</tr>
<tr class="odd">
<td></td>
<td>RetrieveIgnoreDefault</td>
<td>Essa opção afeta apenas colunas com vários valores e faz com que um valor NULL seja retornado quando o número de sequência solicitado for 1 e não houver valores definidos para a coluna no registro.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
