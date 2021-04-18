---
description: Define informações de compartilhamento DDE. Isso geralmente é feito após a edição.
ms.assetid: 002c73ce-7b35-4e8e-bb7e-0e1393b97ccc
title: Função NDdeShareSetInfo (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareSetInfo
- NDdeShareSetInfoA
- NDdeShareSetInfoW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cee7660a58e8f2747a800650b79db20f95504f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761903"
---
# <a name="nddesharesetinfo-function"></a><span data-ttu-id="172d3-104">Função NDdeShareSetInfo</span><span class="sxs-lookup"><span data-stu-id="172d3-104">NDdeShareSetInfo function</span></span>

<span data-ttu-id="172d3-105">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="172d3-105">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="172d3-106">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="172d3-106">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="172d3-107">Define informações de compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="172d3-107">Sets DDE share information.</span></span> <span data-ttu-id="172d3-108">Isso geralmente é feito após a edição.</span><span class="sxs-lookup"><span data-stu-id="172d3-108">This is usually done after editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="172d3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="172d3-109">Syntax</span></span>


```C++
UINT NDdeShareSetInfo(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   nLevel,
  _In_ LPBYTE lpBuffer,
  _In_ DWORD  cBufSize,
  _In_ WORD   sParmNum
);
```



## <a name="parameters"></a><span data-ttu-id="172d3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="172d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="172d3-111">*lpszServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="172d3-111">*lpszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="172d3-112">O nome do servidor cujo DSDM deve ser modificado.</span><span class="sxs-lookup"><span data-stu-id="172d3-112">The name of the server whose DSDM is to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="172d3-113">*lpszShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="172d3-113">*lpszShareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="172d3-114">O nome do nome do compartilhamento cujas informações serão modificadas.</span><span class="sxs-lookup"><span data-stu-id="172d3-114">The name of the share name whose information is to be modified.</span></span> <span data-ttu-id="172d3-115">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="172d3-115">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="172d3-116">*nLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="172d3-116">*nLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="172d3-117">O nível de informações.</span><span class="sxs-lookup"><span data-stu-id="172d3-117">The information level.</span></span> <span data-ttu-id="172d3-118">Esse parâmetro deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="172d3-118">This parameter must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="172d3-119">*lpBuffer* \[in\]</span><span class="sxs-lookup"><span data-stu-id="172d3-119">*lpBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="172d3-120">Um ponteiro para a estrutura [**NDDESHAREINFO**](nddeshareinfo-str.md) que especifica as informações de compartilhamento DDE a serem armazenadas no DSDM.</span><span class="sxs-lookup"><span data-stu-id="172d3-120">A pointer to the [**NDDESHAREINFO**](nddeshareinfo-str.md) structure that specifies the DDE share information to be stored in the DSDM.</span></span> <span data-ttu-id="172d3-121">Atualmente, as informações de compartilhamento DDE são modificadas como um todo, ou seja, nenhuma edição parcial é feita.</span><span class="sxs-lookup"><span data-stu-id="172d3-121">Currently the DDE share information is modified as a whole, that is, no partial edits are made.</span></span> <span data-ttu-id="172d3-122">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="172d3-122">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="172d3-123">*cBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="172d3-123">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="172d3-124">O tamanho do buffer *lpBuffer* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="172d3-124">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="172d3-125">*sParmNum* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="172d3-125">*sParmNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="172d3-126">O índice de parâmetro a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="172d3-126">The parameter index to be modified.</span></span> <span data-ttu-id="172d3-127">A implementação atual não dá suporte à modificação parcial; Portanto, esse parâmetro deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="172d3-127">The current implementation does not support partial modification; therefore, this parameter must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="172d3-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="172d3-128">Return value</span></span>

<span data-ttu-id="172d3-129">Se a função for realizada com sucesso, o valor de retorno será NDDE \_ nenhum \_ erro.</span><span class="sxs-lookup"><span data-stu-id="172d3-129">If the function succeeds, the return value is NDDE\_NO\_ERROR.</span></span>

<span data-ttu-id="172d3-130">Se a função falhar, o valor de retorno será um código de erro, que pode ser convertido em uma mensagem de erro de texto chamando [**NDdeGetErrorString**](nddegeterrorstring.md).</span><span class="sxs-lookup"><span data-stu-id="172d3-130">If the function fails, the return value is an error code, which can be translated into a text error message by calling [**NDdeGetErrorString**](nddegeterrorstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="172d3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="172d3-131">Requirements</span></span>



| <span data-ttu-id="172d3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="172d3-132">Requirement</span></span> | <span data-ttu-id="172d3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="172d3-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="172d3-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="172d3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="172d3-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="172d3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="172d3-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="172d3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="172d3-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="172d3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="172d3-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="172d3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="172d3-139"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="172d3-139"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="172d3-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="172d3-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="172d3-141"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="172d3-141"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="172d3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="172d3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="172d3-143"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="172d3-143"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="172d3-144">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="172d3-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="172d3-145">**NDdeShareSetInfoW** (Unicode) e **NDdeShareSetInfoA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="172d3-145">**NDdeShareSetInfoW** (Unicode) and **NDdeShareSetInfoA** (ANSI)</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="172d3-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="172d3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="172d3-147">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="172d3-147">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="172d3-148">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="172d3-148">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="172d3-149">**NDDESHAREINFO**</span><span class="sxs-lookup"><span data-stu-id="172d3-149">**NDDESHAREINFO**</span></span>](nddeshareinfo-str.md)
</dt> <dt>

[<span data-ttu-id="172d3-150">**NDdeShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="172d3-150">**NDdeShareGetInfo**</span></span>](nddesharegetinfo.md)
</dt> </dl>

 

 




