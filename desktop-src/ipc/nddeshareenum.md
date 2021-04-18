---
description: Recupera a lista de compartilhamentos DDE disponíveis.
ms.assetid: ce5aeddd-d9d1-40a2-a807-1a9c9f98f171
title: Função NDdeShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareEnum
- NDdeShareEnumA
- NDdeShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8bfa4884b88e72cb9a3b64bebf58af53cdc1047e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784501"
---
# <a name="nddeshareenum-function"></a><span data-ttu-id="e9ee1-103">Função NDdeShareEnum</span><span class="sxs-lookup"><span data-stu-id="e9ee1-103">NDdeShareEnum function</span></span>

<span data-ttu-id="e9ee1-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="e9ee1-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="e9ee1-106">Recupera a lista de compartilhamentos DDE disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-106">Retrieves the list of available DDE shares.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ee1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9ee1-107">Syntax</span></span>


```C++
UINT NDdeShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="e9ee1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9ee1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ee1-109">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ee1-110">O nome do servidor no qual o DSDM reside.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee1-111">*nLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ee1-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-112">Reserved.</span></span> <span data-ttu-id="e9ee1-113">Esse parâmetro deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee1-114">*lpBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ee1-115">Um ponteiro para um buffer que recebe a lista de compartilhamentos de DDE.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-115">A pointer to a buffer that receives the list of DDE shares.</span></span> <span data-ttu-id="e9ee1-116">A lista de compartilhamentos DDE é armazenada como uma sequência de cadeias de caracteres separadas por nulo terminando com um caractere nulo duplo no final.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-116">The list of DDE shares is stored as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="e9ee1-117">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="e9ee1-118">Se *lpBuffer* for **NULL**, o DSDM retornará o tamanho do buffer necessário para manter a lista de compartilhamentos no parâmetro *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="e9ee1-118">If *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee1-119">*cBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ee1-120">O tamanho do buffer *lpBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="e9ee1-121">Esse parâmetro deve ser zero se *lpBuffer* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee1-122">*lpnEntriesRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ee1-123">Um ponteiro para uma variável que recebe o número total de compartilhamentos sendo enumerados.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-123">A pointer to a variable that receives the total number of shares being enumerated.</span></span> <span data-ttu-id="e9ee1-124">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e9ee1-125">*lpcbTotalAvailable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9ee1-126">Um ponteiro para uma variável que recebe o número total de bytes necessários no buffer para armazenar a lista de compartilhamentos de DDE.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-126">A pointer to a variable that receives the total number of bytes needed in the buffer to store the list of DDE shares.</span></span> <span data-ttu-id="e9ee1-127">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9ee1-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e9ee1-128">Return value</span></span>

<span data-ttu-id="e9ee1-129">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="e9ee1-130">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="e9ee1-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="e9ee1-131">Se o parâmetro *lpBuffer* for **NULL**, ele retornará NDDE \_ buf \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="e9ee1-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ee1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ee1-132">Requirements</span></span>



| <span data-ttu-id="e9ee1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ee1-133">Requirement</span></span> | <span data-ttu-id="e9ee1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ee1-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ee1-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ee1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e9ee1-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e9ee1-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e9ee1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e9ee1-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e9ee1-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e9ee1-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e9ee1-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9ee1-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9ee1-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9ee1-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9ee1-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9ee1-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9ee1-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e9ee1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e9ee1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9ee1-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9ee1-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9ee1-145">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e9ee1-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9ee1-146">**NDdeShareEnumW** (Unicode) e **NDdeShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e9ee1-146">**NDdeShareEnumW** (Unicode) and **NDdeShareEnumA** (ANSI)</span></span><br/>                  |



## <a name="see-also"></a><span data-ttu-id="e9ee1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9ee1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ee1-148">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="e9ee1-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="e9ee1-149">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="e9ee1-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




