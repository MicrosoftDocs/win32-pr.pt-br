---
title: Estrutura de WINBIO_BSP_SCHEMA (WinBio \_ Types. h)
description: Descreve os recursos de um provedor de serviços biométricos.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BSP_SCHEMA
- Ponteiro de estrutura de PWINBIO_BSP_SCHEMA Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455199"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="42f13-105">\_Estrutura de \_ esquema WINBIO BSP</span><span class="sxs-lookup"><span data-stu-id="42f13-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="42f13-106">A estrutura de **\_ \_ esquema WINBIO BSP** descreve os recursos de um provedor de serviços biométricos.</span><span class="sxs-lookup"><span data-stu-id="42f13-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="42f13-107">Essa estrutura é usada pela função [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .</span><span class="sxs-lookup"><span data-stu-id="42f13-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f13-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42f13-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="42f13-109">Membros</span><span class="sxs-lookup"><span data-stu-id="42f13-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="42f13-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="42f13-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="42f13-111">O tipo de medição biométrica usada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42f13-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="42f13-112">Atualmente, ela deve ser uma **\_ \_ impressão digital do tipo WINBIO**.</span><span class="sxs-lookup"><span data-stu-id="42f13-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="42f13-113">**BspId**</span><span class="sxs-lookup"><span data-stu-id="42f13-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="42f13-114">Um valor que identifica exclusivamente esse componente de provedor de serviços biométricos.</span><span class="sxs-lookup"><span data-stu-id="42f13-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="42f13-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="42f13-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="42f13-116">Uma cadeia de caracteres Unicode terminada em **nulo** que contém uma descrição do provedor de serviços biométricos.</span><span class="sxs-lookup"><span data-stu-id="42f13-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="42f13-117">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="42f13-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="42f13-118">Uma cadeia de caracteres Unicode terminada em **nulo** que contém o nome do fornecedor que fornece o provedor de serviços biométricos.</span><span class="sxs-lookup"><span data-stu-id="42f13-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="42f13-119">**Versão**</span><span class="sxs-lookup"><span data-stu-id="42f13-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="42f13-120">Uma estrutura de [**\_ versão do WINBIO**](winbio-version.md) contém a versão de software do componente do provedor de serviços biométricos.</span><span class="sxs-lookup"><span data-stu-id="42f13-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42f13-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f13-121">Requirements</span></span>



| <span data-ttu-id="42f13-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f13-122">Requirement</span></span> | <span data-ttu-id="42f13-123">Valor</span><span class="sxs-lookup"><span data-stu-id="42f13-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f13-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42f13-124">Minimum supported client</span></span><br/> | <span data-ttu-id="42f13-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="42f13-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="42f13-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42f13-126">Minimum supported server</span></span><br/> | <span data-ttu-id="42f13-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="42f13-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="42f13-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42f13-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f13-129"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42f13-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f13-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="42f13-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f13-131">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="42f13-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="42f13-132">**WinBioEnumServiceProviders**</span><span class="sxs-lookup"><span data-stu-id="42f13-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





