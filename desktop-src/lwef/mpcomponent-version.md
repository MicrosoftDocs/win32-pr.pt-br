---
title: Estrutura de MPCOMPONENT_VERSION (MpClient. h)
description: Versão e tempo de atualização para um componente individual.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCOMPONENT_VERSION
- Ponteiro de estrutura de PMPCOMPONENT_VERSION recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918395"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="81599-105">Estrutura de versão do MPCOMPONENT \_</span><span class="sxs-lookup"><span data-stu-id="81599-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="81599-106">Versão e tempo de atualização para um componente individual.</span><span class="sxs-lookup"><span data-stu-id="81599-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="81599-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81599-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="81599-108">Membros</span><span class="sxs-lookup"><span data-stu-id="81599-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="81599-109">**Versão**</span><span class="sxs-lookup"><span data-stu-id="81599-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="81599-110">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="81599-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="81599-111">Campo de versão.</span><span class="sxs-lookup"><span data-stu-id="81599-111">Version field.</span></span> <span data-ttu-id="81599-112">Cada **palavra** representa principal, secundária, compilação e revisão.</span><span class="sxs-lookup"><span data-stu-id="81599-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="81599-113">**UpdateTime**</span><span class="sxs-lookup"><span data-stu-id="81599-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="81599-114">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="81599-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="81599-115">Hora da última atualização do componente, no formato **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="81599-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81599-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81599-116">Requirements</span></span>



| <span data-ttu-id="81599-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81599-117">Requirement</span></span> | <span data-ttu-id="81599-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81599-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81599-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81599-119">Minimum supported client</span></span><br/> | <span data-ttu-id="81599-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="81599-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="81599-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81599-121">Minimum supported server</span></span><br/> | <span data-ttu-id="81599-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="81599-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81599-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81599-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="81599-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="81599-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





