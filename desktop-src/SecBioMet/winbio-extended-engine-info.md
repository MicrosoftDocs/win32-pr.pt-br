---
title: Estrutura de WINBIO_EXTENDED_ENGINE_INFO (WinBio \_ Types. h)
description: Contém informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_ENGINE_INFO
- Ponteiro de estrutura de PWINBIO_EXTENDED_ENGINE_INFO Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824781"
---
# <a name="winbio_extended_engine_info-structure"></a><span data-ttu-id="49ece-105">\_Estrutura de \_ informações do mecanismo estendido do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="49ece-105">WINBIO\_EXTENDED\_ENGINE\_INFO structure</span></span>

<span data-ttu-id="49ece-106">Contém informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="49ece-106">Contains information about the capabilities and enrollment requirements of the engine adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="49ece-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49ece-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a><span data-ttu-id="49ece-108">Membros</span><span class="sxs-lookup"><span data-stu-id="49ece-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="49ece-109">**GenericEngineCapabilities**</span><span class="sxs-lookup"><span data-stu-id="49ece-109">**GenericEngineCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-110">Os recursos genéricos do componente do mecanismo que está conectado a uma unidade biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="49ece-110">The generic capabilities of the engine component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-111">**Fator**</span><span class="sxs-lookup"><span data-stu-id="49ece-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-112">O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="49ece-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the engine adapter.</span></span> <span data-ttu-id="49ece-113">Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de **\_ \_ \_ informações do mecanismo estendido WINBIO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="49ece-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_ENGINE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-114">**Específicas**</span><span class="sxs-lookup"><span data-stu-id="49ece-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-115">Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a um fator biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="49ece-115">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="49ece-116">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="49ece-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-117">Reserved.</span></span> <span data-ttu-id="49ece-118">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="49ece-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-120">Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada aos recursos faciais.</span><span class="sxs-lookup"><span data-stu-id="49ece-120">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="49ece-121">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="49ece-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-122">Reserved.</span></span> <span data-ttu-id="49ece-123">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-123">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-124">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="49ece-124">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49ece-125">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="49ece-125">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-126">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-126">Reserved.</span></span> <span data-ttu-id="49ece-127">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-127">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="49ece-128">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="49ece-128">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-129">Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a padrões de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-129">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="49ece-130">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="49ece-130">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-131">Reserved.</span></span> <span data-ttu-id="49ece-132">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-132">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-133">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="49ece-133">**EnrollmentRequirements**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-134">O número de exemplos bons necessários para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-134">The number of good samples required to create a new fingerprint template.</span></span>

<dl> <dt>

<span data-ttu-id="49ece-135">**GeneralSamples**</span><span class="sxs-lookup"><span data-stu-id="49ece-135">**GeneralSamples**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-136">O número total de boas amostras necessárias para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-136">The total number of good samples required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-137">**Centraliza**</span><span class="sxs-lookup"><span data-stu-id="49ece-137">**Center**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-138">O número de exemplos bons para o centro da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-138">The number of good samples for the center of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-139">**TopEdge**</span><span class="sxs-lookup"><span data-stu-id="49ece-139">**TopEdge**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-140">O número de exemplos bons para a borda superior da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-140">The number of good samples for the top edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-141">**BottomEdge**</span><span class="sxs-lookup"><span data-stu-id="49ece-141">**BottomEdge**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-142">O número de exemplos bons para a borda inferior da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-142">The number of good samples for the bottom edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-143">**LeftEdge**</span><span class="sxs-lookup"><span data-stu-id="49ece-143">**LeftEdge**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-144">O número de exemplos bons para a borda esquerda da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-144">The number of good samples for the left edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-145">**RightEdge**</span><span class="sxs-lookup"><span data-stu-id="49ece-145">**RightEdge**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-146">O número de exemplos bons para a borda direita da impressão digital necessária para criar um novo modelo de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="49ece-146">The number of good samples for the right edge of the fingerprint required to create a new fingerprint template.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="49ece-147">**Íris**</span><span class="sxs-lookup"><span data-stu-id="49ece-147">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-148">Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a padrões de íris.</span><span class="sxs-lookup"><span data-stu-id="49ece-148">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="49ece-149">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="49ece-149">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-150">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-150">Reserved.</span></span> <span data-ttu-id="49ece-151">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-151">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-152">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="49ece-152">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49ece-153">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="49ece-153">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-154">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-154">Reserved.</span></span> <span data-ttu-id="49ece-155">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-155">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> <dt>

<span data-ttu-id="49ece-156">**Voz**</span><span class="sxs-lookup"><span data-stu-id="49ece-156">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-157">Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a padrões de voz.</span><span class="sxs-lookup"><span data-stu-id="49ece-157">Information about the capabilities and enrollment requirements of the engine adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="49ece-158">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="49ece-158">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-159">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-159">Reserved.</span></span> <span data-ttu-id="49ece-160">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-160">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49ece-161">**EnrollmentRequirements**</span><span class="sxs-lookup"><span data-stu-id="49ece-161">**EnrollmentRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49ece-162">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="49ece-162">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="49ece-163">Reservado.</span><span class="sxs-lookup"><span data-stu-id="49ece-163">Reserved.</span></span> <span data-ttu-id="49ece-164">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49ece-164">Must be zero.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49ece-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ece-165">Requirements</span></span>



| <span data-ttu-id="49ece-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ece-166">Requirement</span></span> | <span data-ttu-id="49ece-167">Valor</span><span class="sxs-lookup"><span data-stu-id="49ece-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ece-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49ece-168">Minimum supported client</span></span><br/> | <span data-ttu-id="49ece-169">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="49ece-169">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="49ece-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49ece-170">Minimum supported server</span></span><br/> | <span data-ttu-id="49ece-171">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="49ece-171">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="49ece-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49ece-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ece-173"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="49ece-173"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49ece-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="49ece-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ece-175">**\_Constantes de recurso WINBIO**</span><span class="sxs-lookup"><span data-stu-id="49ece-175">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> <dt>

[<span data-ttu-id="49ece-176">**\_Constantes de tipo BIOMÉTRICO WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="49ece-176">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> </dl>

 

 





