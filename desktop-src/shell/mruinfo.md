---
description: Contém informações que definem uma nova lista de MRU (usados mais recentemente). Usado por CreateMRUListW.
title: Estrutura MRUINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 652168e6a4e61ac754aac3202e0681ec6b7d9e66
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840757"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="90606-104">Estrutura MRUINFO</span><span class="sxs-lookup"><span data-stu-id="90606-104">MRUINFO structure</span></span>

<span data-ttu-id="90606-105">Contém informações que definem uma nova lista de MRU (usados mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="90606-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="90606-106">Usado por [**CreateMRUListW.**](createmrulist.md)</span><span class="sxs-lookup"><span data-stu-id="90606-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="90606-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90606-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="90606-108">Membros</span><span class="sxs-lookup"><span data-stu-id="90606-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="90606-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="90606-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="90606-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90606-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90606-111">O tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="90606-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="90606-112">**Umax**</span><span class="sxs-lookup"><span data-stu-id="90606-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="90606-113">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="90606-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="90606-114">O número máximo de entradas na lista mru.</span><span class="sxs-lookup"><span data-stu-id="90606-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="90606-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="90606-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="90606-116">Tipo: **UINT**</span><span class="sxs-lookup"><span data-stu-id="90606-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="90606-117">Um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="90606-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="90606-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_ BINARY** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="90606-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="90606-119">Os dados são armazenados no Registro como dados binários em vez de dados de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90606-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="90606-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_ CACHEWRITE** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="90606-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="90606-121">Gravar alterações na versão do MRU armazenada no Registro somente quando um novo item for adicionado ou os recursos da lista mru são liberados da memória.</span><span class="sxs-lookup"><span data-stu-id="90606-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="90606-122">Observe que a versão ativa do MRU na memória é atualizada imediatamente em resposta a qualquer alteração no conteúdo ou na ordenação.</span><span class="sxs-lookup"><span data-stu-id="90606-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="90606-123">**Hkey**</span><span class="sxs-lookup"><span data-stu-id="90606-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="90606-124">Tipo: **HKEY**</span><span class="sxs-lookup"><span data-stu-id="90606-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="90606-125">Um identificador para a chave aberta no momento ou um dos seguintes valores predefinidos sob os quais armazenar os dados MRU.</span><span class="sxs-lookup"><span data-stu-id="90606-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="90606-126">**HKEY \_ Current \_ User**</span><span class="sxs-lookup"><span data-stu-id="90606-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="90606-127">**\_máquina local \_ HKEY**</span><span class="sxs-lookup"><span data-stu-id="90606-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="90606-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="90606-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="90606-129">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="90606-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="90606-130">A subchave sob a qual armazenar os dados MRU.</span><span class="sxs-lookup"><span data-stu-id="90606-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="90606-131">**lpfnCompare**</span><span class="sxs-lookup"><span data-stu-id="90606-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="90606-132">Tipo: **[ **MRUCMPPROC**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="90606-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="90606-133">Um ponteiro para uma função de comparação de dados opcional que pode ser usada para determinar se um item está presente na lista de MRU.</span><span class="sxs-lookup"><span data-stu-id="90606-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="90606-134">Isso é útil quando a lista MRU foi criada com o **sinalizador \_ binário MRU** .</span><span class="sxs-lookup"><span data-stu-id="90606-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="90606-135">Se esse membro for **nulo**, as funções de comparação de cadeia de caracteres padrão serão usadas; para dados binários, é usada uma comparação de memória direta.</span><span class="sxs-lookup"><span data-stu-id="90606-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90606-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="90606-136">Remarks</span></span>

<span data-ttu-id="90606-137">Essa estrutura não está definida em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="90606-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="90606-138">Você mesmo deve defini-lo.</span><span class="sxs-lookup"><span data-stu-id="90606-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="90606-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90606-139">Requirements</span></span>



| <span data-ttu-id="90606-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="90606-140">Requirement</span></span> | <span data-ttu-id="90606-141">Valor</span><span class="sxs-lookup"><span data-stu-id="90606-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90606-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90606-142">Minimum supported client</span></span><br/> | <span data-ttu-id="90606-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90606-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90606-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90606-144">Minimum supported server</span></span><br/> | <span data-ttu-id="90606-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90606-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="90606-146">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="90606-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="90606-147">**MRUINFOW** (Unicode) e **MRUINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="90606-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




