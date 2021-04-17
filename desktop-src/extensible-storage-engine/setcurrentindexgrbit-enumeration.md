---
description: 'Saiba mais sobre: Enumeração SetCurrentIndexGrbit'
title: Enumeração SetCurrentIndexGrbit
TOCTitle: SetCurrentIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcurrentindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39515072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.None
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.NoMove
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit.MoveFirst
- Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2391715332989bf20aae3d0a666c1cef2ce2e135
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798052"
---
# <a name="setcurrentindexgrbit-enumeration"></a><span data-ttu-id="fa3ea-103">Enumeração SetCurrentIndexGrbit</span><span class="sxs-lookup"><span data-stu-id="fa3ea-103">SetCurrentIndexGrbit enumeration</span></span>

<span data-ttu-id="fa3ea-104">Opções para [JetSetCurrentIndex2 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) e [JetSetCurrentIndex3 (JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span><span class="sxs-lookup"><span data-stu-id="fa3ea-104">Options for [JetSetCurrentIndex2(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit)](./api.jetsetcurrentindex2-method.md) and [JetSetCurrentIndex3(JET_SESID, JET_TABLEID, String, SetCurrentIndexGrbit, Int32)](./api.jetsetcurrentindex3-method.md).</span></span>

<span data-ttu-id="fa3ea-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="fa3ea-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa3ea-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fa3ea-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fa3ea-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3ea-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa3ea-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetCurrentIndexGrbit
'Usage
Dim instance As SetCurrentIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum SetCurrentIndexGrbit
```

## <a name="members"></a><span data-ttu-id="fa3ea-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fa3ea-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="fa3ea-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="fa3ea-110">Member name</span></span></th>
<th><span data-ttu-id="fa3ea-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa3ea-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fa3ea-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fa3ea-112">None</span></span></td>
<td><span data-ttu-id="fa3ea-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-113">Default options.</span></span> <span data-ttu-id="fa3ea-114">Isso é o mesmo que o MoveFirst.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-114">This is the same as MoveFirst.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="fa3ea-115">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="fa3ea-115">MoveFirst</span></span></td>
<td><span data-ttu-id="fa3ea-116">Indica que o cursor deve ser posicionado na primeira entrada do índice especificado.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-116">Indicates that the cursor should be positioned on the first entry of the specified index.</span></span> <span data-ttu-id="fa3ea-117">Se o índice atual estiver sendo selecionado, essa opção será ignorada.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-117">If the current index is being selected then this option is ignored.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="fa3ea-118">Nomover</span><span class="sxs-lookup"><span data-stu-id="fa3ea-118">NoMove</span></span></td>
<td><span data-ttu-id="fa3ea-119">Indica que o cursor deve ser posicionado na entrada de índice do novo índice que corresponde ao registro associado à entrada de índice na posição atual do cursor no índice antigo.</span><span class="sxs-lookup"><span data-stu-id="fa3ea-119">Indicates that the cursor should be positioned on the index entry of the new index that corresponds to the record associated with the index entry at the current position of the cursor on the old index.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="fa3ea-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa3ea-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa3ea-121">Referência</span><span class="sxs-lookup"><span data-stu-id="fa3ea-121">Reference</span></span>

[<span data-ttu-id="fa3ea-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fa3ea-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
