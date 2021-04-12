---
description: 'Saiba mais sobre: Enumeração CrashDumpGrbit'
title: Enumeração CrashDumpGrbit (Microsoft. ISAM. ESENT. Interop. windows7)
TOCTitle: CrashDumpGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.crashdumpgrbit(v=EXCHG.10)
ms:contentKeyID: 39515535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeDirtyPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMaximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheMinimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCachedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.CacheIncludeCorruptedPages
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Minimum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.Maximum
- Microsoft.Isam.Esent.Interop.Windows7.CrashDumpGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3108190143115b1e6be5b7e0981d49c4bd9d4afa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296497"
---
# <a name="crashdumpgrbit-enumeration"></a>Enumeração CrashDumpGrbit

Opções para JetConfigureProcessForCrashDump.

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CrashDumpGrbit
'Usage
Dim instance As CrashDumpGrbit
```

``` csharp
[FlagsAttribute]
public enum CrashDumpGrbit
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
<td>Mínimo</td>
<td>O mínimo de despejo inclui CacheMinimum.</td>
</tr>
<tr class="odd">
<td></td>
<td>Máximo</td>
<td>O máximo de despejo inclui CacheMaximum.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheMinimum</td>
<td>CacheMinimum inclui páginas que são travadas. CacheMinimum inclui páginas que são usadas para memória. CacheMinimum inclui páginas sinalizadas com erros.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheMaximum</td>
<td>O máximo de cache inclui o mínimo de cache. O máximo de cache inclui a imagem de cache inteira.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeDirtyPages</td>
<td>O despejo inclui páginas que são modificadas.</td>
</tr>
<tr class="odd">
<td></td>
<td>CacheIncludeCachedPages</td>
<td>O despejo inclui páginas que contêm dados válidos.</td>
</tr>
<tr class="even">
<td></td>
<td>CacheIncludeCorruptedPages</td>
<td>O despejo inclui páginas corrompidas (caras para computação).</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop. Windows7](./microsoft.isam.esent.interop.windows7-namespace.md)
