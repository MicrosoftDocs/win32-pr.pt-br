---
description: 'Saiba mais sobre: método API. JetDefragment'
title: Método API. JetDefragment
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785231"
---
# <a name="apijetdefragment-method"></a><span data-ttu-id="b8e18-103">Método API. JetDefragment</span><span class="sxs-lookup"><span data-stu-id="b8e18-103">Api.JetDefragment method</span></span>

<span data-ttu-id="b8e18-104">Inicia e interrompe as tarefas de desfragmentação do banco de dados que aprimoram a organização em um banco de dado.</span><span class="sxs-lookup"><span data-stu-id="b8e18-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="b8e18-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8e18-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8e18-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8e18-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e18-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8e18-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b8e18-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8e18-108">Parameters</span></span>

  - <span data-ttu-id="b8e18-109">sesid</span><span class="sxs-lookup"><span data-stu-id="b8e18-109">sesid</span></span>  
    <span data-ttu-id="b8e18-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8e18-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b8e18-111">A sessão a ser usada para a chamada.</span><span class="sxs-lookup"><span data-stu-id="b8e18-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e18-112">dbid</span><span class="sxs-lookup"><span data-stu-id="b8e18-112">dbid</span></span>  
    <span data-ttu-id="b8e18-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b8e18-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="b8e18-114">O banco de dados a ser desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="b8e18-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e18-115">tableName</span><span class="sxs-lookup"><span data-stu-id="b8e18-115">tableName</span></span>  
    <span data-ttu-id="b8e18-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b8e18-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b8e18-117">Parâmetro não utilizado.</span><span class="sxs-lookup"><span data-stu-id="b8e18-117">Unused parameter.</span></span> <span data-ttu-id="b8e18-118">A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.</span><span class="sxs-lookup"><span data-stu-id="b8e18-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e18-119">passa</span><span class="sxs-lookup"><span data-stu-id="b8e18-119">passes</span></span>  
    <span data-ttu-id="b8e18-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b8e18-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b8e18-121">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro define o número máximo de passagens de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="b8e18-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="b8e18-122">Ao parar uma tarefa de desfragmentação online, esse parâmetro é definido como o número de passagens executadas.</span><span class="sxs-lookup"><span data-stu-id="b8e18-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e18-123">segundos</span><span class="sxs-lookup"><span data-stu-id="b8e18-123">seconds</span></span>  
    <span data-ttu-id="b8e18-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b8e18-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b8e18-125">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro define o tempo máximo para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="b8e18-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="b8e18-126">Ao parar uma tarefa de desfragmentação online, esse buffer de saída é definido com o período de tempo usado para desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="b8e18-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="b8e18-127">grbit</span><span class="sxs-lookup"><span data-stu-id="b8e18-127">grbit</span></span>  
    <span data-ttu-id="b8e18-128">Tipo: [Microsoft. ISAM. ESENT. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b8e18-128">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b8e18-129">Opções de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="b8e18-129">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b8e18-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8e18-130">Return value</span></span>

<span data-ttu-id="b8e18-131">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b8e18-131">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="b8e18-132">Um código de aviso.</span><span class="sxs-lookup"><span data-stu-id="b8e18-132">A warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8e18-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8e18-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8e18-134">Referência</span><span class="sxs-lookup"><span data-stu-id="b8e18-134">Reference</span></span>

[<span data-ttu-id="b8e18-135">Classe de API</span><span class="sxs-lookup"><span data-stu-id="b8e18-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b8e18-136">Membros da API</span><span class="sxs-lookup"><span data-stu-id="b8e18-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b8e18-137">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b8e18-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
