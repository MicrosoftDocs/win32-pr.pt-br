---
description: 'Saiba mais sobre: enumeração de JET_prep'
title: Enumeração de JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788942"
---
# <a name="jet_prep-enumeration"></a>Enumeração de JET_prep

Tipos de atualização para JetPrepareUpdate.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
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
<td>Inserir</td>
<td>Esse sinalizador faz com que o cursor se prepare para uma inserção de um novo registro. Todos os dados são inicializados para o estado padrão do registro. Se a tabela tiver uma coluna de incremento automático, um novo valor será atribuído a esse registro, independentemente de a atualização ter êxito ou não ser cancelada.</td>
</tr>
<tr class="even">
<td></td>
<td>Substitua</td>
<td>Esse sinalizador faz com que o cursor se prepare para uma substituição do registro atual. Se a tabela tiver uma coluna de versão, a coluna versão será definida como o próximo valor em sua sequência. Se essa atualização não for concluída, o valor da versão no registro não será afetado. Um bloqueio de atualização é obtido no registro para impedir que outras sessões atualizem esse registro antes da conclusão desta sessão.</td>
</tr>
<tr class="odd">
<td></td>
<td>Cancelar</td>
<td>Esse sinalizador faz com que JetPrepareUpdate cancele a atualização para este cursor.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Esse sinalizador é semelhante a JET_prepReplace, mas nenhum bloqueio é usado para impedir que outras sessões atualizem esse registro. Em vez disso, essa sessão pode receber JET_errWriteConflict quando chama JetUpdate para concluir a atualização.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Esse sinalizador faz com que o cursor se prepare para uma inserção de uma cópia do registro existente. Deve haver um registro atual se essa opção for usada. O estado inicial do novo registro é copiado do registro atual. Valores longos armazenados fora do registro são praticamente copiados.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Esse sinalizador faz com que o cursor se prepare para uma inserção do mesmo registro e um Delete ou o registro original. Ele é usado em casos em que a chave primária foi alterada.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
