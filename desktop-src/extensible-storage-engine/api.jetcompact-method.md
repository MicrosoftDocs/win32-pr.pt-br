---
description: 'Saiba mais sobre: método API. JetCompact'
title: Método API. JetCompact
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920791"
---
# <a name="apijetcompact-method"></a><span data-ttu-id="b7fc1-103">Método API. JetCompact</span><span class="sxs-lookup"><span data-stu-id="b7fc1-103">Api.JetCompact method</span></span>

<span data-ttu-id="b7fc1-104">Faz uma cópia de um banco de dados existente.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-104">Makes a copy of an existing database.</span></span> <span data-ttu-id="b7fc1-105">A cópia é compactada para um estado ideal para uso.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-105">The copy is compacted to a state optimal for usage.</span></span> <span data-ttu-id="b7fc1-106">Os dados nos dados copiados serão empacotados de acordo com as medidas escolhidas para os índices na criação do índice.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-106">Data in the copied data will be packed according to the measures chosen for the indexes at index create.</span></span> <span data-ttu-id="b7fc1-107">Dessa forma, os dados compactados podem ser armazenados da maneira mais densa possível.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-107">In this way, compacted data may be stored as densely as possible.</span></span> <span data-ttu-id="b7fc1-108">Como alternativa, os dados compactados podem reservar espaço para o aumento de registro subsequente ou inserções de índice.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-108">Alternatively, compacted data may reserve space for subsequent record growth or index insertions.</span></span>

<span data-ttu-id="b7fc1-109">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b7fc1-110">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b7fc1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7fc1-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="b7fc1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7fc1-112">Parameters</span></span>

  - <span data-ttu-id="b7fc1-113">sesid</span><span class="sxs-lookup"><span data-stu-id="b7fc1-113">sesid</span></span>  
    <span data-ttu-id="b7fc1-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b7fc1-115">A sessão a ser usada para a chamada.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-115">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7fc1-116">sourceDatabase</span><span class="sxs-lookup"><span data-stu-id="b7fc1-116">sourceDatabase</span></span>  
    <span data-ttu-id="b7fc1-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b7fc1-118">O banco de dados de origem que será compactado.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-118">The source database that will be compacted.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7fc1-119">destinationDatabase</span><span class="sxs-lookup"><span data-stu-id="b7fc1-119">destinationDatabase</span></span>  
    <span data-ttu-id="b7fc1-120">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-120">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="b7fc1-121">O nome a ser usado para o banco de dados compactado.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-121">The name to use for the compacted database.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7fc1-122">statusCallback</span><span class="sxs-lookup"><span data-stu-id="b7fc1-122">statusCallback</span></span>  
    <span data-ttu-id="b7fc1-123">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-123">Type: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)</span></span>  
    
    <span data-ttu-id="b7fc1-124">Uma função de retorno de chamada que pode ser chamada periodicamente por meio da operação Compact do banco de dados para relatar o progresso.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-124">A callback function that can be called periodically through the database compact operation to report progress.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7fc1-125">ignorado</span><span class="sxs-lookup"><span data-stu-id="b7fc1-125">ignored</span></span>  
    <span data-ttu-id="b7fc1-126">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CONVERT](./jet-convert-class.md)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-126">Type: [Microsoft.Isam.Esent.Interop.JET_CONVERT](./jet-convert-class.md)</span></span>  
    
    <span data-ttu-id="b7fc1-127">Esse parâmetro é ignorado e deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-127">This parameter is ignored and should be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="b7fc1-128">grbit</span><span class="sxs-lookup"><span data-stu-id="b7fc1-128">grbit</span></span>  
    <span data-ttu-id="b7fc1-129">Tipo: [Microsoft. ISAM. ESENT. Interop. CompactGrbit](./compactgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b7fc1-129">Type: [Microsoft.Isam.Esent.Interop.CompactGrbit](./compactgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b7fc1-130">Opções de compactação.</span><span class="sxs-lookup"><span data-stu-id="b7fc1-130">Compact options.</span></span>

## <a name="see-also"></a><span data-ttu-id="b7fc1-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7fc1-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b7fc1-132">Referência</span><span class="sxs-lookup"><span data-stu-id="b7fc1-132">Reference</span></span>

[<span data-ttu-id="b7fc1-133">Classe de API</span><span class="sxs-lookup"><span data-stu-id="b7fc1-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b7fc1-134">Membros da API</span><span class="sxs-lookup"><span data-stu-id="b7fc1-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b7fc1-135">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b7fc1-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
