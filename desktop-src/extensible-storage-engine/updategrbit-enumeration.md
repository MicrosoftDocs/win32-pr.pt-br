---
description: 'Saiba mais sobre: Enumeração UpdateGrbit'
title: Enumeração UpdateGrbit (Microsoft. ISAM. ESENT. Interop. Server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e27809ef16fb00fd538e4c37826d10fefa3b396c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501902"
---
# <a name="updategrbit-enumeration"></a><span data-ttu-id="878bc-103">Enumeração UpdateGrbit</span><span class="sxs-lookup"><span data-stu-id="878bc-103">UpdateGrbit enumeration</span></span>

<span data-ttu-id="878bc-104">Opções para [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span><span class="sxs-lookup"><span data-stu-id="878bc-104">Options for [JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit)](./server2003api.jetupdate2-method.md).</span></span>

<span data-ttu-id="878bc-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="878bc-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="878bc-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="878bc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="878bc-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="878bc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="878bc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="878bc-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
```

## <a name="members"></a><span data-ttu-id="878bc-109">Membros</span><span class="sxs-lookup"><span data-stu-id="878bc-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="878bc-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="878bc-110">Member name</span></span></th>
<th><span data-ttu-id="878bc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="878bc-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="878bc-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="878bc-112">None</span></span></td>
<td><span data-ttu-id="878bc-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="878bc-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="878bc-114">CheckESE97Compatibility</span><span class="sxs-lookup"><span data-stu-id="878bc-114">CheckESE97Compatibility</span></span></td>
<td><span data-ttu-id="878bc-115"><strong>Obsoleto.</strong></span><span class="sxs-lookup"><span data-stu-id="878bc-115"><strong>Obsolete.</strong></span></span> <span data-ttu-id="878bc-116">Esse sinalizador faz com que a atualização retorne um erro se a atualização não fosse possível na versão 2000 do Windows do ESE, que impõe um número menor máximo de instâncias de coluna com vários valores em cada registro do que as versões posteriores do ESE.</span><span class="sxs-lookup"><span data-stu-id="878bc-116">This flag causes the update to return an error if the update would not have been possible in the Windows 2000 version of ESE, which enforced a smaller maximum number of multi-valued column instances in each record than later versions of ESE.</span></span> <span data-ttu-id="878bc-117">Isso é importante apenas para aplicativos que desejam replicar dados entre aplicativos hospedados no Windows 2000 e aplicativos hospedados no Windows 2003 ou versões posteriores do ESE.</span><span class="sxs-lookup"><span data-stu-id="878bc-117">This is important only for applications that wish to replicate data between applications hosted on Windows 2000 and applications hosted on Windows 2003, or later versions of ESE.</span></span> <span data-ttu-id="878bc-118">Não deve ser necessário para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="878bc-118">It should not be necessary for most applications.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="878bc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="878bc-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="878bc-120">Referência</span><span class="sxs-lookup"><span data-stu-id="878bc-120">Reference</span></span>

[<span data-ttu-id="878bc-121">Namespace Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="878bc-121">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
