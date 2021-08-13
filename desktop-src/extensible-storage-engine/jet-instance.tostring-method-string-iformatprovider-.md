---
description: 'Saiba mais sobre: JET_INSTANCE. Método ToString (String, IFormatProvider)'
title: JET_INSTANCE. Método ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.tostring(v=EXCHG.10)
ms:contentKeyID: 39511283
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c45c24f4b8b6f40042031b96b7895b347ce0250744ec8fde8bf72626785128fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765577"
---
# <a name="jet_instancetostring-method-string-iformatprovider"></a>JET_INSTANCE. Método ToString (String, IFormatProvider)

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
Dim instance As JET_INSTANCE
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
    
    A [Cadeia de](/dotnet/api/system.string) Caracteres que especifica o formato a ser usado; ou nulo para usar o formato padrão definido para o tipo da implementação [IFormattable.](/dotnet/api/system.iformattable)

<!-- end list -->

  - Formatprovider  
    Tipo: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    O [IFormatProvider a](/dotnet/api/system.iformatprovider) ser usado para formatar o valor; ou nulo para obter as informações de formato numérico da configuração de localidade atual do sistema operacional.

#### <a name="return-value"></a>Valor retornado

Tipo: [System.String](/dotnet/api/system.string)  
Uma [Cadeia de](/dotnet/api/system.string) caracteres que contém o valor da instância atual no formato especificado.  

#### <a name="implements"></a>Implementações

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[JET_INSTANCE estrutura](./jet-instance-structure.md)

[JET_INSTANCE membros](./jet-instance-members.md)

[Sobrecarga toString](./jet-instance.tostring-method2.md)

[Namespace Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
