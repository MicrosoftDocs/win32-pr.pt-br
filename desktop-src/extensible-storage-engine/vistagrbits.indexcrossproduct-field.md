---
description: 'Saiba mais sobre: campo VistaGrbits. IndexCrossProduct'
title: Campo VistaGrbits. IndexCrossProduct (Microsoft. ISAM. ESENT. Interop. vista)
TOCTitle: IndexCrossProduct field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexcrossproduct(v=EXCHG.10)
ms:contentKeyID: 55104426
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexCrossProduct
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1b16f741c63d455d18a887331505080aef62990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922934"
---
# <a name="vistagrbitsindexcrossproduct-field"></a>Campo VistaGrbits. IndexCrossProduct

A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna com vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave. Caso contrário, o índice teria apenas uma entrada para cada valor múltiplo na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usaria o primeiro valor múltiplo de outras colunas de chave que são colunas com valores múltiplos. Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores "vermelho" e "azul" e na coluna B que tem os valores "1" e "2", as seguintes entradas de índice serão criadas: "vermelho", "1"; "vermelho", "2"; "azul", "1"; "Blue", "2". Caso contrário, as seguintes entradas de índice seriam criadas: "vermelho", "1"; "Blue", "1".

**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintaxe

``` vb
'Declaration
Public Const IndexCrossProduct As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexCrossProduct
```

``` csharp
public const CreateIndexGrbit IndexCrossProduct
```

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe VistaGrbits](./vistagrbits-class.md)

[Membros do VistaGrbits](./vistagrbits-members.md)

[Namespace Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
