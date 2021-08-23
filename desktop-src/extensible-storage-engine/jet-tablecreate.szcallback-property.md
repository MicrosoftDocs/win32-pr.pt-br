---
description: 'Saiba mais sobre a propriedade: JET_TABLECREATE. szCallback'
title: Propriedade JET_TABLECREATE. szCallback
TOCTitle: 'szCallback property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.szcallback(v=EXCHG.10)
ms:contentKeyID: 55103969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 414abc99547a07f46902a355efcb42ce01cd6bde24c84d3a0ca309b008ef02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729056"
---
# <a name="jet_tablecreateszcallback-property"></a>Propriedade JET_TABLECREATE. szCallback

Obtém ou define uma função de retorno de chamada a ser usada para a tabela. Isso está no formato "módulo \! FunctionName" e pressupõe código não gerenciado. Consulte **JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)** para obter uma alternativa.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szCallback As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szCallback

instance.szCallback = value
```

``` csharp
public string szCallback { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe JET_TABLECREATE](./jet-tablecreate-class.md)

[Membros do JET_TABLECREATE](./jet-tablecreate-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
