---
description: 'Saiba mais sobre: JET_OSSNAPID. Método ToString (String, IFormatProvider)'
title: JET_OSSNAPID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 95e93fd3a6bbf7f2fa3505fcb9480367b780ecc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788971"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a>JET_OSSNAPID. Método ToString (String, IFormatProvider)

Formata o valor da instância atual usando o formato especificado.

**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_OSSNAPID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Parâmetros

  - format  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    A [cadeia de caracteres](/dotnet/api/system.string) que especifica o formato a ser usado. -ou-NULL para usar o formato padrão definido para o tipo da implementação de [IFormattable](/dotnet/api/system.iformattable) .

<!-- end list -->

  - formatProvider  
    Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    O [IFormatProvider](/dotnet/api/system.iformatprovider) a ser usado para formatar o valor. -ou-NULL para obter as informações de formato numérico da configuração de localidade atual do sistema operacional.

#### <a name="return-value"></a>Retornar valor

Tipo: [System. String](/dotnet/api/system.string)  
Uma [cadeia de caracteres](/dotnet/api/system.string) que contém o valor da instância atual no formato especificado.  

#### <a name="implements"></a>Implementações

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_OSSNAPID](./jet-ossnapid-structure.md)

[Membros do JET_OSSNAPID](./jet-ossnapid-members.md)

[Sobrecarga de ToString](./jet-ossnapid.tostring-method.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
