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
# <a name="vistagrbitsindexcrossproduct-field"></a><span data-ttu-id="0eb5b-103">Campo VistaGrbits. IndexCrossProduct</span><span class="sxs-lookup"><span data-stu-id="0eb5b-103">VistaGrbits.IndexCrossProduct field</span></span>

<span data-ttu-id="0eb5b-104">A especificação desse sinalizador para um índice que tenha mais de uma coluna de chave que seja uma coluna com vários valores resultará na criação de uma entrada de índice para cada resultado de um produto cruzado de todos os valores nessas colunas de chave.</span><span class="sxs-lookup"><span data-stu-id="0eb5b-104">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="0eb5b-105">Caso contrário, o índice teria apenas uma entrada para cada valor múltiplo na coluna de chave mais significativa, que é uma coluna com vários valores, e cada uma dessas entradas de índice usaria o primeiro valor múltiplo de outras colunas de chave que são colunas com valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="0eb5b-105">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="0eb5b-106">Por exemplo, se você tiver especificado esse sinalizador para um índice na coluna A que tem os valores "vermelho" e "azul" e na coluna B que tem os valores "1" e "2", as seguintes entradas de índice serão criadas: "vermelho", "1"; "vermelho", "2"; "azul", "1"; "Blue", "2".</span><span class="sxs-lookup"><span data-stu-id="0eb5b-106">For example, if you specified this flag for an index over column A that has the values "red" and "blue" and over column B that has the values "1" and "2" then the following index entries would be created: "red", "1"; "red", "2"; "blue", "1"; "blue", "2".</span></span> <span data-ttu-id="0eb5b-107">Caso contrário, as seguintes entradas de índice seriam criadas: "vermelho", "1"; "Blue", "1".</span><span class="sxs-lookup"><span data-stu-id="0eb5b-107">Otherwise, the following index entries would be created: "red", "1"; "blue", "1".</span></span>

<span data-ttu-id="0eb5b-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0eb5b-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="0eb5b-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0eb5b-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb5b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0eb5b-110">Syntax</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0eb5b-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="0eb5b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0eb5b-112">Referência</span><span class="sxs-lookup"><span data-stu-id="0eb5b-112">Reference</span></span>

[<span data-ttu-id="0eb5b-113">Classe VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="0eb5b-113">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="0eb5b-114">Membros do VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="0eb5b-114">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="0eb5b-115">Namespace Microsoft. ISAM. ESENT. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="0eb5b-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
