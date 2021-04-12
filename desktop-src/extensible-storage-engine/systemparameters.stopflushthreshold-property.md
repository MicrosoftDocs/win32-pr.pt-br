---
description: 'Saiba mais sobre: Propriedade SystemParameters. StopFlushThreshold'
title: Propriedade SystemParameters. StopFlushThreshold
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297242"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="52d34-103">Propriedade SystemParameters. StopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="52d34-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="52d34-104">Obtém ou define o limite no qual o cache da página do banco de dados encerra a remoção de páginas do cache para liberar espaço para páginas que não são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="52d34-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="52d34-105">Quando o número de buffers de página no cache ultrapassar esse limite, o processo em segundo plano que foi iniciado para reabastecer o pool de buffers disponíveis será interrompido.</span><span class="sxs-lookup"><span data-stu-id="52d34-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="52d34-106">Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="52d34-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="52d34-107">Esse limite também deve ser maior que o limite de início definido por JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="52d34-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="52d34-108">A distância entre o limite inicial e o limite de interrupção afeta a eficiência com a qual as páginas de banco de dados são liberadas pelo processo em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="52d34-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="52d34-109">Um intervalo maior fará com que seja mais provável que as gravações nas páginas vizinhas possam ser combinadas.</span><span class="sxs-lookup"><span data-stu-id="52d34-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="52d34-110">No entanto, um limite de interrupção alto reduzirá o tamanho efetivo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="52d34-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="52d34-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="52d34-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="52d34-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="52d34-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="52d34-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52d34-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="52d34-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52d34-114">Property value</span></span>

<span data-ttu-id="52d34-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="52d34-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="52d34-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="52d34-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="52d34-117">Referência</span><span class="sxs-lookup"><span data-stu-id="52d34-117">Reference</span></span>

[<span data-ttu-id="52d34-118">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="52d34-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="52d34-119">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="52d34-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="52d34-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="52d34-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
