---
description: Recupera informações de compartilhamento de DDE. Isso geralmente é feito para edição.
ms.assetid: a2e48a4d-2b72-40a3-b827-474da1db0910
title: Função NDdeShareGetInfo (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareGetInfo
- NDdeShareGetInfoA
- NDdeShareGetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 72dc9ae12b174555debfa21afac15e5bfbed993e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760421"
---
# <a name="nddesharegetinfo-function"></a><span data-ttu-id="39ede-104">Função NDdeShareGetInfo</span><span class="sxs-lookup"><span data-stu-id="39ede-104">NDdeShareGetInfo function</span></span>

<span data-ttu-id="39ede-105">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="39ede-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="39ede-106">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="39ede-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="39ede-107">Recupera informações de compartilhamento de DDE.</span><span class="sxs-lookup"><span data-stu-id="39ede-107">Retrieves DDE share information.</span></span> <span data-ttu-id="39ede-108">Isso geralmente é feito para edição.</span><span class="sxs-lookup"><span data-stu-id="39ede-108">This is usually done for editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ede-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39ede-109">Syntax</span></span>


```C++
UINT NDdeShareGetInfo(
  _In_  LPTSTR  lpszServer,
  _In_  LPTSTR  lpszShareName,
  _In_  UINT    nLevel,
  _Out_ LPBYTE  lpBuffer,
  _In_  DWORD   cBufSize,
  _Out_ LPDWORD lpnTotalAvailable,
  _In_  LPWORD  lpnItems
);
```



## <a name="parameters"></a><span data-ttu-id="39ede-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39ede-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ede-111">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39ede-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-112">O nome do servidor no qual o DSDM reside.</span><span class="sxs-lookup"><span data-stu-id="39ede-112">The name of the server on which the DSDM resides.</span></span>

</dd> <dt>

<span data-ttu-id="39ede-113">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39ede-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-114">O nome do compartilhamento cujas informações serão recuperadas do DSDM.</span><span class="sxs-lookup"><span data-stu-id="39ede-114">The share name whose information is to be retrieved from the DSDM.</span></span> <span data-ttu-id="39ede-115">Esse parâmetro não deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="39ede-115">This parameter must not be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39ede-116">*nLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39ede-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-117">O nível de informações.</span><span class="sxs-lookup"><span data-stu-id="39ede-117">The information level.</span></span> <span data-ttu-id="39ede-118">Esse parâmetro deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="39ede-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="39ede-119">*lpBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="39ede-119">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-120">Um ponteiro para um buffer que recebe a estrutura [**NDDESHAREINFO**](nddeshareinfo-str.md) e os dados associados apontados por seus membros.</span><span class="sxs-lookup"><span data-stu-id="39ede-120">A pointer to a buffer that receives the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure and associated data pointed to by its members.</span></span> <span data-ttu-id="39ede-121">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="39ede-121">This parameter can be **NULL**.</span></span> <span data-ttu-id="39ede-122">Se *lpBuffer* for **NULL**, o DSDM calculará o número de bytes necessários para armazenar as informações de compartilhamento solicitadas e retornará esse valor no campo *LPNTOTALAVAILABLE* junto com o \_ erro NDDE \_ buf muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="39ede-122">If *lpBuffer* is **NULL**, then the DSDM calculates the number of bytes required to store the requested share information and returns that value in the *lpnTotalAvailable* field along with the NDDE\_BUF\_TOO\_SMALL error.</span></span>

</dd> <dt>

<span data-ttu-id="39ede-123">*cBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39ede-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-124">O tamanho do buffer *lpBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="39ede-124">The size of the *lpBuffer* buffer, in bytes.</span></span> <span data-ttu-id="39ede-125">Se *lpBuffer* for **NULL**, *cBufSize* deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="39ede-125">If *lpBuffer* is **NULL**, then *cBufSize* should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="39ede-126">*lpnTotalAvailable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="39ede-126">*lpnTotalAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-127">Um ponteiro para uma variável que recebe o número total de bytes necessários para armazenar as informações de compartilhamento solicitadas.</span><span class="sxs-lookup"><span data-stu-id="39ede-127">A pointer to a variable that receives the total number of bytes needed to store the requested share information.</span></span> <span data-ttu-id="39ede-128">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="39ede-128">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="39ede-129">*lpnItems* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39ede-129">*lpnItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39ede-130">Um ponteiro para uma máscara de seleção de item para recuperação de informações de compartilhamento parcial.</span><span class="sxs-lookup"><span data-stu-id="39ede-130">A pointer to an item selection mask for partial share information retrieval.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ede-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39ede-131">Return value</span></span>

<span data-ttu-id="39ede-132">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="39ede-132">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="39ede-133">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="39ede-133">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span> <span data-ttu-id="39ede-134">Se o parâmetro *lpBuffer* for **NULL**, ele retornará NDDE \_ buf \_ muito \_ pequeno.</span><span class="sxs-lookup"><span data-stu-id="39ede-134">If the *lpBuffer* parameter is **NULL**, it returns NDDE\_BUF\_TOO\_SMALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ede-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39ede-135">Requirements</span></span>



| <span data-ttu-id="39ede-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="39ede-136">Requirement</span></span> | <span data-ttu-id="39ede-137">Valor</span><span class="sxs-lookup"><span data-stu-id="39ede-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="39ede-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39ede-138">Minimum supported client</span></span><br/> | <span data-ttu-id="39ede-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39ede-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="39ede-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39ede-140">Minimum supported server</span></span><br/> | <span data-ttu-id="39ede-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39ede-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="39ede-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39ede-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ede-143"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ede-143"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="39ede-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39ede-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="39ede-145"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39ede-145"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="39ede-146">DLL</span><span class="sxs-lookup"><span data-stu-id="39ede-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39ede-147"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ede-147"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="39ede-148">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="39ede-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39ede-149">**NDdeShareGetInfoW** (Unicode) e **NDdeShareGetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="39ede-149">**NDdeShareGetInfoW** (Unicode) and **NDdeShareGetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="39ede-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="39ede-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ede-151">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="39ede-151">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="39ede-152">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="39ede-152">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="39ede-153">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="39ede-153">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="39ede-154">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="39ede-154">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> </dl>

 

 




