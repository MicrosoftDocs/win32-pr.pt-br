---
description: 'Saiba mais sobre: Propriedade SystemParameters. StartFlushThreshold'
title: Propriedade SystemParameters. StartFlushThreshold
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297243"
---
# <a name="systemparametersstartflushthreshold-property"></a><span data-ttu-id="c93c2-103">Propriedade SystemParameters. StartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="c93c2-103">SystemParameters.StartFlushThreshold property</span></span>

<span data-ttu-id="c93c2-104">Obtém ou define o limite no qual o cache da página do banco de dados começa a remover páginas do cache para liberar espaço para páginas que não estão armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="c93c2-104">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="c93c2-105">Quando o número de buffers de página no cache cair abaixo desse limite, um processo em segundo plano será iniciado para reabastecer o pool de buffers disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c93c2-105">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="c93c2-106">Esse limite é sempre relativo ao tamanho máximo do cache, conforme definido por JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="c93c2-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="c93c2-107">Esse limite também deve ser menor que o limite de parada definido por JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="c93c2-107">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="c93c2-108">A altura da distância do limite inicial determinará o tempo de resposta que o cache da página do banco de dados deve ter para produzir os buffers disponíveis antes que o aplicativo precise deles.</span><span class="sxs-lookup"><span data-stu-id="c93c2-108">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="c93c2-109">Um limite de início alto dará ao processo em segundo plano mais tempo para reagir.</span><span class="sxs-lookup"><span data-stu-id="c93c2-109">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="c93c2-110">No entanto, um limite de início alto implica um limite de parada maior e reduzirá o tamanho efetivo do cache de página do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c93c2-110">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="c93c2-111">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c93c2-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c93c2-112">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c93c2-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c93c2-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c93c2-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="c93c2-114">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c93c2-114">Property value</span></span>

<span data-ttu-id="c93c2-115">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="c93c2-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="c93c2-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="c93c2-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c93c2-117">Referência</span><span class="sxs-lookup"><span data-stu-id="c93c2-117">Reference</span></span>

[<span data-ttu-id="c93c2-118">Classe SystemParameters</span><span class="sxs-lookup"><span data-stu-id="c93c2-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="c93c2-119">Membros do SystemParameters</span><span class="sxs-lookup"><span data-stu-id="c93c2-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="c93c2-120">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c93c2-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
