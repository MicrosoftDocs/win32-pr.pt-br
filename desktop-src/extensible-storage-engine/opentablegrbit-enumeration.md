---
description: 'Saiba mais sobre: Enumeração OpenTableGrbit'
title: Enumeração OpenTableGrbit
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767803"
---
# <a name="opentablegrbit-enumeration"></a>Enumeração OpenTableGrbit

Opções para JetOpenTable.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
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
<td>DenyWrite</td>
<td>Esta tabela não pode ser aberta para acesso de gravação por outra sessão.</td>
</tr>
<tr class="odd">
<td></td>
<td>DenyRead</td>
<td>Esta tabela não pode ser aberta para acesso de leitura por outra sessão.</td>
</tr>
<tr class="even">
<td></td>
<td>ReadOnly</td>
<td>Solicitar acesso somente leitura à tabela.</td>
</tr>
<tr class="odd">
<td></td>
<td>Atualizável</td>
<td>Solicitar acesso de gravação à tabela.</td>
</tr>
<tr class="even">
<td></td>
<td>PermitDDL</td>
<td>Permitir modificações DDL em uma tabela sinalizada como FixedDDL. Essa opção deve ser usada com DenyRead.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>Não armazenar em cache as páginas desta tabela.</td>
</tr>
<tr class="even">
<td></td>
<td>Li</td>
<td>Fornece uma dica de que a tabela provavelmente não está no cache do buffer e que a leitura prévia pode ser benéfica para o desempenho.</td>
</tr>
<tr class="odd">
<td></td>
<td>Sequencial</td>
<td>Suponha um padrão de acesso sequencial e páginas de banco de dados de pré-busca.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>A tabela pertence à classe 1 de estatísticas.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>A tabela pertence à classe 2 de estatísticas.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>A tabela pertence à classe de estatísticas 3.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>A tabela pertence às estatísticas classe 4.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>A tabela pertence à classe de estatísticas 5.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>A tabela pertence à classe de estatísticas 6.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>A tabela pertence à classe de estatísticas 7.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>A tabela pertence à classe de estatísticas 8.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>A tabela pertence à classe de estatísticas 9.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>A tabela pertence à classe de estatísticas 10.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>A tabela pertence à classe de estatísticas 11.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>A tabela pertence à classe de estatísticas 12.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>A tabela pertence à classe de estatísticas 13.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>A tabela pertence à classe de estatísticas 14.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>A tabela pertence à classe de estatísticas 15.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
