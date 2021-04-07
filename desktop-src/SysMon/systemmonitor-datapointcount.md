---
title: Propriedade SystemMonitor. DataPointCount
description: Recupera ou define o número de pontos de dados exibidos em um grafo de linha.
ms.assetid: bc1a86c2-635b-4e93-ac96-e7be4b1d375a
keywords:
- Propriedade DataPointCount SysMon
- Propriedade DataPointCount SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, Propriedade DataPointCount
topic_type:
- apiref
api_name:
- SystemMonitor.DataPointCount
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffb8b39216895ce4ebce6924ca7cc99b5366cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918220"
---
# <a name="systemmonitordatapointcount-property"></a><span data-ttu-id="12d7c-106">Propriedade SystemMonitor. DataPointCount</span><span class="sxs-lookup"><span data-stu-id="12d7c-106">SystemMonitor.DataPointCount property</span></span>

<span data-ttu-id="12d7c-107">Recupera ou define o número de pontos de dados exibidos em um grafo de linha.</span><span class="sxs-lookup"><span data-stu-id="12d7c-107">Retrieves or sets the number of data points displayed in a line graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d7c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="12d7c-108">Syntax</span></span>


```VB
Property DataPointCount As Long
```



## <a name="property-value"></a><span data-ttu-id="12d7c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="12d7c-109">Property value</span></span>

<span data-ttu-id="12d7c-110">Número de pontos de dados exibidos na exibição de um gráfico de linhas.</span><span class="sxs-lookup"><span data-stu-id="12d7c-110">Number of data points displayed in the view for a line graph.</span></span> <span data-ttu-id="12d7c-111">O valor padrão é 100 pontos de dados.</span><span class="sxs-lookup"><span data-stu-id="12d7c-111">The default value is 100 data points.</span></span> <span data-ttu-id="12d7c-112">O intervalo válido de valores é de 2 a 1.000.</span><span class="sxs-lookup"><span data-stu-id="12d7c-112">The valid range of values is 2 to 1,000.</span></span>

## <a name="remarks"></a><span data-ttu-id="12d7c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="12d7c-113">Remarks</span></span>

<span data-ttu-id="12d7c-114">Essa propriedade será usada somente se [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for **sysmonCurrentActivity**.</span><span class="sxs-lookup"><span data-stu-id="12d7c-114">This property is used only if [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is **sysmonCurrentActivity**.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d7c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12d7c-115">Requirements</span></span>



| <span data-ttu-id="12d7c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d7c-116">Requirement</span></span> | <span data-ttu-id="12d7c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="12d7c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12d7c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12d7c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="12d7c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12d7c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12d7c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12d7c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="12d7c-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12d7c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12d7c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="12d7c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d7c-123"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="12d7c-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





