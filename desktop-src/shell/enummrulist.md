---
description: Enumera o conteúdo da lista MRU (usada mais recentemente). Opcionalmente, recupera um item da enumeração.
title: Função EnumMRUListW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829704"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="84f3a-104">Função EnumMRUListW</span><span class="sxs-lookup"><span data-stu-id="84f3a-104">EnumMRUListW function</span></span>

<span data-ttu-id="84f3a-105">\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84f3a-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="84f3a-106">Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="84f3a-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="84f3a-107">\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-107">\]</span></span>

<span data-ttu-id="84f3a-108">Enumera o conteúdo da lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="84f3a-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="84f3a-109">Opcionalmente, recupera um item da enumeração.</span><span class="sxs-lookup"><span data-stu-id="84f3a-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f3a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84f3a-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="84f3a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84f3a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84f3a-112">*hMRU* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f3a-113">Tipo: **identificador**</span><span class="sxs-lookup"><span data-stu-id="84f3a-113">Type: **HANDLE**</span></span>

<span data-ttu-id="84f3a-114">O identificador da lista MRU, obtido quando a lista foi criada.</span><span class="sxs-lookup"><span data-stu-id="84f3a-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="84f3a-115">*nItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f3a-116">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="84f3a-116">Type: **int**</span></span>

<span data-ttu-id="84f3a-117">O item a ser retornado.</span><span class="sxs-lookup"><span data-stu-id="84f3a-117">The item to return.</span></span> <span data-ttu-id="84f3a-118">Se esse valor for menor que 0, a função retornará o número de itens na lista MRU.</span><span class="sxs-lookup"><span data-stu-id="84f3a-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="84f3a-119">*lpData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84f3a-120">Tipo: \**void \** _</span><span class="sxs-lookup"><span data-stu-id="84f3a-120">Type: \**void\** _</span></span>

<span data-ttu-id="84f3a-121">Um ponteiro para um buffer que recebe o item solicitado em _nItem \*.</span><span class="sxs-lookup"><span data-stu-id="84f3a-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="84f3a-122">Se *nItem* for menor que 0, o conteúdo desse buffer não será alterado.</span><span class="sxs-lookup"><span data-stu-id="84f3a-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="84f3a-123">*uLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84f3a-124">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="84f3a-124">Type: **UINT**</span></span>

<span data-ttu-id="84f3a-125">O tamanho do buffer, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="84f3a-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="84f3a-126">Se a lista MRU foi criada com o **sinalizador \_ binário MRU** , esse é o tamanho em bytes.</span><span class="sxs-lookup"><span data-stu-id="84f3a-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="84f3a-127">Caso contrário, é o tamanho em caracteres.</span><span class="sxs-lookup"><span data-stu-id="84f3a-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84f3a-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84f3a-128">Return value</span></span>

<span data-ttu-id="84f3a-129">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="84f3a-129">Type: **int**</span></span>

<span data-ttu-id="84f3a-130">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="84f3a-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="84f3a-131">Retorna o número de itens na enumeração, se *nItem* for menor que 0.</span><span class="sxs-lookup"><span data-stu-id="84f3a-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="84f3a-132">Retornará-1 se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="84f3a-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="84f3a-133">Caso contrário, retorna o tamanho da cadeia de caracteres retornada em *lpData*, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="84f3a-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="84f3a-134">Se a lista MRU foi criada com o **sinalizador \_ binário MRU** , esse é o tamanho em bytes.</span><span class="sxs-lookup"><span data-stu-id="84f3a-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="84f3a-135">Caso contrário, é o tamanho em caracteres.</span><span class="sxs-lookup"><span data-stu-id="84f3a-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="84f3a-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="84f3a-136">Remarks</span></span>

<span data-ttu-id="84f3a-137">Essa função não está incluída em um cabeçalho ou biblioteca pública.</span><span class="sxs-lookup"><span data-stu-id="84f3a-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="84f3a-138">Ele pode ser acessado por meio de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extraído de comctl32.dll por seu ordinal, que é 403 para **EnumMRUListW**.</span><span class="sxs-lookup"><span data-stu-id="84f3a-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f3a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84f3a-139">Requirements</span></span>



| <span data-ttu-id="84f3a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="84f3a-140">Requirement</span></span> | <span data-ttu-id="84f3a-141">Valor</span><span class="sxs-lookup"><span data-stu-id="84f3a-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84f3a-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f3a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="84f3a-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="84f3a-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84f3a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="84f3a-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="84f3a-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84f3a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="84f3a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84f3a-147"><dt>Comctl32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="84f3a-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="84f3a-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="84f3a-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="84f3a-149">**EnumMRUListW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="84f3a-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="84f3a-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="84f3a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f3a-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="84f3a-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="84f3a-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="84f3a-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
