---
description: 'Saiba mais sobre: EsentErrorException. Error Property'
title: Propriedade EsentErrorException. Error
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentErrorException.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.error(v=EXCHG.10)
ms:contentKeyID: 55101646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.get_Error
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e777886ed95ea72a02626f7eb91724123a495f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171744"
---
# <a name="esenterrorexceptionerror-property"></a>Propriedade EsentErrorException. Error

Obtém o erro de ESENT subjacente para esta exceção.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public ReadOnly Property Error As JET_err
    Get
'Usage
Dim instance As EsentErrorException
Dim value As JET_err

value = instance.Error
```

``` csharp
public JET_err Error { get; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe EsentErrorException](./esenterrorexception-class.md)

[Membros do EsentErrorException](./esenterrorexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
