---
description: 'Saiba mais sobre: Propriedade Instanceparameters. EventSource'
title: Propriedade instanceparameters. EventSource
TOCTitle: 'EventSource property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsource(v=EXCHG.10)
ms:contentKeyID: 55103563
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSource
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSource
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5cba0c6f9aef4b9e6633a5d0073b1fdbc2c3b1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755381"
---
# <a name="instanceparameterseventsource-property"></a><span data-ttu-id="4d9bf-103">Propriedade instanceparameters. EventSource</span><span class="sxs-lookup"><span data-stu-id="4d9bf-103">InstanceParameters.EventSource property</span></span>

<span data-ttu-id="4d9bf-104">Obtém ou define uma cadeia de caracteres específica do aplicativo que será adicionada a qualquer mensagem de log de eventos emitida pelo mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-104">Gets or sets an application specific string that will be added to any event log messages that are emitted by the database engine.</span></span> <span data-ttu-id="4d9bf-105">Isso permite uma fácil correlação de mensagens de log de eventos com o aplicativo de origem.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-105">This allows easy correlation of event log messages with the source application.</span></span> <span data-ttu-id="4d9bf-106">Por padrão, o nome executável do aplicativo host será usado.</span><span class="sxs-lookup"><span data-stu-id="4d9bf-106">By default the host application executable name will be used.</span></span>

<span data-ttu-id="4d9bf-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4d9bf-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4d9bf-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4d9bf-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4d9bf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d9bf-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSource As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSource

instance.EventSource = value
```

``` csharp
public string EventSource { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4d9bf-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4d9bf-110">Property value</span></span>

<span data-ttu-id="4d9bf-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4d9bf-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4d9bf-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d9bf-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4d9bf-113">Referência</span><span class="sxs-lookup"><span data-stu-id="4d9bf-113">Reference</span></span>

[<span data-ttu-id="4d9bf-114">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="4d9bf-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="4d9bf-115">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="4d9bf-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="4d9bf-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4d9bf-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
