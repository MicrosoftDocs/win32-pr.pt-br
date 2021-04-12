---
description: Recupera os nomes de todos os compartilhamentos de DDE de rede que são confiáveis no contexto do processo de chamada.
ms.assetid: 8e2323a4-0c27-44e6-9598-08a3c1a88bd3
title: Função NDdeTrustedShareEnum (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeTrustedShareEnum
- NDdeTrustedShareEnumA
- NDdeTrustedShareEnumW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: caa3f7c20b95243e03c0c6025d1ff32d60443ab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297298"
---
# <a name="nddetrustedshareenum-function"></a><span data-ttu-id="10b02-103">Função NDdeTrustedShareEnum</span><span class="sxs-lookup"><span data-stu-id="10b02-103">NDdeTrustedShareEnum function</span></span>

<span data-ttu-id="10b02-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="10b02-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="10b02-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="10b02-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="10b02-106">Recupera os nomes de todos os compartilhamentos de DDE de rede que são confiáveis no contexto do processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="10b02-106">Retrieves the names of all network DDE shares that are trusted in the context of the calling process.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b02-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10b02-107">Syntax</span></span>


```C++
UINT NDdeTrustedShareEnum(
  _In_  LPTSTR  lpszServer,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnEntriesRead,
  _Out_ LPDWORD lpcbTotalAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="10b02-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10b02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b02-109">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10b02-109">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b02-110">O nome do servidor no qual o DSDM reside.</span><span class="sxs-lookup"><span data-stu-id="10b02-110">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="10b02-111">*nLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10b02-111">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b02-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="10b02-112">Reserved.</span></span> <span data-ttu-id="10b02-113">Esse parâmetro deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="10b02-113">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="10b02-114">*lpBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10b02-114">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10b02-115">Um ponteiro para um buffer que recebe a lista de compartilhamentos DDE confiáveis.</span><span class="sxs-lookup"><span data-stu-id="10b02-115">A pointer to a buffer that receives the list of trusted DDE shares.</span></span> <span data-ttu-id="10b02-116">A lista de compartilhamentos DDE confiáveis é retornada como uma sequência de cadeias de caracteres separadas por nulo terminando com um caractere nulo duplo no final.</span><span class="sxs-lookup"><span data-stu-id="10b02-116">The list of trusted DDE shares is returned as a sequence of null-separated strings terminating with a double null character at the end.</span></span> <span data-ttu-id="10b02-117">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="10b02-117">This parameter can be **NULL**.</span></span> <span data-ttu-id="10b02-118">Se o *lpBuffer* for **nulo**, o DSDM retornará o tamanho do buffer necessário para manter a lista de compartilhamentos no campo *lpcbTotalAvailable* .</span><span class="sxs-lookup"><span data-stu-id="10b02-118">If the *lpBuffer* is **NULL**, the DSDM returns the size of buffer required to hold the list of shares in the *lpcbTotalAvailable* field.</span></span>

</dd> <dt>

<span data-ttu-id="10b02-119">*cBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="10b02-119">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10b02-120">O tamanho do buffer *lpBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="10b02-120">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="10b02-121">Esse parâmetro deve ser zero se *lpBuffer* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="10b02-121">This parameter must be zero if *lpBuffer* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10b02-122">*lpnEntriesRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10b02-122">*lpnEntriesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10b02-123">Um ponteiro para uma variável que recebe o número total de compartilhamentos confiáveis sendo enumerados.</span><span class="sxs-lookup"><span data-stu-id="10b02-123">A pointer to a variable that receives the total number of trusted shares being enumerated.</span></span> <span data-ttu-id="10b02-124">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="10b02-124">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10b02-125">*lpcbTotalAvailable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10b02-125">*lpcbTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10b02-126">Um ponteiro para uma variável que recebe o número total de bytes necessários para armazenar a lista de compartilhamentos DDE confiáveis.</span><span class="sxs-lookup"><span data-stu-id="10b02-126">A pointer to a variable that receives the total number of bytes needed to store the list of trusted DDE shares.</span></span> <span data-ttu-id="10b02-127">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="10b02-127">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b02-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10b02-128">Return value</span></span>

<span data-ttu-id="10b02-129">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="10b02-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="10b02-130">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="10b02-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="10b02-131">Se o parâmetro *lpBuffer* for **NULL**, ele retornará NDDE \_ buf \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="10b02-131">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b02-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10b02-132">Requirements</span></span>



| <span data-ttu-id="10b02-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b02-133">Requirement</span></span> | <span data-ttu-id="10b02-134">Valor</span><span class="sxs-lookup"><span data-stu-id="10b02-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10b02-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10b02-135">Minimum supported client</span></span><br/> | <span data-ttu-id="10b02-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10b02-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="10b02-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10b02-137">Minimum supported server</span></span><br/> | <span data-ttu-id="10b02-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="10b02-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="10b02-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="10b02-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b02-140"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b02-140"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="10b02-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="10b02-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="10b02-142"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10b02-142"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="10b02-143">DLL</span><span class="sxs-lookup"><span data-stu-id="10b02-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10b02-144"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10b02-144"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="10b02-145">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="10b02-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="10b02-146">**NDdeTrustedShareEnumW** (Unicode) e **NDdeTrustedShareEnumA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="10b02-146">**NDdeTrustedShareEnumW** (Unicode) and **NDdeTrustedShareEnumA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="10b02-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="10b02-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b02-148">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="10b02-148">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="10b02-149">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="10b02-149">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




