---
description: 'Saiba mais sobre: método API. JetRegisterCallback'
title: Método API. JetRegisterCallback
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763313"
---
# <a name="apijetregistercallback-method"></a>Método API. JetRegisterCallback

Permite que o aplicativo configure o mecanismo de banco de dados para emitir notificações para o aplicativo para eventos específicos. Essas notificações são associadas a uma tabela específica e permanecem em vigor somente até que a instância que contém a tabela seja desligada usando [JetTerm (JET_INSTANCE)](./api.jetterm-method.md).

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a>Parâmetros

  - sesid  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    A sessão a ser usada.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Um cursor aberto na tabela em que o retorno de chamada deve ser registrado.

<!-- end list -->

  - cbtyp  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)  
    
    Os motivos de retorno de chamada para os quais o aplicativo deseja receber notificações.

<!-- end list -->

  - retorno de chamada  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)  
    
    A função do retorno de chamada.

<!-- end list -->

  - contexto  
    Tipo: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Um contexto que será dado ao retorno de chamada.

<!-- end list -->

  - retorno de chamada  
    Tipo: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)  
    
    Um identificador que pode ser usado posteriormente para cancelar o registro da função de retorno de chamada fornecida usando [JetUnregisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp JET_HANDLE)](./api.jetunregistercallback-method.md).

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Membros da API](./api-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
