---
description: 'Saiba mais sobre: Enumeração CreateDatabaseGrbit'
title: Enumeração CreateDatabaseGrbit
TOCTitle: CreateDatabaseGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createdatabasegrbit(v=EXCHG.10)
ms:contentKeyID: 39515634
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.OverwriteExisting
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.RecoveryOff
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit.None
- Microsoft.Isam.Esent.Interop.CreateDatabaseGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8e23b7b875863b747fc5d2ba021c90d5f7f71048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010618"
---
# <a name="createdatabasegrbit-enumeration"></a><span data-ttu-id="a2b7c-103">Enumeração CreateDatabaseGrbit</span><span class="sxs-lookup"><span data-stu-id="a2b7c-103">CreateDatabaseGrbit enumeration</span></span>

<span data-ttu-id="a2b7c-104">Opções para [JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span><span class="sxs-lookup"><span data-stu-id="a2b7c-104">Options for [JetCreateDatabase(JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)](./api.jetcreatedatabase-method.md).</span></span>

<span data-ttu-id="a2b7c-105">Esta enumeração tem um atributo [FlagsAttribute](/dotnet/api/system.flagsattribute) que permite uma combinação bit a bit dos valores membros dela.</span><span class="sxs-lookup"><span data-stu-id="a2b7c-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="a2b7c-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a2b7c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a2b7c-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a2b7c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a2b7c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2b7c-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateDatabaseGrbit
'Usage
Dim instance As CreateDatabaseGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateDatabaseGrbit
```

## <a name="members"></a><span data-ttu-id="a2b7c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a2b7c-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="a2b7c-110">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="a2b7c-110">Member name</span></span></th>
<th><span data-ttu-id="a2b7c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2b7c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a2b7c-112">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a2b7c-112">None</span></span></td>
<td><span data-ttu-id="a2b7c-113">Opções padrão.</span><span class="sxs-lookup"><span data-stu-id="a2b7c-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="a2b7c-114">OverwriteExisting</span><span class="sxs-lookup"><span data-stu-id="a2b7c-114">OverwriteExisting</span></span></td>
<td><span data-ttu-id="a2b7c-115">Por padrão, se JetCreateDatabase for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído.</span><span class="sxs-lookup"><span data-stu-id="a2b7c-115">By default, if JetCreateDatabase is called and the database already exists, the Api call will fail and the original database will not be overwritten.</span></span> <span data-ttu-id="a2b7c-116">OverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo.</span><span class="sxs-lookup"><span data-stu-id="a2b7c-116">OverwriteExisting changes this behavior, and the old database will be overwritten with a new one.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="a2b7c-117">RecoveryOff</span><span class="sxs-lookup"><span data-stu-id="a2b7c-117">RecoveryOff</span></span></td>
<td><span data-ttu-id="a2b7c-118">Desliga o log.</span><span class="sxs-lookup"><span data-stu-id="a2b7c-118">Turns off logging.</span></span> <span data-ttu-id="a2b7c-119">A definição desse bit perde a capacidade de reproduzir arquivos de log e recuperar o banco de dados para um estado utilizável consistente após uma falha.</span><span class="sxs-lookup"><span data-stu-id="a2b7c-119">Setting this bit loses the ability to replay log files and recover the database to a consistent usable state after a crash.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="a2b7c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2b7c-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a2b7c-121">Referência</span><span class="sxs-lookup"><span data-stu-id="a2b7c-121">Reference</span></span>

[<span data-ttu-id="a2b7c-122">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a2b7c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
