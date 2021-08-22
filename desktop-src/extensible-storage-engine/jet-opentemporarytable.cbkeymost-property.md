---
description: 'Saiba mais sobre: JET_OPENTEMPORARYTABLE.cbKeyMost'
title: JET_OPENTEMPORARYTABLE.cbKeyMost (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 225c801770bb41337ee9f3ae248092c60441cd2e9a059f64897ad19053bfe30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107695"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>JET_OPENTEMPORARYTABLE.cbKeyMost

Obtém ou define o tamanho máximo de uma chave que representa uma determinada linha. O tamanho máximo da chave pode ser definido para controlar como as chaves são truncadas. O truncamento de chave é importante porque pode afetar quando as linhas são consideradas distintas. Se esse parâmetro for definido como 0 ou 255, o tamanho máximo da chave e sua semântica permanecerão idênticos ao tamanho máximo da chave com suporte do Windows Server 2003. Esse parâmetro também pode ser definido como um valor maior como uma função do tamanho da página do banco de dados para a instância [DatabasePageSize](./jet-param-enumeration.md). Consulte [KeyMost](./vistaparam.keymost-field.md) para obter mais informações.

**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valor da propriedade

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_OPENTEMPORARYTABLE classe](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE membros](./jet-opentemporarytable-members.md)

[Namespace Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
