---
title: Estrutura de WINBIO_VERSION (WinBio \_ Types. h)
description: Contém o número de versão do software de um componente do provedor de serviços biométrico.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_VERSION
- Ponteiro de estrutura de PWINBIO_VERSION Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455949"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="a546e-105">Estrutura de versão do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="a546e-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="a546e-106">A estrutura de **\_ versão do WINBIO** contém o número de versão do software de um componente do provedor de serviços biométricos.</span><span class="sxs-lookup"><span data-stu-id="a546e-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="a546e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a546e-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="a546e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a546e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a546e-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="a546e-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a546e-110">Um **DWORD** que contém o número de versão principal.</span><span class="sxs-lookup"><span data-stu-id="a546e-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="a546e-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="a546e-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a546e-112">Um **DWORD** que contém o número de versão secundária.</span><span class="sxs-lookup"><span data-stu-id="a546e-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a546e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a546e-113">Requirements</span></span>



| <span data-ttu-id="a546e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a546e-114">Requirement</span></span> | <span data-ttu-id="a546e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a546e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a546e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a546e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a546e-117">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a546e-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a546e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a546e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a546e-119">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a546e-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a546e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a546e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a546e-121"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a546e-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a546e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a546e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a546e-123">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="a546e-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="a546e-124">**\_esquema WINBIO BSP \_**</span><span class="sxs-lookup"><span data-stu-id="a546e-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="a546e-125">**\_esquema de unidade WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a546e-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





