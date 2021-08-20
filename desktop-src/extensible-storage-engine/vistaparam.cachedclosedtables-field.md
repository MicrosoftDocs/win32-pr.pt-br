---
description: 'Saiba mais sobre: campo VistaParam. CachedClosedTables'
title: Campo VistaParam. CachedClosedTables (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 444456bc49b1cf2358feb32cadb36bec85cef5585436639dcf38caa02308af34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038654"
---
# <a name="vistaparamcachedclosedtables-field"></a>Campo VistaParam. CachedClosedTables

Esse parâmetro controla o número de recursos da árvore B + em cache pela instância depois que as tabelas que eles representam foram fechadas pelo aplicativo. Valores grandes para esse parâmetro farão com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com que um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo. Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaParam](./vistaparam-class.md)

[Membros do VistaParam](./vistaparam-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
