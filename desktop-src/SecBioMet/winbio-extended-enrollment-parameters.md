---
title: Estrutura de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS ( \_ adaptador WINBIO. h)
description: Contém informações adicionais que um adaptador de mecanismo precisa para criar um modelo de registro.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
- Ponteiro de estrutura de PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454796"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a><span data-ttu-id="9e966-105">\_Estrutura de \_ parâmetros de registro ESTENDIdo WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="9e966-105">WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS structure</span></span>

<span data-ttu-id="9e966-106">A estrutura de **\_ \_ \_ parâmetros de registro estendido WINBIO** contém informações adicionais que um adaptador de mecanismo precisa para criar um modelo de registro.</span><span class="sxs-lookup"><span data-stu-id="9e966-106">The **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure contains additional information that an engine adapter needs to create an enrollment template.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e966-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e966-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="9e966-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9e966-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e966-109">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="9e966-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="9e966-110">O tamanho (em bytes) da estrutura **de \_ \_ \_ parâmetros de registro estendido do WINBIO** .</span><span class="sxs-lookup"><span data-stu-id="9e966-110">The size (in bytes) of the **WINBIO\_EXTENDED\_ENROLLMENT\_PARAMETERS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="9e966-111">**Subfator**</span><span class="sxs-lookup"><span data-stu-id="9e966-111">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="9e966-112">Um dos valores [**\_ \_ constantes do subtipo WINBIO Biometric**](winbio-biometric-subtype-constants.md) que fornece informações adicionais sobre o registro.</span><span class="sxs-lookup"><span data-stu-id="9e966-112">One of the [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md) values that provides additional information about the enrollment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e966-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e966-113">Remarks</span></span>

<span data-ttu-id="9e966-114">O Windows Biometric Framework passa essa estrutura para o método [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante uma operação de registro.</span><span class="sxs-lookup"><span data-stu-id="9e966-114">The Windows Biometric Framework passes this structure to the [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) method during an enrollment operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e966-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e966-115">Requirements</span></span>



| <span data-ttu-id="9e966-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e966-116">Requirement</span></span> | <span data-ttu-id="9e966-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9e966-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e966-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e966-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9e966-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="9e966-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="9e966-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e966-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9e966-121">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="9e966-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="9e966-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e966-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e966-123"><dt>\_Adaptador WinBio. h (inclui o \_ adaptador WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e966-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





