---
description: 'Saiba mais sobre: enumeração de JET_SNT'
title: Enumeração de JET_SNT
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771414"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="40202-103">Enumeração de JET_SNT</span><span class="sxs-lookup"><span data-stu-id="40202-103">JET_SNT enumeration</span></span>

<span data-ttu-id="40202-104">Tipo de progresso que está sendo relatado.</span><span class="sxs-lookup"><span data-stu-id="40202-104">Type of progress being reported.</span></span>

<span data-ttu-id="40202-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40202-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40202-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40202-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40202-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40202-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="40202-108">Membros</span><span class="sxs-lookup"><span data-stu-id="40202-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="40202-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="40202-109">Member name</span></span></th>
<th><span data-ttu-id="40202-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="40202-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40202-111">Começar</span><span class="sxs-lookup"><span data-stu-id="40202-111">Begin</span></span></td>
<td><span data-ttu-id="40202-112">Retorno de chamada para o início de uma operação.</span><span class="sxs-lookup"><span data-stu-id="40202-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40202-113">Progresso</span><span class="sxs-lookup"><span data-stu-id="40202-113">Progress</span></span></td>
<td><span data-ttu-id="40202-114">Retorno de chamada para o andamento da operação.</span><span class="sxs-lookup"><span data-stu-id="40202-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40202-115">Concluir</span><span class="sxs-lookup"><span data-stu-id="40202-115">Complete</span></span></td>
<td><span data-ttu-id="40202-116">Retorno de chamada para a conclusão de uma operação.</span><span class="sxs-lookup"><span data-stu-id="40202-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40202-117">Falha</span><span class="sxs-lookup"><span data-stu-id="40202-117">Fail</span></span></td>
<td><span data-ttu-id="40202-118">Retorno de chamada para falha durante a operação.</span><span class="sxs-lookup"><span data-stu-id="40202-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40202-119">RecoveryStep</span><span class="sxs-lookup"><span data-stu-id="40202-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="40202-120">Retorno de chamada para o controle de recuperação.</span><span class="sxs-lookup"><span data-stu-id="40202-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="40202-121">Usado para processamento interno em versões do sistema operacional Windows anteriores ao Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40202-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="40202-122">Esse valor não é aplicável a versões do Windows a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40202-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="40202-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="40202-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40202-124">Referência</span><span class="sxs-lookup"><span data-stu-id="40202-124">Reference</span></span>

[<span data-ttu-id="40202-125">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="40202-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
