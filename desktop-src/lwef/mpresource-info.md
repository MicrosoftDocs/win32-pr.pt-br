---
title: Estrutura de MPRESOURCE_INFO (MpClient. h)
description: Estrutura de informações do recurso.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPRESOURCE_INFO
- Ponteiro de estrutura de PMPRESOURCE_INFO recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918717"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="200d6-105">Estrutura de informações do MPRESOURCE \_</span><span class="sxs-lookup"><span data-stu-id="200d6-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="200d6-106">Estrutura de informações do recurso.</span><span class="sxs-lookup"><span data-stu-id="200d6-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="200d6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="200d6-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="200d6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="200d6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="200d6-109">**Esquema**</span><span class="sxs-lookup"><span data-stu-id="200d6-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="200d6-110">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="200d6-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="200d6-111">Identificador do esquema de recursos, como "arquivo" ou "dir".</span><span class="sxs-lookup"><span data-stu-id="200d6-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="200d6-112">**Caminho**</span><span class="sxs-lookup"><span data-stu-id="200d6-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="200d6-113">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="200d6-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="200d6-114">Caminho absoluto do recurso, com base no **esquema**.</span><span class="sxs-lookup"><span data-stu-id="200d6-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="200d6-115">**Classe**</span><span class="sxs-lookup"><span data-stu-id="200d6-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="200d6-116">Tipo: **\_ classe MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="200d6-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="200d6-117">Esse campo é definido quando o recurso é identificado como parte da ameaça.</span><span class="sxs-lookup"><span data-stu-id="200d6-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="200d6-118">Ele especifica a classe de recurso, principalmente concreta versus Lated.</span><span class="sxs-lookup"><span data-stu-id="200d6-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="200d6-119">Pode ser uma combinação desses valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="200d6-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="200d6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="200d6-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="200d6-121">Significado</span><span class="sxs-lookup"><span data-stu-id="200d6-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="200d6-122"><dt>**MP \_ 0x0000 de classe de recurso \_ \_ desconhecido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="200d6-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="200d6-123"><dt>**MP \_ Classe de recurso \_ \_ concreta**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="200d6-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="200d6-124">Mutuamente exclusivo com **classe de \_ recurso \_ MP \_ latence**.</span><span class="sxs-lookup"><span data-stu-id="200d6-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="200d6-125"><dt>**MP \_ Classe de recurso \_ \_ Lated**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="200d6-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="200d6-126">Mutuamente exclusivo com **classe de \_ recurso de MP \_ \_ concreta**.</span><span class="sxs-lookup"><span data-stu-id="200d6-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="200d6-127"><dt>**MP \_ \_Arquivo de \_ exemplo \_ de classe de recurso**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="200d6-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="200d6-128"><dt>**MP \_ 0x0100 \_ \_ compartilhado de classe de recurso**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="200d6-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="200d6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="200d6-129">Requirements</span></span>



| <span data-ttu-id="200d6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="200d6-130">Requirement</span></span> | <span data-ttu-id="200d6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="200d6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="200d6-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="200d6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="200d6-133">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="200d6-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="200d6-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="200d6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="200d6-135">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="200d6-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="200d6-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="200d6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="200d6-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="200d6-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





