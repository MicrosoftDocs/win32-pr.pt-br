---
description: Os qualificadores a seguir são usados pelo provedor WDM em arquivos de driver de dispositivo MOF quando estão extraindo dados do WNODEs para gerar instâncias de classes de driver WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Qualificadores específicos para o provedor WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788852"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="068ec-103">Qualificadores específicos para o provedor WDM</span><span class="sxs-lookup"><span data-stu-id="068ec-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="068ec-104">Os qualificadores a seguir são usados pelo [provedor WDM](/windows/desktop/WmiCoreProv/wdm-provider) em arquivos de driver de dispositivo MOF quando estão extraindo dados do WNODEs para gerar instâncias de classes de driver WDM.</span><span class="sxs-lookup"><span data-stu-id="068ec-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="068ec-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**Faltandovalue**</span><span class="sxs-lookup"><span data-stu-id="068ec-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="068ec-106">Tipo de dados: **DWORD, array, uint8, UInt16, UInt32, sint8, sint16 ou sint32.**</span><span class="sxs-lookup"><span data-stu-id="068ec-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="068ec-107">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="068ec-107">Applies to: properties</span></span>

<span data-ttu-id="068ec-108">Um valor ausente para essa propriedade deve ser representado por **NULL** em vez de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="068ec-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="068ec-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span><span class="sxs-lookup"><span data-stu-id="068ec-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="068ec-110">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="068ec-110">Data type: **uint32**</span></span>

<span data-ttu-id="068ec-111">Aplica-se a: Propriedades</span><span class="sxs-lookup"><span data-stu-id="068ec-111">Applies to: properties</span></span>

<span data-ttu-id="068ec-112">Índice na WNODE dos dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="068ec-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="068ec-113">O provedor WDM usa esse qualificador para determinar como os dados são formatados ao extrair dados do WNODE e gerar classes WMI.</span><span class="sxs-lookup"><span data-stu-id="068ec-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="068ec-114">O valor inicial é 1.</span><span class="sxs-lookup"><span data-stu-id="068ec-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="068ec-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span><span class="sxs-lookup"><span data-stu-id="068ec-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="068ec-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="068ec-116">Data type: **uint32**</span></span>

<span data-ttu-id="068ec-117">Aplica-se a: classes</span><span class="sxs-lookup"><span data-stu-id="068ec-117">Applies to: classes</span></span>

<span data-ttu-id="068ec-118">Indicação do custo do recurso para acessar o bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="068ec-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="068ec-119">Por exemplo, as informações de geometria de disco não exigem muitos recursos para obter, pois estão disponíveis na extensão do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="068ec-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="068ec-120">O desempenho de leitura/gravação de disco é mais intensivo por recursos porque requer trabalho extra em cada operação de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="068ec-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="068ec-121">Portanto, o valor do qualificador **WMIExpense** é maior para o desempenho de leitura/gravação no disco.</span><span class="sxs-lookup"><span data-stu-id="068ec-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="068ec-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span><span class="sxs-lookup"><span data-stu-id="068ec-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="068ec-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="068ec-123">Data type: **uint32**</span></span>

<span data-ttu-id="068ec-124">Aplica-se a: métodos</span><span class="sxs-lookup"><span data-stu-id="068ec-124">Applies to: methods</span></span>

<span data-ttu-id="068ec-125">Índice na WNODE dos dados da propriedade.</span><span class="sxs-lookup"><span data-stu-id="068ec-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="068ec-126">O provedor WDM usa esse qualificador para determinar como os dados são formatados ao extrair dados do WNODE e gerar classes WMI.</span><span class="sxs-lookup"><span data-stu-id="068ec-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="068ec-127">O valor inicial é 1.</span><span class="sxs-lookup"><span data-stu-id="068ec-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="068ec-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="068ec-128">Requirements</span></span>



| <span data-ttu-id="068ec-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="068ec-129">Requirement</span></span> | <span data-ttu-id="068ec-130">Valor</span><span class="sxs-lookup"><span data-stu-id="068ec-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="068ec-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="068ec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="068ec-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="068ec-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="068ec-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="068ec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="068ec-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="068ec-134">Windows Server 2008</span></span><br/> |



 

