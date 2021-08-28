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
ms.openlocfilehash: 6c8280bf4abfbc9eb5818d1aab460a17298db7b0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477452"
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


|  | Nome do membro | Descrição | 
|--|-------------|-------------|
|  | Tudo | Interrompe todos os serviços ESE para a instância especificada. | 
|  | BackgroundUserTasks | Interrompe tarefas de manutenção em segundo plano específicas do cliente reiniciáveis (desfragmentação da árvore B +). | 
|  | QuiesceCaches | Quiesces todos os caches sujos em disco. Assíncrono. O fechamento em pausa será cancelado se o bit de retomação for chamado posteriormente. | 
|  | Retomar | Retoma as operações StopService emitidas anteriormente, ou seja, "reinicia o serviço". Pode ser combinado com grbits acima para retomar serviços específicos ou com 0x0 retoma todos os serviços interrompidos anteriormente.<p>Aviso: esse bit só pode ser usado para retomar JET_bitStopServiceBackground e JET_bitStopServiceQuiesceCaches, se você fez uma JET_bitStopServiceAll ou JET_bitStopServiceAPI, a tentativa de usar JET_bitStopServiceResume falhará.</p> | 



## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
