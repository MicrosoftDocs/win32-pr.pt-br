---
description: 'Saiba mais sobre a propriedade: Instanceparameters. EventSourceKey'
title: Propriedade instanceparameters. EventSourceKey
TOCTitle: 'EventSourceKey property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.eventsourcekey(v=EXCHG.10)
ms:contentKeyID: 55107449
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.EventSourceKey
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EventSourceKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d1dc80943095611737d0c9704bcc0e82ffee506f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921224"
---
# <a name="instanceparameterseventsourcekey-property"></a><span data-ttu-id="89aa4-103">Propriedade instanceparameters. EventSourceKey</span><span class="sxs-lookup"><span data-stu-id="89aa4-103">InstanceParameters.EventSourceKey property</span></span>

<span data-ttu-id="89aa4-104">Obtém ou define o nome do log de eventos que o mecanismo de banco de dados usa para suas mensagens de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="89aa4-104">Gets or sets the name of the event log the database engine uses for its event log messages.</span></span> <span data-ttu-id="89aa4-105">Por padrão, todas as mensagens de log de eventos vão para o log de eventos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="89aa4-105">By default, all event log messages will go to the Application event log.</span></span> <span data-ttu-id="89aa4-106">Se o nome da chave do registro para outro log de eventos estiver configurado, as mensagens do log de eventos entrarão em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="89aa4-106">If the registry key name for another event log is configured then the event log messages will go there instead.</span></span>

<span data-ttu-id="89aa4-107">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89aa4-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89aa4-108">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89aa4-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89aa4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="89aa4-109">Syntax</span></span>

``` vb
'Declaration
Public Property EventSourceKey As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.EventSourceKey

instance.EventSourceKey = value
```

``` csharp
public string EventSourceKey { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="89aa4-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="89aa4-110">Property value</span></span>

<span data-ttu-id="89aa4-111">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="89aa4-111">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="89aa4-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="89aa4-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89aa4-113">Referência</span><span class="sxs-lookup"><span data-stu-id="89aa4-113">Reference</span></span>

[<span data-ttu-id="89aa4-114">Classe instanceparameters</span><span class="sxs-lookup"><span data-stu-id="89aa4-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="89aa4-115">Membros de instanceparameters</span><span class="sxs-lookup"><span data-stu-id="89aa4-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="89aa4-116">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="89aa4-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
