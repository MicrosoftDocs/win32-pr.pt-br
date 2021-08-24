---
description: 'Saiba mais sobre: método DurableCommitCallback. ReleaseResource'
title: Método DurableCommitCallback. ReleaseResource (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 758c27b1b3a67b91b7921276ec26e9c9776b65255c4cfa88d32b839f9950c2af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725266"
---
# <a name="durablecommitcallbackreleaseresource-method"></a>Método DurableCommitCallback. ReleaseResource

Libera a sessão de confirmação durável.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a>Comentários

Não tente definir o parâmetro de instância como NULL, pois o retorno de chamada é descartado após JetTerm e o retorno de chamada não pode ser definido após JetTerm.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe DurableCommitCallback](./durablecommitcallback-class.md)

[Membros do DurableCommitCallback](./durablecommitcallback-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
