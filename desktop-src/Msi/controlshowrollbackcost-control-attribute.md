---
description: Esse atributo especifica se os arquivos de backup de reversão são incluídos nos custos exibidos pelo controle VolumeCostList.
ms.assetid: a3ed4d8a-170b-4708-afc2-03d2a5b665a3
title: Atributo de controle ControlShowRollbackCost
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7947777a356933ab74051163b6b9b023736dbb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829478"
---
# <a name="controlshowrollbackcost-control-attribute"></a><span data-ttu-id="7607f-103">Atributo de controle ControlShowRollbackCost</span><span class="sxs-lookup"><span data-stu-id="7607f-103">ControlShowRollbackCost Control Attribute</span></span>

<span data-ttu-id="7607f-104">Esse atributo especifica se os arquivos de backup de reversão são incluídos nos custos exibidos pelo [controle VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="7607f-104">This attribute specifies whether or not the rollback backup files are included in the costs displayed by the [VolumeCostList control](volumecostlist-control.md).</span></span>

<span data-ttu-id="7607f-105">Se esse bit for definido e a propriedade [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, os arquivos de backup de reversão serão incluídos no custo exibido pelo [controle VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="7607f-105">If this bit is set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

<span data-ttu-id="7607f-106">Se esse bit não for definido e a propriedade [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = P, os arquivos de backup de reversão não serão incluídos no custo exibido pelo [controle VolumeCostList](volumecostlist-control.md).</span><span class="sxs-lookup"><span data-stu-id="7607f-106">If this bit is not set and [**PROMPTROLLBACKCOST**](promptrollbackcost.md) property = P, the rollback backup files are not included in the cost displayed by the [VolumeCostList Control](volumecostlist-control.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="7607f-107">Controles válidos</span><span class="sxs-lookup"><span data-stu-id="7607f-107">Valid Controls</span></span>

[<span data-ttu-id="7607f-108">VolumeCostList</span><span class="sxs-lookup"><span data-stu-id="7607f-108">VolumeCostList</span></span>](volumecostlist-control.md)

## <a name="value"></a><span data-ttu-id="7607f-109">Valor</span><span class="sxs-lookup"><span data-stu-id="7607f-109">Value</span></span>



| <span data-ttu-id="7607f-110">Decimal</span><span class="sxs-lookup"><span data-stu-id="7607f-110">Decimal</span></span> | <span data-ttu-id="7607f-111">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7607f-111">Hexadecimal</span></span> | <span data-ttu-id="7607f-112">Constante</span><span class="sxs-lookup"><span data-stu-id="7607f-112">Constant</span></span>                         |
|---------|-------------|----------------------------------|
| <span data-ttu-id="7607f-113">4194304</span><span class="sxs-lookup"><span data-stu-id="7607f-113">4194304</span></span> | <span data-ttu-id="7607f-114">0x00400000</span><span class="sxs-lookup"><span data-stu-id="7607f-114">0x00400000</span></span>  | <span data-ttu-id="7607f-115">**msidbControlShowRollbackCost**</span><span class="sxs-lookup"><span data-stu-id="7607f-115">**msidbControlShowRollbackCost**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7607f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7607f-116">Remarks</span></span>

<span data-ttu-id="7607f-117">Esse atributo de controle será ignorado se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou F.</span><span class="sxs-lookup"><span data-stu-id="7607f-117">This control attribute is ignored if [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D or F.</span></span>

<span data-ttu-id="7607f-118">Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, o custo da reversão, os arquivos de backup serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="7607f-118">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = F, the cost of the rollback, backup files is included.</span></span>

<span data-ttu-id="7607f-119">Se [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D ou [**DISABLEROLLBACK**](-disablerollback.md) Propriedade = 1, o custo da reversão, os arquivos de backup não serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="7607f-119">If [**PROMPTROLLBACKCOST**](promptrollbackcost.md) = D, or [**DISABLEROLLBACK**](-disablerollback.md) property = 1, the cost of the rollback, backup files is not included.</span></span>

 

 



