---
description: 'Saiba mais sobre: JET_PFNSTATUS delegado'
title: JET_PFNSTATUS delegado
TOCTitle: JET_PFNSTATUS delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnstatus(v=EXCHG.10)
ms:contentKeyID: 39515654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS
- Microsoft.Isam.Esent.Interop.JET_PFNSTATUS.BeginInvoke
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16cc5807d858f964f995b449a0a0eee78659aefd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813531"
---
# <a name="jet_pfnstatus-delegate"></a><span data-ttu-id="b257f-103">JET_PFNSTATUS delegado</span><span class="sxs-lookup"><span data-stu-id="b257f-103">JET_PFNSTATUS delegate</span></span>

<span data-ttu-id="b257f-104">Recebe informações sobre o progresso de operações de execução longa, como operações de desfragmentação, backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="b257f-104">Receives information about the progress of long-running operations, such as defragmentation, backup, or restore operations.</span></span> <span data-ttu-id="b257f-105">Durante essas operações, o mecanismo de banco de dados chama essa função de retorno de chamada para fornecer uma atualização no andamento da operação.</span><span class="sxs-lookup"><span data-stu-id="b257f-105">During such operations, the database engine calls this callback function to give an update on the progress of the operation.</span></span>

<span data-ttu-id="b257f-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b257f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b257f-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b257f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b257f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b257f-108">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNSTATUS ( _
    sesid As JET_SESID, _
    snp As JET_SNP, _
    snt As JET_SNT, _
    data As Object _
) As JET_err
'Usage
Dim instance As New JET_PFNSTATUS(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNSTATUS(
    JET_SESID sesid,
    JET_SNP snp,
    JET_SNT snt,
    Object data
)
```

#### <a name="parameters"></a><span data-ttu-id="b257f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b257f-109">Parameters</span></span>

  - <span data-ttu-id="b257f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="b257f-110">sesid</span></span>  
    <span data-ttu-id="b257f-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b257f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b257f-112">A sessão com a qual a operação de longa execução foi chamada.</span><span class="sxs-lookup"><span data-stu-id="b257f-112">The session with which the long running operation was called.</span></span>

<!-- end list -->

  - <span data-ttu-id="b257f-113">padrões</span><span class="sxs-lookup"><span data-stu-id="b257f-113">snp</span></span>  
    <span data-ttu-id="b257f-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SNP](./jet-snp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b257f-114">Type: [Microsoft.Isam.Esent.Interop.JET_SNP](./jet-snp-enumeration.md)</span></span>  
    
    <span data-ttu-id="b257f-115">O tipo de operação.</span><span class="sxs-lookup"><span data-stu-id="b257f-115">The type of operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="b257f-116">snt</span><span class="sxs-lookup"><span data-stu-id="b257f-116">snt</span></span>  
    <span data-ttu-id="b257f-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SNT](./jet-snt-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b257f-117">Type: [Microsoft.Isam.Esent.Interop.JET_SNT](./jet-snt-enumeration.md)</span></span>  
    
    <span data-ttu-id="b257f-118">O status da operação.</span><span class="sxs-lookup"><span data-stu-id="b257f-118">The status of the operation.</span></span>

<!-- end list -->

  - <span data-ttu-id="b257f-119">data</span><span class="sxs-lookup"><span data-stu-id="b257f-119">data</span></span>  
    <span data-ttu-id="b257f-120">Tipo: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="b257f-120">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="b257f-121">Dados opcionais.</span><span class="sxs-lookup"><span data-stu-id="b257f-121">Optional data.</span></span> <span data-ttu-id="b257f-122">Pode ser um [JET_SNPROG](./jet-snprog-class.md).</span><span class="sxs-lookup"><span data-stu-id="b257f-122">May be a [JET_SNPROG](./jet-snprog-class.md).</span></span>

#### <a name="return-value"></a><span data-ttu-id="b257f-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b257f-123">Return value</span></span>

<span data-ttu-id="b257f-124">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b257f-124">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="b257f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b257f-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b257f-126">Referência</span><span class="sxs-lookup"><span data-stu-id="b257f-126">Reference</span></span>

[<span data-ttu-id="b257f-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b257f-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
