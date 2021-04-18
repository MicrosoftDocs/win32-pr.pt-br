---
description: 'Saiba mais sobre: Instance.Inimétodo t (JET_RSTINFO, InitGrbit)'
title: Método t Instance.Ini(JET_RSTINFO, InitGrbit)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1945b0119053a2759b57b8781b86cf682b3a364c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784648"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a>Método t Instance.Ini(JET_RSTINFO, InitGrbit)

Inicialize o JET_INSTANCE. Essa API requer pelo menos a versão vista do ESENT.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Parâmetros

  - recuperação de  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Parâmetros de recuperação adicionais para remapear bancos de dados durante a recuperação, posicione onde parar a recuperação ou status de recuperação.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)  
    
    Opções de inicialização.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de instância](./instance-class.md)

[Membros da Instância ](./instance-members.md)

[Sobrecarga de init](./instance.init-method2.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
