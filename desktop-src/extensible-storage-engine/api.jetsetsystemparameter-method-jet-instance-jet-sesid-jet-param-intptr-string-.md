---
description: 'Saiba mais sobre: método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres)'
title: Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres)
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100822
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a92ea3d6b6d4b828e409cd08b896f54c4aa053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170768"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string"></a>Método API. JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres)

Define opções de configuração do banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As IntPtr, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    IntPtr paramValue,
    string paramString
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância na qual definir a opção ou [nil](./jet-instance.nil-property.md) para definir a opção em todas as instâncias.

<!-- end list -->

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - paramid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)  
    
    O parâmetro a ser definido.

<!-- end list -->

  - paramValue  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    O valor do parâmetro a ser definido, se o parâmetro for um tipo inteiro.

<!-- end list -->

  - paramstring  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    O valor do parâmetro a ser definido, se o parâmetro for um tipo de cadeia de caracteres.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Um código de aviso de ESENT.  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetSetSystemParameter](./api.jetsetsystemparameter-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
