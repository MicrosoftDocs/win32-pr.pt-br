---
description: A camada de dados geralmente contém informações mais estáticas&\# 8212; informações mantidas na mídia durável.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Otimizar chamadas entre os dados e a lógica de negócios do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765659"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a><span data-ttu-id="bd820-103">Otimização de interações entre a camada de lógica de negócios COM+ e a camada de dados</span><span class="sxs-lookup"><span data-stu-id="bd820-103">Optimizing Interactions Between the COM+ Business Logic Tier and the Data Tier</span></span>

<span data-ttu-id="bd820-104">A camada de dados geralmente contém principalmente informações estáticas – informações mantidas em mídia durável.</span><span class="sxs-lookup"><span data-stu-id="bd820-104">The data tier often contains mostly static information—information persisted on durable media.</span></span> <span data-ttu-id="bd820-105">Como essa camada abrange informações que são principalmente estáticas, ela requer uma análise completa para possíveis afunilamentos.</span><span class="sxs-lookup"><span data-stu-id="bd820-105">Because this tier encompasses information that is mostly static, it requires a thorough analysis for potential bottlenecks.</span></span> <span data-ttu-id="bd820-106">Além da possibilidade óbvia de gargalos de conexão, os pontos de acesso podem ser causados por registros acessados com frequência, métodos ineficientes para acessar dados e a necessidade de coordenar o acesso a sistemas herdados.</span><span class="sxs-lookup"><span data-stu-id="bd820-106">In addition to the obvious possibility for connection bottlenecks, hot spots can be caused by frequently accessed records, inefficient data access methods, and the need to coordinate access to legacy systems.</span></span>

## <a name="connecting-to-the-data-tier"></a><span data-ttu-id="bd820-107">Conectando-se à camada de dados</span><span class="sxs-lookup"><span data-stu-id="bd820-107">Connecting to the Data Tier</span></span>

<span data-ttu-id="bd820-108">Duas considerações desempenham um papel importante na criação de uma camada de dados para um aplicativo COM+: pooling de conexões e [ativação JIT (just-in-time) com+](com--just-in-time-activation.md)e o uso de DSNs.</span><span class="sxs-lookup"><span data-stu-id="bd820-108">Two considerations play an important role in designing a data tier for a COM+ application: connection pooling and [COM+ just-in-time (JIT) activation](com--just-in-time-activation.md), and the use of DSNs.</span></span> <span data-ttu-id="bd820-109">Os componentes que fazem conexões com a camada de dados devem usar o conjunto de [pools de objetos com+](com--object-pooling.md) no componente.</span><span class="sxs-lookup"><span data-stu-id="bd820-109">Components that make connections to the data tier should use [COM+ object pooling](com--object-pooling.md) set on the component.</span></span>

<span data-ttu-id="bd820-110">Ao criar DSNs, use as cadeias de caracteres de construtor de objeto especificadas no componente em vez de criar um DSN de arquivo.</span><span class="sxs-lookup"><span data-stu-id="bd820-110">When creating DSNs, use object constructor strings specified on the component instead of creating a File DSN.</span></span> <span data-ttu-id="bd820-111">Os DSNs de arquivo são mais lentos que uma conexão usando uma cadeia de caracteres de construtor de objeto.</span><span class="sxs-lookup"><span data-stu-id="bd820-111">File DSNs are slower than a connection using an object constructor string.</span></span> <span data-ttu-id="bd820-112">As cadeias de caracteres do construtor de objetos podem ser especificadas na folha de propriedades do componente.</span><span class="sxs-lookup"><span data-stu-id="bd820-112">Object constructor strings can be specified on the component property sheet.</span></span> <span data-ttu-id="bd820-113">Para obter mais informações, consulte [cadeias de caracteres do construtor de objeto com+](com--object-constructor-strings.md).</span><span class="sxs-lookup"><span data-stu-id="bd820-113">For more information, see [COM+ Object Constructor Strings](com--object-constructor-strings.md).</span></span>

<span data-ttu-id="bd820-114">Se você estiver usando componentes para acessar um banco de dados SQL Server, use o pool de objetos COM+ em vez do pool de conexões SQL.</span><span class="sxs-lookup"><span data-stu-id="bd820-114">If you are using components to access a SQL Server database, use COM+ object pooling instead of SQL connection pooling.</span></span>

<span data-ttu-id="bd820-115">Se o componente estiver usando o ADO para buscar vários conjuntos de registros, estabeleça várias conexões para o componente.</span><span class="sxs-lookup"><span data-stu-id="bd820-115">If your component is using ADO to fetch multiple recordsets, establish multiple connections for the component.</span></span> <span data-ttu-id="bd820-116">Quando o ADO recupera vários conjuntos de registros, ele cria várias conexões em segundo plano se você não criá-las.</span><span class="sxs-lookup"><span data-stu-id="bd820-116">When ADO retrieves multiple recordsets, it creates multiple connections in the background if you do not create them.</span></span> <span data-ttu-id="bd820-117">Se você criá-los, poderá agrupá-los e ter mais controle sobre o número de conexões usadas.</span><span class="sxs-lookup"><span data-stu-id="bd820-117">If you create them, you can pool them and have more control over the number of the connections used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd820-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd820-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd820-119">Otimização de interações entre a camada de lógica de negócios COM+ e a camada de apresentação</span><span class="sxs-lookup"><span data-stu-id="bd820-119">Optimizing Interactions Between the COM+ Business Logic Tier and the Presentation Tier</span></span>](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



