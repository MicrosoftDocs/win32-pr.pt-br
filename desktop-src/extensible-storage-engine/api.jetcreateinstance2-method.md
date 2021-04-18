---
description: 'Saiba mais sobre: método API. JetCreateInstance2'
title: Método API. JetCreateInstance2
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773042"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="7e10e-103">Método API. JetCreateInstance2</span><span class="sxs-lookup"><span data-stu-id="7e10e-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="7e10e-104">Aloque uma nova instância do mecanismo de banco de dados para uso em um único processo, com um nome de exibição especificado.</span><span class="sxs-lookup"><span data-stu-id="7e10e-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="7e10e-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e10e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e10e-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7e10e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e10e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e10e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7e10e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e10e-108">Parameters</span></span>

  - <span data-ttu-id="7e10e-109">instance</span><span class="sxs-lookup"><span data-stu-id="7e10e-109">instance</span></span>  
    <span data-ttu-id="7e10e-110">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7e10e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7e10e-111">Retorna a instância recém-criada.</span><span class="sxs-lookup"><span data-stu-id="7e10e-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e10e-112">name</span><span class="sxs-lookup"><span data-stu-id="7e10e-112">name</span></span>  
    <span data-ttu-id="7e10e-113">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7e10e-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7e10e-114">Especifica um identificador de cadeia de caracteres exclusivo para a instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="7e10e-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="7e10e-115">Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="7e10e-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e10e-116">displayName</span><span class="sxs-lookup"><span data-stu-id="7e10e-116">displayName</span></span>  
    <span data-ttu-id="7e10e-117">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7e10e-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7e10e-118">Um nome de exibição para a instância a ser criada.</span><span class="sxs-lookup"><span data-stu-id="7e10e-118">A display name for the instance to be created.</span></span> <span data-ttu-id="7e10e-119">Isso será usado em entradas do EventLog.</span><span class="sxs-lookup"><span data-stu-id="7e10e-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="7e10e-120">grbit</span><span class="sxs-lookup"><span data-stu-id="7e10e-120">grbit</span></span>  
    <span data-ttu-id="7e10e-121">Tipo: [Microsoft. ISAM. ESENT. Interop. CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7e10e-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7e10e-122">Opções de criação.</span><span class="sxs-lookup"><span data-stu-id="7e10e-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e10e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e10e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e10e-124">Referência</span><span class="sxs-lookup"><span data-stu-id="7e10e-124">Reference</span></span>

[<span data-ttu-id="7e10e-125">Classe de API</span><span class="sxs-lookup"><span data-stu-id="7e10e-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7e10e-126">Membros da API</span><span class="sxs-lookup"><span data-stu-id="7e10e-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7e10e-127">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7e10e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
