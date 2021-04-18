---
description: 'Saiba mais sobre: método API. JetDefragment2'
title: Método API. JetDefragment2
TOCTitle: 'JetDefragment2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.JET_CALLBACK,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment2(v=EXCHG.10)
ms:contentKeyID: 55100696
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b22c89b304103954a2088bf05ba98797777489be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793865"
---
# <a name="apijetdefragment2-method"></a><span data-ttu-id="a555c-103">Método API. JetDefragment2</span><span class="sxs-lookup"><span data-stu-id="a555c-103">Api.JetDefragment2 method</span></span>

<span data-ttu-id="a555c-104">Inicia e interrompe as tarefas de desfragmentação do banco de dados que aprimoram a organização em um banco de dado.</span><span class="sxs-lookup"><span data-stu-id="a555c-104">Starts and stops database defragmentation tasks that improves data organization within a database.</span></span>

<span data-ttu-id="a555c-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a555c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a555c-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a555c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a555c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a555c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetDefragment2 ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    callback As JET_CALLBACK, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim callback As JET_CALLBACK
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment2(sesid, _
    dbid, tableName, passes, seconds, _
    callback, grbit)
```

``` csharp
public static JET_wrn JetDefragment2(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    JET_CALLBACK callback,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a555c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a555c-108">Parameters</span></span>

  - <span data-ttu-id="a555c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="a555c-109">sesid</span></span>  
    <span data-ttu-id="a555c-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a555c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a555c-111">A sessão a ser usada para a chamada.</span><span class="sxs-lookup"><span data-stu-id="a555c-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="a555c-112">dbid</span><span class="sxs-lookup"><span data-stu-id="a555c-112">dbid</span></span>  
    <span data-ttu-id="a555c-113">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a555c-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a555c-114">O banco de dados a ser desfragmentado.</span><span class="sxs-lookup"><span data-stu-id="a555c-114">The database to be defragmented.</span></span>

<!-- end list -->

  - <span data-ttu-id="a555c-115">tableName</span><span class="sxs-lookup"><span data-stu-id="a555c-115">tableName</span></span>  
    <span data-ttu-id="a555c-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="a555c-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="a555c-117">Parâmetro não utilizado.</span><span class="sxs-lookup"><span data-stu-id="a555c-117">Unused parameter.</span></span> <span data-ttu-id="a555c-118">A desfragmentação é executada para todo o banco de dados descrito pela ID de banco de dados fornecida.</span><span class="sxs-lookup"><span data-stu-id="a555c-118">Defragmentation is performed for the entire database described by the given database ID.</span></span>

<!-- end list -->

  - <span data-ttu-id="a555c-119">passa</span><span class="sxs-lookup"><span data-stu-id="a555c-119">passes</span></span>  
    <span data-ttu-id="a555c-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a555c-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a555c-121">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro define o número máximo de passagens de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="a555c-121">When starting an online defragmentation task, this parameter sets the maximum number of defragmentation passes.</span></span> <span data-ttu-id="a555c-122">Ao parar uma tarefa de desfragmentação online, esse parâmetro é definido como o número de passagens executadas.</span><span class="sxs-lookup"><span data-stu-id="a555c-122">When stopping an online defragmentation task, this parameter is set to the number of passes performed.</span></span>

<!-- end list -->

  - <span data-ttu-id="a555c-123">segundos</span><span class="sxs-lookup"><span data-stu-id="a555c-123">seconds</span></span>  
    <span data-ttu-id="a555c-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a555c-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a555c-125">Ao iniciar uma tarefa de desfragmentação online, esse parâmetro define o tempo máximo para a desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="a555c-125">When starting an online defragmentation task, this parameter sets the maximum time for defragmentation.</span></span> <span data-ttu-id="a555c-126">Ao parar uma tarefa de desfragmentação online, esse buffer de saída é definido com o período de tempo usado para desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="a555c-126">When stopping an online defragmentation task, this output buffer is set to the length of time used for defragmentation.</span></span>

<!-- end list -->

  - <span data-ttu-id="a555c-127">retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="a555c-127">callback</span></span>  
    <span data-ttu-id="a555c-128">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="a555c-128">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="a555c-129">Função de retorno de chamada que a desfragmentação usa para relatar o progresso.</span><span class="sxs-lookup"><span data-stu-id="a555c-129">Callback function that defrag uses to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="a555c-130">grbit</span><span class="sxs-lookup"><span data-stu-id="a555c-130">grbit</span></span>  
    <span data-ttu-id="a555c-131">Tipo: [Microsoft. ISAM. ESENT. Interop. DefragGrbit](./defraggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a555c-131">Type: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a555c-132">Opções de desfragmentação.</span><span class="sxs-lookup"><span data-stu-id="a555c-132">Defragmentation options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a555c-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a555c-133">Return value</span></span>

<span data-ttu-id="a555c-134">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a555c-134">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="a555c-135">Um código de aviso.</span><span class="sxs-lookup"><span data-stu-id="a555c-135">A warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="a555c-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="a555c-136">Remarks</span></span>

<span data-ttu-id="a555c-137">O retorno de chamada passado para JetDefragment2 pode ser executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a555c-137">The callback passed to JetDefragment2 can be executed asynchronously.</span></span> <span data-ttu-id="a555c-138">O GC não sabe que o código não gerenciado tem uma referência ao retorno de chamada, portanto, é importante garantir que o retorno de chamada não seja coletado.</span><span class="sxs-lookup"><span data-stu-id="a555c-138">The GC doesn't know that the unmanaged code has a reference to the callback so it is important to make sure the callback isn't collected.</span></span>

## <a name="see-also"></a><span data-ttu-id="a555c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="a555c-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a555c-140">Referência</span><span class="sxs-lookup"><span data-stu-id="a555c-140">Reference</span></span>

[<span data-ttu-id="a555c-141">Classe de API</span><span class="sxs-lookup"><span data-stu-id="a555c-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a555c-142">Membros da API</span><span class="sxs-lookup"><span data-stu-id="a555c-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a555c-143">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a555c-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
