---
description: 'Saiba mais sobre: JET_LS. Método ToString (String, IFormatProvider)'
title: JET_LS. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.tostring(v=EXCHG.10)
ms:contentKeyID: 39512228
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1011f8433b98925d8c3c08112dd1c4d0c5e6c2f3672b66ece5d6f11070f3d549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401326"
---
# <a name="jet_lstostring-method-string-iformatprovider"></a>JET_LS. Método ToString (String, IFormatProvider)

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
Dim instance As JET_LS
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

#### <a name="return-value"></a>Valor retornado

Tipo: [System. String](/dotnet/api/system.string)  
Uma [cadeia de caracteres](/dotnet/api/system.string) que contém o valor da instância atual no formato especificado.  

#### <a name="implements"></a>Implementações

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Estrutura de JET_LS](./jet-ls-structure.md)

[Membros do JET_LS](./jet-ls-members.md)

[Sobrecarga de ToString](./jet-ls.tostring-method2.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
