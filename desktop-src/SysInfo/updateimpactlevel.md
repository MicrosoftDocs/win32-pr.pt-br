---
description: Indica um impacto alto, médio ou baixo de um dispositivo que executa um sistema operacional desatualizado.
ms.assetid: C7F30B63-66B0-4F37-A05B-7D366A12B640
title: Enumeração UpdateImpactLevel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateImpactLevel
api_type:
- HeaderDef
api_location:
- waasapitypes.h
ms.openlocfilehash: c18cc7916abbc1dce595df9a21d2fdef3976af11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749432"
---
# <a name="updateimpactlevel-enumeration"></a><span data-ttu-id="fb814-103">Enumeração UpdateImpactLevel</span><span class="sxs-lookup"><span data-stu-id="fb814-103">UpdateImpactLevel enumeration</span></span>

<span data-ttu-id="fb814-104">Indica um impacto alto, médio ou baixo de um dispositivo que executa um sistema operacional desatualizado.</span><span class="sxs-lookup"><span data-stu-id="fb814-104">Indicates a high, medium, or low impact of a device running an out-of-date OS.</span></span> <span data-ttu-id="fb814-105">Essa enumeração é geralmente usada por estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) , que, por sua vez, são aninhadas dentro do [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) retornado de [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span><span class="sxs-lookup"><span data-stu-id="fb814-105">This enumeration is generally used by [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures, which is in turn nested inside the returned [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) from [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb814-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb814-106">Syntax</span></span>


```C++
typedef enum TagUpdateImpactLevel { 
      UpdateImpactLevel_None    = 0,
  UpdateImpactLevel_Low         = 1,
      UpdateImpactLevel_Medium  = 2,
  UpdateImpactLevel_High        = 3
} UpdateImpactLevel;
```



## <a name="constants"></a><span data-ttu-id="fb814-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="fb814-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fb814-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span>**UpdateImpactLevel \_ Nenhum**</span><span class="sxs-lookup"><span data-stu-id="fb814-108"><span id="____UpdateImpactLevel_None"></span><span id="____updateimpactlevel_none"></span><span id="____UPDATEIMPACTLEVEL_NONE"></span> **UpdateImpactLevel\_None**</span></span>
</dt> <dd>

<span data-ttu-id="fb814-109">Não há nenhum impacto previsto em seu dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb814-109">There is no foreseeable impact to your device.</span></span> <span data-ttu-id="fb814-110">Isso pode ocorrer porque o dispositivo está atualizado ou não está atualizado porque o dispositivo está respeitando sua Windows Update para períodos de adiamento de negócios ou está desatualizado, mas ainda não atingiu o limite de **daysOutOfDate** para alcançar um nível de impacto mais alto.</span><span class="sxs-lookup"><span data-stu-id="fb814-110">This can be because the device is up-to-date, or is not up-to-date because the device is honoring its Windows Update for Business deferral periods, or is out-of-date but has not yet reached the **daysOutOfDate** threshold to reach a higher impact level.</span></span>

</dd> <dt>

<span data-ttu-id="fb814-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel \_ baixo**</span><span class="sxs-lookup"><span data-stu-id="fb814-111"><span id="UpdateImpactLevel_Low"></span><span id="updateimpactlevel_low"></span><span id="UPDATEIMPACTLEVEL_LOW"></span>**UpdateImpactLevel\_Low**</span></span>
</dt> <dd>

<span data-ttu-id="fb814-112">O dispositivo não está executando o sistema operacional mais recente, mas tem uma atualização recente.</span><span class="sxs-lookup"><span data-stu-id="fb814-112">The device is not running the latest OS, but has a recent update.</span></span>

</dd> <dt>

<span data-ttu-id="fb814-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span>**UpdateImpactLevel \_ Média**</span><span class="sxs-lookup"><span data-stu-id="fb814-113"><span id="____UpdateImpactLevel_Medium"></span><span id="____updateimpactlevel_medium"></span><span id="____UPDATEIMPACTLEVEL_MEDIUM"></span> **UpdateImpactLevel\_Medium**</span></span>
</dt> <dd>

<span data-ttu-id="fb814-114">O dispositivo está executando o sistema operacional mais recente, mas tem uma atualização moderadamente recente.</span><span class="sxs-lookup"><span data-stu-id="fb814-114">The device is running the latest OS, but has a moderately recent update.</span></span>

</dd> <dt>

<span data-ttu-id="fb814-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel \_ alto**</span><span class="sxs-lookup"><span data-stu-id="fb814-115"><span id="UpdateImpactLevel_High"></span><span id="updateimpactlevel_high"></span><span id="UPDATEIMPACTLEVEL_HIGH"></span>**UpdateImpactLevel\_High**</span></span>
</dt> <dd>

<span data-ttu-id="fb814-116">O dispositivo está desatualizado há muito tempo.</span><span class="sxs-lookup"><span data-stu-id="fb814-116">The device has been out-of-date for a long time.</span></span> <span data-ttu-id="fb814-117">Este dispositivo pode ter vulnerabilidades de segurança e pode estar sem correções importantes que tornam o Windows mais bem executado.</span><span class="sxs-lookup"><span data-stu-id="fb814-117">This device may have security vulnerabilities and may be missing important fixes that make Windows run better.</span></span> <span data-ttu-id="fb814-118">Quando um dispositivo estiver executando uma versão do Windows que não tem mais suporte, o **UpdateImpactLevel \_ High** será sempre retornado.</span><span class="sxs-lookup"><span data-stu-id="fb814-118">When a device is running a version of Windows that is no longer supported, **UpdateImpactLevel\_High** is always returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb814-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb814-119">Remarks</span></span>

<span data-ttu-id="fb814-120">Quando [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) é chamado, uma estrutura [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) é retornada.</span><span class="sxs-lookup"><span data-stu-id="fb814-120">When [**GetOSUpdateAssessment**](/windows/desktop/api/waasapi/nf-waasapi-iwaasassessor-getosupdateassessment) is called, an [**OSUpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-osupdateassessment) structure is returned.</span></span> <span data-ttu-id="fb814-121">Na estrutura, há um **assessmentForCurrent** e um **assessmentForUpToDate**.</span><span class="sxs-lookup"><span data-stu-id="fb814-121">Within the structure there is an **assessmentForCurrent** and **assessmentForUpToDate**.</span></span> <span data-ttu-id="fb814-122">Ambas são estruturas [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) .</span><span class="sxs-lookup"><span data-stu-id="fb814-122">Both of these are [**UpdateAssessment**](/windows/win32/api/waasapitypes/ns-waasapitypes-updateassessment) structures.</span></span> <span data-ttu-id="fb814-123">Ambos os membros têm uma enumeração **UpdateImpactLevel** , que indica um alto, médio, baixo ou nenhum impacto para um dispositivo que esteja executando um sistema operacional desatualizado.</span><span class="sxs-lookup"><span data-stu-id="fb814-123">Both members have an **UpdateImpactLevel** enumeration, which indicates a high, medium, low or no impact for a device running an out-of-date OS.</span></span> <span data-ttu-id="fb814-124">Esses níveis são determinados pelo valor de **daysOutOfDate**.</span><span class="sxs-lookup"><span data-stu-id="fb814-124">The These levels are determined by the value of **daysOutOfDate**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb814-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb814-125">Requirements</span></span>



| <span data-ttu-id="fb814-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb814-126">Requirement</span></span> | <span data-ttu-id="fb814-127">Valor</span><span class="sxs-lookup"><span data-stu-id="fb814-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb814-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb814-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fb814-129">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="fb814-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fb814-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb814-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fb814-131">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="fb814-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fb814-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="fb814-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb814-133"><dt>WaaSAPI. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb814-133"><dt>WaaSAPI.idl</dt></span></span> </dl> |



 

 




