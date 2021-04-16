---
description: 'Saiba mais sobre: classe EsentSPOwnExtCorruptedException'
title: Classe EsentSPOwnExtCorruptedException
TOCTitle: EsentSPOwnExtCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentspownextcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102983
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSPOwnExtCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 15f3f37dfafcaa58d63a34c19d629f4469826cd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750524"
---
# <a name="esentspownextcorruptedexception-class"></a>Classe EsentSPOwnExtCorruptedException

Classe base para JET_err. SPOwnExtCorrupted exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentSPOwnExtCorruptedException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSPOwnExtCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSPOwnExtCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSPOwnExtCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentSPOwnExtCorruptedException](./esentspownextcorruptedexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
