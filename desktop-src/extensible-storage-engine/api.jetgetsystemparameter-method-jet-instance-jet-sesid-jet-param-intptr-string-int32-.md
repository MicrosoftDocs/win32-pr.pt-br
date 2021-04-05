---
description: 'Saiba mais sobre: método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)'
title: Método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100731
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25e8430931cbf45c84d65fb68ae877ed96e7cea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826943"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string-int32"></a>Método API. JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)

Obtém as opções de configuração do banco de dados.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As IntPtr, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref IntPtr paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a>Parâmetros

  - instance  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    A instância da qual as opções são recuperadas.

<!-- end list -->

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - paramid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_param](./jet-param-enumeration.md)  
    
    O parâmetro a ser obtido.

<!-- end list -->

  - paramValue  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Retorna o valor do parâmetro, se o valor for um inteiro.

<!-- end list -->

  - paramstring  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Retorna o valor do parâmetro, se o valor for uma cadeia de caracteres.

<!-- end list -->

  - maxParam  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    O tamanho máximo da cadeia de caracteres do parâmetro.

#### <a name="return-value"></a>Retornar valor

Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Um código de aviso de ESENT.  

## <a name="remarks"></a>Comentários

[ErrorToString](./jet-param-enumeration.md) passa o número do erro no ParamValue, que é o motivo pelo qual ele é um parâmetro ref e não um parâmetro out.

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Sobrecarga de JetGetSystemParameter](./api.jetgetsystemparameter-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
