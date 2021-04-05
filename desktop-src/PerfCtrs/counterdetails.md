---
description: A tabela de detalhes descreve um contador específico em um determinado computador.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: Detalhes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921751"
---
# <a name="counterdetails"></a><span data-ttu-id="d4569-103">Detalhes</span><span class="sxs-lookup"><span data-stu-id="d4569-103">CounterDetails</span></span>

<span data-ttu-id="d4569-104">A tabela de **detalhes** descreve um contador específico em um determinado computador.</span><span class="sxs-lookup"><span data-stu-id="d4569-104">The **CounterDetails** table describes a specific counter on a particular computer.</span></span>

<span data-ttu-id="d4569-105">A tabela de **detalhes** define os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="d4569-105">The **CounterDetails** table defines the following fields:</span></span>

-   <span data-ttu-id="d4569-106">**Counterid:** Um identificador exclusivo no banco de dados que é mapeado para uma cadeia de caracteres de texto de nome de contador específico.</span><span class="sxs-lookup"><span data-stu-id="d4569-106">**CounterID:** A unique identifier in the database that maps to a specific counter name text string.</span></span> <span data-ttu-id="d4569-107">Este campo é a chave primária desta tabela.</span><span class="sxs-lookup"><span data-stu-id="d4569-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="d4569-108">**MachineName:** O nome do computador que registrou esse conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="d4569-108">**MachineName:** The name of the computer that logged this data set.</span></span>
-   <span data-ttu-id="d4569-109">**ObjectName:** O nome do objeto de desempenho.</span><span class="sxs-lookup"><span data-stu-id="d4569-109">**ObjectName:** The name of the performance object.</span></span>
-   <span data-ttu-id="d4569-110">**CounterName:** O nome do contador.</span><span class="sxs-lookup"><span data-stu-id="d4569-110">**CounterName:** The name of the counter.</span></span>
-   <span data-ttu-id="d4569-111">**Tipoy:** O tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="d4569-111">**CounterType:** The counter type.</span></span> <span data-ttu-id="d4569-112">Para obter uma lista de tipos de contadores e suas fórmulas, consulte a seção tipos de contadores do [Kit de implantação do Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="d4569-112">For a list of counter types and their formulas, see the Counter Types section of the [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span></span>
-   <span data-ttu-id="d4569-113">**DefaultScale:** O dimensionamento padrão a ser aplicado aos dados brutos do contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="d4569-113">**DefaultScale:** The default scaling to be applied to the raw performance counter data.</span></span>
-   <span data-ttu-id="d4569-114">**InstanceName:** O nome da instância do contador.</span><span class="sxs-lookup"><span data-stu-id="d4569-114">**InstanceName:** The name of the counter instance.</span></span>
-   <span data-ttu-id="d4569-115">**InstanceIndex:** O número de índice da instância do contador.</span><span class="sxs-lookup"><span data-stu-id="d4569-115">**InstanceIndex:** The index number of the counter instance.</span></span>
-   <span data-ttu-id="d4569-116">**ParentName:** Alguns contadores são logicamente associados a outras pessoas e são chamados de pais.</span><span class="sxs-lookup"><span data-stu-id="d4569-116">**ParentName:** Some counters are logically associated with others, and are referred to as parents.</span></span> <span data-ttu-id="d4569-117">Por exemplo, o pai de um thread é um processo e o pai de um driver de disco lógico é uma unidade física.</span><span class="sxs-lookup"><span data-stu-id="d4569-117">For example, the parent of a thread is a process and the parent of a logical disk driver is a physical drive.</span></span> <span data-ttu-id="d4569-118">Este campo contém o nome do pai.</span><span class="sxs-lookup"><span data-stu-id="d4569-118">This field contains the name of the parent.</span></span> <span data-ttu-id="d4569-119">O valor neste campo ou o campo **ParentObjectID** identifica uma instância pai específica.</span><span class="sxs-lookup"><span data-stu-id="d4569-119">Either the value in this field or the **ParentObjectID** field identifies a specific parent instance.</span></span> <span data-ttu-id="d4569-120">Se o valor nesse campo for **nulo**, o valor no campo **ParentObjectID** deverá ser verificado para identificar o pai.</span><span class="sxs-lookup"><span data-stu-id="d4569-120">If the value in this field is **NULL**, the value in the **ParentObjectID** field must be checked to identify the parent.</span></span> <span data-ttu-id="d4569-121">Se os valores em ambos os campos forem **nulos**, o contador não terá um pai.</span><span class="sxs-lookup"><span data-stu-id="d4569-121">If the values in both fields are **NULL**, the counter does not have a parent.</span></span>
-   <span data-ttu-id="d4569-122">**ParentObjectID:** O identificador exclusivo do pai.</span><span class="sxs-lookup"><span data-stu-id="d4569-122">**ParentObjectID:** The unique identifier of the parent.</span></span> <span data-ttu-id="d4569-123">O valor desse campo ou **painame** identifica uma instância pai específica.</span><span class="sxs-lookup"><span data-stu-id="d4569-123">The value in either this field or the **ParentName** field identifies a specific parent instance.</span></span> <span data-ttu-id="d4569-124">Se o valor nesse campo for **nulo**, o valor no campo **parentName** deverá ser verificado para identificar o pai.</span><span class="sxs-lookup"><span data-stu-id="d4569-124">If the value in this field is **NULL**, the value in the **ParentName** field must be checked to identify the parent.</span></span>

 

 
