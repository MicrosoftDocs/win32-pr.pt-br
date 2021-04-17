---
description: 'Saiba mais sobre: Enumeração StopServiceGrbit'
title: Enumeração StopServiceGrbit (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761197"
---
# <a name="stopservicegrbit-enumeration"></a>Enumeração StopServiceGrbit

Opções para [JetStopServiceInstance2 (JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).

Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>Membros

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>Tudo</td>
<td>Interrompe todos os serviços ESE para a instância especificada.</td>
</tr>
<tr class="even">
<td></td>
<td>BackgroundUserTasks</td>
<td>Interrompe tarefas de manutenção em segundo plano específicas do cliente reiniciáveis (desfragmentação da árvore B +).</td>
</tr>
<tr class="odd">
<td></td>
<td>QuiesceCaches</td>
<td>Quiesces todos os caches sujos em disco. Assíncrono. O fechamento em pausa será cancelado se o bit de retomação for chamado posteriormente.</td>
</tr>
<tr class="even">
<td></td>
<td>Retomar</td>
<td>Retoma as operações StopService emitidas anteriormente, ou seja, &quot; reinicia o serviço &quot; . Pode ser combinado com grbits acima para retomar serviços específicos ou com 0x0 retoma todos os serviços interrompidos anteriormente.
<p>Aviso: esse bit só pode ser usado para retomar JET_bitStopServiceBackground e JET_bitStopServiceQuiesceCaches, se você fez uma JET_bitStopServiceAll ou JET_bitStopServiceAPI, a tentativa de usar JET_bitStopServiceResume falhará.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
