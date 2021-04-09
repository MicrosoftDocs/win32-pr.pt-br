---
description: Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado.
ms.assetid: 7077e3bc-df6e-401b-9ac7-15144b79af96
title: Função NDdeGetErrorString (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeGetErrorString
- NDdeGetErrorStringA
- NDdeGetErrorStringW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 8e043c8281d3ad049346ac7ce68991eb6bd08af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010351"
---
# <a name="nddegeterrorstring-function"></a><span data-ttu-id="b603b-103">Função NDdeGetErrorString</span><span class="sxs-lookup"><span data-stu-id="b603b-103">NDdeGetErrorString function</span></span>

<span data-ttu-id="b603b-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="b603b-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="b603b-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="b603b-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="b603b-106">Converte um código de erro retornado por uma função DDE de rede em uma cadeia de caracteres de erro que explica o código de erro retornado.</span><span class="sxs-lookup"><span data-stu-id="b603b-106">Converts an error code returned by a network DDE function into an error string that explains the returned error code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b603b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b603b-107">Syntax</span></span>


```C++
UINT NDdeGetErrorString(
  _In_  UINT   uErrorCode,
  _Out_ LPTSTR lpszErrorString,
  _In_  DWORD  cBufSize
);
```



## <a name="parameters"></a><span data-ttu-id="b603b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b603b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b603b-109">*uErrorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b603b-109">*uErrorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b603b-110">O código de erro a ser convertido em uma cadeia de caracteres de erro.</span><span class="sxs-lookup"><span data-stu-id="b603b-110">The error code to be converted into an error string.</span></span>

</dd> <dt>

<span data-ttu-id="b603b-111">*lpszErrorString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b603b-111">*lpszErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b603b-112">Um ponteiro para um buffer que recebe a cadeia de caracteres de erro traduzida.</span><span class="sxs-lookup"><span data-stu-id="b603b-112">A pointer to a buffer that receives the translated error string.</span></span> <span data-ttu-id="b603b-113">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b603b-113">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="b603b-114">Se o buffer não for grande o suficiente para armazenar a cadeia de caracteres de erro completa, a cadeia de caracteres será truncada.</span><span class="sxs-lookup"><span data-stu-id="b603b-114">If the buffer is not large enough to store the complete error string, the string is truncated.</span></span>

</dd> <dt>

<span data-ttu-id="b603b-115">*cBufSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b603b-115">*cBufSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b603b-116">O tamanho do buffer para receber a cadeia de caracteres de erro, em **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="b603b-116">The size of the buffer to receive the error string, in **TCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b603b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b603b-117">Return value</span></span>

<span data-ttu-id="b603b-118">Se a função obtiver êxito, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="b603b-118">If the function succeeds, the return value is zero.</span></span>

<span data-ttu-id="b603b-119">Se a função falhar, o valor de retorno será um código de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b603b-119">If the function fails, the return value is a nonzero error code.</span></span> <span data-ttu-id="b603b-120">Se o buffer *lpszErrorString* não for grande o suficiente para aceitar a cadeia de caracteres de erro completa e a cadeia de caracteres estiver truncada, a função retornará o valor NDDE \_ \_ erro interno.</span><span class="sxs-lookup"><span data-stu-id="b603b-120">If the *lpszErrorString* buffer is not large enough to accept the complete error string, and the string is truncated, the function returns the value NDDE\_INTERNAL\_ERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="b603b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b603b-121">Requirements</span></span>



| <span data-ttu-id="b603b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b603b-122">Requirement</span></span> | <span data-ttu-id="b603b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b603b-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b603b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b603b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b603b-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b603b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b603b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b603b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b603b-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b603b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b603b-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b603b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b603b-129"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b603b-129"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="b603b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b603b-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b603b-131"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b603b-131"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b603b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b603b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b603b-133"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b603b-133"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="b603b-134">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b603b-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b603b-135">**NDdeGetErrorStringW** (Unicode) e **NDdeGetErrorStringA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b603b-135">**NDdeGetErrorStringW** (Unicode) and **NDdeGetErrorStringA** (ANSI)</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="b603b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b603b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b603b-137">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="b603b-137">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="b603b-138">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="b603b-138">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> </dl>

 

 




