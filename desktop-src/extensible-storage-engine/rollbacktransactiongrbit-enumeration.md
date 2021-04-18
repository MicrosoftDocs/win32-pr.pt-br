---
description: 'Saiba mais sobre: Enumeração RollbackTransactionGrbit'
title: Enumeração RollbackTransactionGrbit
TOCTitle: RollbackTransactionGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.rollbacktransactiongrbit(v=EXCHG.10)
ms:contentKeyID: 39513584
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.RollbackAll
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit.None
- Microsoft.Isam.Esent.Interop.RollbackTransactionGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bf2635d94070fc47bebbd6cdd0e53deddeb4c5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800060"
---
# <a name="rollbacktransactiongrbit-enumeration"></a><span data-ttu-id="c0d83-103">Enumeração RollbackTransactionGrbit</span><span class="sxs-lookup"><span data-stu-id="c0d83-103">RollbackTransactionGrbit enumeration</span></span>

<span data-ttu-id="c0d83-104">Opções para JetRollbackTransaction.</span><span class="sxs-lookup"><span data-stu-id="c0d83-104">Options for JetRollbackTransaction.</span></span>

<span data-ttu-id="c0d83-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="c0d83-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="c0d83-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c0d83-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c0d83-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c0d83-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d83-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0d83-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration RollbackTransactionGrbit
'Usage
Dim instance As RollbackTransactionGrbit
```

``` csharp
[FlagsAttribute]
public enum RollbackTransactionGrbit
```

## <a name="members"></a><span data-ttu-id="c0d83-109">Membros</span><span class="sxs-lookup"><span data-stu-id="c0d83-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="c0d83-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="c0d83-110">Member name</span></span></th>
<th><span data-ttu-id="c0d83-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0d83-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="c0d83-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c0d83-112">None</span></span></td>
<td><span data-ttu-id="c0d83-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="c0d83-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="c0d83-114">RollbackAll</span><span class="sxs-lookup"><span data-stu-id="c0d83-114">RollbackAll</span></span></td>
<td><span data-ttu-id="c0d83-115">Essa opção solicita que todas as alterações feitas no estado do banco de dados durante todos os pontos de salvamento sejam desfeitas.</span><span class="sxs-lookup"><span data-stu-id="c0d83-115">This option requests that all changes made to the state of the database during all save points be undone.</span></span> <span data-ttu-id="c0d83-116">Como resultado, a sessão sairá da transação.</span><span class="sxs-lookup"><span data-stu-id="c0d83-116">As a result, the session will exit the transaction.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="c0d83-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0d83-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c0d83-118">Referência</span><span class="sxs-lookup"><span data-stu-id="c0d83-118">Reference</span></span>

[<span data-ttu-id="c0d83-119">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c0d83-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
