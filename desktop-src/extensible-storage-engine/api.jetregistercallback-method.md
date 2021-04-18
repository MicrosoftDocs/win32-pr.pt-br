---
description: 'Saiba mais sobre: método API. JetRegisterCallback'
title: Método API. JetRegisterCallback
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763313"
---
# <a name="apijetregistercallback-method"></a><span data-ttu-id="45782-103">Método API. JetRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="45782-103">Api.JetRegisterCallback method</span></span>

<span data-ttu-id="45782-104">Permite que o aplicativo configure o mecanismo de banco de dados para emitir notificações para o aplicativo para eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="45782-104">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="45782-105">Essas notificações são associadas a uma tabela específica e permanecem em vigor somente até que a instância que contém a tabela seja desligada usando [JetTerm (JET_INSTANCE)](./api.jetterm-method.md).</span><span class="sxs-lookup"><span data-stu-id="45782-105">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm(JET_INSTANCE)](./api.jetterm-method.md).</span></span>

<span data-ttu-id="45782-106">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="45782-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="45782-107">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="45782-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="45782-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45782-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="45782-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45782-109">Parameters</span></span>

  - <span data-ttu-id="45782-110">sesid</span><span class="sxs-lookup"><span data-stu-id="45782-110">sesid</span></span>  
    <span data-ttu-id="45782-111">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45782-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="45782-112">A sessão a ser usada.</span><span class="sxs-lookup"><span data-stu-id="45782-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="45782-113">TableID</span><span class="sxs-lookup"><span data-stu-id="45782-113">tableid</span></span>  
    <span data-ttu-id="45782-114">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45782-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="45782-115">Um cursor aberto na tabela em que o retorno de chamada deve ser registrado.</span><span class="sxs-lookup"><span data-stu-id="45782-115">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="45782-116">cbtyp</span><span class="sxs-lookup"><span data-stu-id="45782-116">cbtyp</span></span>  
    <span data-ttu-id="45782-117">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="45782-117">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="45782-118">Os motivos de retorno de chamada para os quais o aplicativo deseja receber notificações.</span><span class="sxs-lookup"><span data-stu-id="45782-118">The callback reasons for which the application wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="45782-119">retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="45782-119">callback</span></span>  
    <span data-ttu-id="45782-120">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="45782-120">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="45782-121">A função do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="45782-121">The callback function.</span></span>

<!-- end list -->

  - <span data-ttu-id="45782-122">contexto</span><span class="sxs-lookup"><span data-stu-id="45782-122">context</span></span>  
    <span data-ttu-id="45782-123">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="45782-123">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="45782-124">Um contexto que será dado ao retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="45782-124">A context that will be given to the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="45782-125">retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="45782-125">callbackId</span></span>  
    <span data-ttu-id="45782-126">Tipo: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="45782-126">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="45782-127">Um identificador que pode ser usado posteriormente para cancelar o registro da função de retorno de chamada fornecida usando [JetUnregisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp JET_HANDLE)](./api.jetunregistercallback-method.md).</span><span class="sxs-lookup"><span data-stu-id="45782-127">A handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="45782-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="45782-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="45782-129">Referência</span><span class="sxs-lookup"><span data-stu-id="45782-129">Reference</span></span>

[<span data-ttu-id="45782-130">Classe de API</span><span class="sxs-lookup"><span data-stu-id="45782-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="45782-131">Membros da API</span><span class="sxs-lookup"><span data-stu-id="45782-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="45782-132">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="45782-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
