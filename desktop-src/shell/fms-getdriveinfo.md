---
description: Contém informações sobre a unidade selecionada na janela do Active File Manager (a janela de diretório ou a janela de resultados da pesquisa).
title: Estrutura de FMS_GETDRIVEINFO (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 14f8a90b-d0ed-4818-a719-8fc4ea617bef
ms.openlocfilehash: b19b54d89f74fa122effa5853beb2961e0ddf1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967937"
---
# <a name="fms_getdriveinfo-structure"></a><span data-ttu-id="44549-103">\_Estrutura GETdriveinfo do FMS</span><span class="sxs-lookup"><span data-stu-id="44549-103">FMS\_GETDRIVEINFO structure</span></span>

<span data-ttu-id="44549-104">Contém informações sobre a unidade selecionada na janela do Active File Manager (a janela de diretório ou a janela de resultados da pesquisa).</span><span class="sxs-lookup"><span data-stu-id="44549-104">Contains information about the drive selected in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="44549-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44549-105">Syntax</span></span>


```C++
typedef struct _FMS_GETDRIVEINFO {
  DWORD dwTotalSpace;
  DWORD dwFreeSpace;
  TCHAR szPath[260];
  TCHAR szVolume[14];
  TCHAR szShare[128];
} FMS_GETDRIVEINFO;
```



## <a name="members"></a><span data-ttu-id="44549-106">Membros</span><span class="sxs-lookup"><span data-stu-id="44549-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="44549-107">**dwTotalSpace**</span><span class="sxs-lookup"><span data-stu-id="44549-107">**dwTotalSpace**</span></span>
</dt> <dd>

<span data-ttu-id="44549-108">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="44549-108">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="44549-109">A quantidade total de espaço de armazenamento, em bytes, no disco associado à unidade.</span><span class="sxs-lookup"><span data-stu-id="44549-109">The total amount of storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="44549-110">**dwFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="44549-110">**dwFreeSpace**</span></span>
</dt> <dd>

<span data-ttu-id="44549-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="44549-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="44549-112">A quantidade de espaço de armazenamento livre, em bytes, no disco associado à unidade.</span><span class="sxs-lookup"><span data-stu-id="44549-112">The amount of free storage space, in bytes, on the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="44549-113">**szPath**</span><span class="sxs-lookup"><span data-stu-id="44549-113">**szPath**</span></span>
</dt> <dd>

<span data-ttu-id="44549-114">Tipo: **TCHAR \[ 260 \]**</span><span class="sxs-lookup"><span data-stu-id="44549-114">Type: **TCHAR\[260\]**</span></span>

</dd> <dd>

<span data-ttu-id="44549-115">o caminho de término nulo do diretório atual.</span><span class="sxs-lookup"><span data-stu-id="44549-115">the null-terminated path of the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="44549-116">**szVolume**</span><span class="sxs-lookup"><span data-stu-id="44549-116">**szVolume**</span></span>
</dt> <dd>

<span data-ttu-id="44549-117">Tipo: **TCHAR \[ 14 \]**</span><span class="sxs-lookup"><span data-stu-id="44549-117">Type: **TCHAR\[14\]**</span></span>

</dd> <dd>

<span data-ttu-id="44549-118">O rótulo de volume com terminação nula do disco associado à unidade.</span><span class="sxs-lookup"><span data-stu-id="44549-118">The null-terminated volume label of the disk associated with the drive.</span></span>

</dd> <dt>

<span data-ttu-id="44549-119">**szShare**</span><span class="sxs-lookup"><span data-stu-id="44549-119">**szShare**</span></span>
</dt> <dd>

<span data-ttu-id="44549-120">Tipo: **TCHAR \[ 128 \]**</span><span class="sxs-lookup"><span data-stu-id="44549-120">Type: **TCHAR\[128\]**</span></span>

</dd> <dd>

<span data-ttu-id="44549-121">O nome finalizado por nulo do recurso de rede (se a unidade estiver sendo acessada por meio de uma rede).</span><span class="sxs-lookup"><span data-stu-id="44549-121">The null-terminated name of the network resource (if the drive is being accessed through a network).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44549-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44549-122">Requirements</span></span>



| <span data-ttu-id="44549-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="44549-123">Requirement</span></span> | <span data-ttu-id="44549-124">Valor</span><span class="sxs-lookup"><span data-stu-id="44549-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="44549-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44549-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44549-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44549-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="44549-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44549-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44549-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44549-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="44549-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44549-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="44549-130"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="44549-130"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44549-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="44549-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44549-132">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="44549-132">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="44549-133">**FM \_ GETdriveinfo**</span><span class="sxs-lookup"><span data-stu-id="44549-133">**FM\_GETDRIVEINFO**</span></span>](fm-getdriveinfo.md)
</dt> </dl>

 

 




