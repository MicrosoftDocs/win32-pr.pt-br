---
description: 'Saiba mais sobre: JET_DBID. Método ToString (String, IFormatProvider)'
title: JET_DBID. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b6fca1494a31bc342d4f8ad2933968c58efacc5f5e115ff10fe92a8afbabca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017254"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a>JET_DBID. Método ToString (String, IFormatProvider)

Formata o valor da instância atual usando o formato especificado.

**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_DBID
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
    Tipo: [System.String](/dotnet/api/system.string)  
    
    A [Cadeia de](/dotnet/api/system.string) caracteres que especifica o formato a ser usado. -ou- nulo para usar o formato padrão definido para o tipo da implementação [IFormattable.](/dotnet/api/system.iformattable)

<!-- end list -->

  - Formatprovider  
    Tipo: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    O [IFormatProvider a](/dotnet/api/system.iformatprovider) ser usado para formatar o valor. -ou- nulo para obter as informações de formato numérico da configuração de localidade atual do sistema operacional.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.String](/dotnet/api/system.string)  
Uma [Cadeia de](/dotnet/api/system.string) caracteres que contém o valor da instância atual no formato especificado.  

#### <a name="implements"></a>Implementações

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_DBID estrutura](./jet-dbid-structure.md)

[JET_DBID membros](./jet-dbid-members.md)

[Sobrecarga toString](./jet-dbid.tostring-method.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
