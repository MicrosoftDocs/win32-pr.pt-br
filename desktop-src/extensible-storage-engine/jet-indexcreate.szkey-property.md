---
description: 'Saiba mais sobre a propriedade: JET_INDEXCREATE. szKey'
title: Propriedade JET_INDEXCREATE. szKey
TOCTitle: 'szKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.szkey(v=EXCHG.10)
ms:contentKeyID: 55103656
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_szKey
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.szKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86ade65ee28eef6314d31653772b0c22657476d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297409"
---
# <a name="jet_indexcreateszkey-property"></a><span data-ttu-id="f59ab-103">Propriedade JET_INDEXCREATE. szKey</span><span class="sxs-lookup"><span data-stu-id="f59ab-103">JET_INDEXCREATE.szKey property</span></span>

<span data-ttu-id="f59ab-104">Obtém ou define a descrição da chave de índice.</span><span class="sxs-lookup"><span data-stu-id="f59ab-104">Gets or sets the description of the index key.</span></span> <span data-ttu-id="f59ab-105">Essa é uma cadeia de caracteres dupla com terminação nula de tokens delimitados por nulo.</span><span class="sxs-lookup"><span data-stu-id="f59ab-105">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="f59ab-106">Cada token tem o formato de \[ nome de coluna-especificador de direção \] \[ \] , em que a especificação de direção é "+" ou "-".</span><span class="sxs-lookup"><span data-stu-id="f59ab-106">Each token is of the form \[direction-specifier\]\[column-name\], where direction-specification is either "+" or "-".</span></span> <span data-ttu-id="f59ab-107">por exemplo, um szKey de "+ ABC \\ 0-Def \\ 0 + GHI \\ 0" irá indexar as três colunas "ABC" (em ordem crescente), "def" (em ordem decrescente) e "GHI" (em ordem crescente).</span><span class="sxs-lookup"><span data-stu-id="f59ab-107">for example, a szKey of "+abc\\0-def\\0+ghi\\0" will index over the three columns "abc" (in ascending order), "def" (in descending order), and "ghi" (in ascending order).</span></span>

<span data-ttu-id="f59ab-108">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f59ab-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f59ab-109">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f59ab-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f59ab-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="f59ab-110">Syntax</span></span>

``` vb
'Declaration
Public Property szKey As String
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As String

value = instance.szKey

instance.szKey = value
```

``` csharp
public string szKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f59ab-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f59ab-111">Property value</span></span>

<span data-ttu-id="f59ab-112">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="f59ab-112">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f59ab-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="f59ab-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f59ab-114">Referência</span><span class="sxs-lookup"><span data-stu-id="f59ab-114">Reference</span></span>

[<span data-ttu-id="f59ab-115">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="f59ab-115">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="f59ab-116">Membros do JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="f59ab-116">JET_INDEXCREATE members</span></span>](./jet-indexcreate-members.md)

[<span data-ttu-id="f59ab-117">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f59ab-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
