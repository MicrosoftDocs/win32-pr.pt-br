---
title: Estrutura de WINBIO_EXTENDED_STORAGE_INFO (WinBio \_ Types. h)
description: Contém informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_STORAGE_INFO
- Ponteiro de estrutura de PWINBIO_EXTENDED_STORAGE_INFO Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918094"
---
# <a name="winbio_extended_storage_info-structure"></a><span data-ttu-id="e11c8-105">\_Estrutura de \_ informações de armazenamento ESTENDIdo WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="e11c8-105">WINBIO\_EXTENDED\_STORAGE\_INFO structure</span></span>

<span data-ttu-id="e11c8-106">Contém informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica.</span><span class="sxs-lookup"><span data-stu-id="e11c8-106">Contains information about the capabilities and enrollment requirements of the storage adapter for a biometric unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e11c8-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a><span data-ttu-id="e11c8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e11c8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e11c8-109">**GenericStorageCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e11c8-109">**GenericStorageCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-110">Os recursos genéricos do componente de armazenamento que está conectado a uma unidade biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="e11c8-110">The generic capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> <dt>

<span data-ttu-id="e11c8-111">**Fator**</span><span class="sxs-lookup"><span data-stu-id="e11c8-111">**Factor**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-112">O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e11c8-112">The type of biometric unit for which this structure contains information about capabilities and enrollment requirements of the storage adapter.</span></span> <span data-ttu-id="e11c8-113">Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de **\_ \_ \_ informações de armazenamento estendida WINBIO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .</span><span class="sxs-lookup"><span data-stu-id="e11c8-113">For example, if the value of the **Factor** member is **WINBIO\_TYPE\_FINGERPRINT**, the **WINBIO\_EXTENDED\_STORAGE\_INFO** structure applies to a fingerprint reader and contains the relevant information in the **Specifc.Fingerprint** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e11c8-114">**Específicas**</span><span class="sxs-lookup"><span data-stu-id="e11c8-114">**Specific**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-115">Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a um fator biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="e11c8-115">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to a specific biometric factor.</span></span>

<dl> <dt>

<span data-ttu-id="e11c8-116">**Nulo**</span><span class="sxs-lookup"><span data-stu-id="e11c8-116">**Null**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-117">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e11c8-117">Reserved.</span></span> <span data-ttu-id="e11c8-118">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e11c8-118">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e11c8-119">**FacialFeatures**</span><span class="sxs-lookup"><span data-stu-id="e11c8-119">**FacialFeatures**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-120">Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada aos recursos faciais.</span><span class="sxs-lookup"><span data-stu-id="e11c8-120">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to facial features.</span></span>

<dl> <dt>

<span data-ttu-id="e11c8-121">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="e11c8-121">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-122">Os recursos de reconhecimento facial do componente de armazenamento que está conectado a uma unidade biométrica específica.</span><span class="sxs-lookup"><span data-stu-id="e11c8-122">The facial recognition capabilities of the storage component that is connected to a specific biometric unit.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e11c8-123">**Fingerprint**</span><span class="sxs-lookup"><span data-stu-id="e11c8-123">**Fingerprint**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-124">Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de impressão digital.</span><span class="sxs-lookup"><span data-stu-id="e11c8-124">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to fingerprint patterns.</span></span>

<dl> <dt>

<span data-ttu-id="e11c8-125">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="e11c8-125">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-126">Os recursos de reconhecimento de impressão digital do componente de armazenamento que está conectado a uma unidade biométrica específica</span><span class="sxs-lookup"><span data-stu-id="e11c8-126">The fingerprint recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e11c8-127">**Íris**</span><span class="sxs-lookup"><span data-stu-id="e11c8-127">**Iris**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-128">Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de íris.</span><span class="sxs-lookup"><span data-stu-id="e11c8-128">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to iris patterns.</span></span>

<dl> <dt>

<span data-ttu-id="e11c8-129">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="e11c8-129">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-130">Os recursos de reconhecimento de íris do componente de armazenamento que está conectado a uma unidade biométrica específica</span><span class="sxs-lookup"><span data-stu-id="e11c8-130">The iris recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e11c8-131">**Voz**</span><span class="sxs-lookup"><span data-stu-id="e11c8-131">**Voice**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-132">Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de voz.</span><span class="sxs-lookup"><span data-stu-id="e11c8-132">Information about the capabilities and enrollment requirements of the storage adapter for a biometric unit related to voice patterns.</span></span>

<dl> <dt>

<span data-ttu-id="e11c8-133">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="e11c8-133">**Capabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e11c8-134">Os recursos de reconhecimento de voz do componente de armazenamento que está conectado a uma unidade biométrica específica</span><span class="sxs-lookup"><span data-stu-id="e11c8-134">The voice recognition capabilities of the storage component that is connected to a specific biometric unit</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e11c8-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11c8-135">Requirements</span></span>



| <span data-ttu-id="e11c8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11c8-136">Requirement</span></span> | <span data-ttu-id="e11c8-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e11c8-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11c8-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e11c8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e11c8-139">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e11c8-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e11c8-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e11c8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e11c8-141">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e11c8-141">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="e11c8-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e11c8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e11c8-143"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="e11c8-143"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11c8-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e11c8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11c8-145">**\_Constantes de tipo BIOMÉTRICO WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="e11c8-145">**WINBIO\_BIOMETRIC\_TYPE Constants**</span></span>](winbio-biometric-type-constants.md)
</dt> <dt>

[<span data-ttu-id="e11c8-146">**\_Constantes de recurso WINBIO**</span><span class="sxs-lookup"><span data-stu-id="e11c8-146">**WINBIO\_CAPABILITY Constants**</span></span>](winbio-capability-constants.md)
</dt> </dl>

 

 





