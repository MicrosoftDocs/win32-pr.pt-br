---
title: Classe Win32_WinSAT
description: Define informações de avaliação de resumo para a avaliação formal mais recente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- WinSAT de classe de Win32_WinSAT
- Classe Win32_WinSAT WinSAT, descrita
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762996"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="a2278-105">\_Classe Win32 WinSAT</span><span class="sxs-lookup"><span data-stu-id="a2278-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="a2278-106">\[**Win32 \_ O WinSAT** pode ser alterado ou indisponível para versões após a Windows 8.1.\]</span><span class="sxs-lookup"><span data-stu-id="a2278-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="a2278-107">Define informações de avaliação de resumo para a avaliação formal mais recente.</span><span class="sxs-lookup"><span data-stu-id="a2278-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="a2278-108">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a2278-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2278-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2278-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="a2278-110">Membros</span><span class="sxs-lookup"><span data-stu-id="a2278-110">Members</span></span>

<span data-ttu-id="a2278-111">A classe **Win32 \_ WinSAT** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a2278-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="a2278-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2278-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a2278-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a2278-113">Properties</span></span>

<span data-ttu-id="a2278-114">A classe **Win32 \_ WinSAT** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a2278-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a2278-115">**CPUScore**</span><span class="sxs-lookup"><span data-stu-id="a2278-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-116">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="a2278-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-118">Uma pontuação para os processadores no computador.</span><span class="sxs-lookup"><span data-stu-id="a2278-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="a2278-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="a2278-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-120">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="a2278-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-122">Depois de Windows 8.1, o WinSAT não avalia mais os recursos de gráficos tridimensionais (jogos) do computador e a capacidade do driver gráfico de processar objetos e executar sombreadores usando essa avaliação.</span><span class="sxs-lookup"><span data-stu-id="a2278-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="a2278-123">Para compatibilidade, os valores de sentinela de relatório do WinSAT para as métricas e pontuações, no entanto, não são calculados em tempo real.</span><span class="sxs-lookup"><span data-stu-id="a2278-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="a2278-124">**DiskScore**</span><span class="sxs-lookup"><span data-stu-id="a2278-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-125">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="a2278-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-127">Uma pontuação para a taxa de transferência de leitura sequencial no disco rígido primário no computador.</span><span class="sxs-lookup"><span data-stu-id="a2278-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="a2278-128">**GraphicsScore**</span><span class="sxs-lookup"><span data-stu-id="a2278-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-129">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="a2278-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-131">Uma pontuação para os recursos gráficos do computador.</span><span class="sxs-lookup"><span data-stu-id="a2278-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="a2278-132">**MemoryScore**</span><span class="sxs-lookup"><span data-stu-id="a2278-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-133">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="a2278-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-135">Uma pontuação para a taxa de transferência de memória e a capacidade do computador.</span><span class="sxs-lookup"><span data-stu-id="a2278-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="a2278-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="a2278-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a2278-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a2278-139">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="a2278-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="a2278-140">Essa propriedade deve ser definida como "MostRecentAssessment" na cláusula WHERE da consulta WQL.</span><span class="sxs-lookup"><span data-stu-id="a2278-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="a2278-141">**WinSATAssessmentState**</span><span class="sxs-lookup"><span data-stu-id="a2278-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a2278-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-144">Estado da avaliação.</span><span class="sxs-lookup"><span data-stu-id="a2278-144">State of the assessment.</span></span> <span data-ttu-id="a2278-145">Para obter uma descrição dos valores possíveis, consulte a enumeração do [**\_ \_ estado de avaliação do WINSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .</span><span class="sxs-lookup"><span data-stu-id="a2278-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="a2278-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span><span class="sxs-lookup"><span data-stu-id="a2278-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a2278-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Válido** (1)</span><span class="sxs-lookup"><span data-stu-id="a2278-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a2278-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span><span class="sxs-lookup"><span data-stu-id="a2278-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a2278-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span><span class="sxs-lookup"><span data-stu-id="a2278-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a2278-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="a2278-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a2278-151">**WinSPRLevel**</span><span class="sxs-lookup"><span data-stu-id="a2278-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a2278-152">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="a2278-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="a2278-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a2278-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a2278-154">Pontuação básica do computador.</span><span class="sxs-lookup"><span data-stu-id="a2278-154">Base score for the computer.</span></span> <span data-ttu-id="a2278-155">Para obter detalhes sobre o valor de pontuação, consulte a propriedade [**IProvideWinSATResultsInfo:: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .</span><span class="sxs-lookup"><span data-stu-id="a2278-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a2278-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2278-156">Remarks</span></span>

<span data-ttu-id="a2278-157">Para obter informações sobre as pontuações do subcomponente, como **MemoryScore**, consulte a propriedade [**IProvideWinSATAssessmentInfo:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .</span><span class="sxs-lookup"><span data-stu-id="a2278-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="a2278-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a2278-158">Examples</span></span>

<span data-ttu-id="a2278-159">Para obter um exemplo que mostra como usar o WMI para recuperar dados dessa classe, consulte o método [**\_ bitmap IProvideWinSATVisuals:: Get**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .</span><span class="sxs-lookup"><span data-stu-id="a2278-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2278-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2278-160">Requirements</span></span>



| <span data-ttu-id="a2278-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2278-161">Requirement</span></span> | <span data-ttu-id="a2278-162">Valor</span><span class="sxs-lookup"><span data-stu-id="a2278-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2278-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2278-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a2278-164">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2278-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a2278-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2278-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a2278-166">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a2278-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a2278-167">Namespace</span><span class="sxs-lookup"><span data-stu-id="a2278-167">Namespace</span></span><br/>                | <span data-ttu-id="a2278-168">Raiz\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="a2278-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="a2278-169">MOF</span><span class="sxs-lookup"><span data-stu-id="a2278-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a2278-170"><dt>WinSAT. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a2278-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a2278-171">DLL</span><span class="sxs-lookup"><span data-stu-id="a2278-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2278-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2278-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 





