---
description: 'Saiba mais sobre: classe EsentPageNotInitializedException'
title: Classe EsentPageNotInitializedException
TOCTitle: EsentPageNotInitializedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpagenotinitializedexception(v=EXCHG.10)
ms:contentKeyID: 55107308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPageNotInitializedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c349560498993d0920f344ef716835afa8fb62c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297168"
---
# <a name="esentpagenotinitializedexception-class"></a>Classe EsentPageNotInitializedException

Classe base para JET_err. PageNotInitialized exceções.

## <a name="inheritance-hierarchy"></a>Hierarquia de herança

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. EsentException](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. EsentErrorException](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. EsentDataException](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. EsentCorruptionException](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. EsentPageNotInitializedException  

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPageNotInitializedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPageNotInitializedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPageNotInitializedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Acesso thread-safe

Qualquer membro estático público (Shared no Visual Basic) desse tipo é seguro para threads. Não há garantia de que qualquer membro de instância seja seguro para threads.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Membros do EsentPageNotInitializedException](./esentpagenotinitializedexception-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
