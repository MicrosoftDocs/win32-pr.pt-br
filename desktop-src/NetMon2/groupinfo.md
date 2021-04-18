---
description: Associa um nome de grupo e seu identificador.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Estrutura GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787483"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="1b050-103">Estrutura GROUPINFO</span><span class="sxs-lookup"><span data-stu-id="1b050-103">GROUPINFO structure</span></span>

<span data-ttu-id="1b050-104">A estrutura **GROUPINFO** associa um nome de grupo e seu identificador.</span><span class="sxs-lookup"><span data-stu-id="1b050-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b050-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b050-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="1b050-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1b050-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b050-107">**szGroupName**</span><span class="sxs-lookup"><span data-stu-id="1b050-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="1b050-108">Valor incrementado de uma matriz na estrutura **GroupName** .</span><span class="sxs-lookup"><span data-stu-id="1b050-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1b050-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="1b050-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="1b050-110">Identificador para um grupo.</span><span class="sxs-lookup"><span data-stu-id="1b050-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b050-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b050-111">Requirements</span></span>



| <span data-ttu-id="1b050-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b050-112">Requirement</span></span> | <span data-ttu-id="1b050-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1b050-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1b050-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b050-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1b050-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1b050-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1b050-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b050-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1b050-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1b050-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1b050-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1b050-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b050-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b050-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




