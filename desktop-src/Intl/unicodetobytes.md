---
UID: ''
title: Função UnicodeToBytes
description: Converte caracteres Unicode em bytes GB18030.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "103639053"
---
# <a name="unicodetobytes-function"></a><span data-ttu-id="88614-103">Função UnicodeToBytes</span><span class="sxs-lookup"><span data-stu-id="88614-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="88614-104">Description</span><span class="sxs-lookup"><span data-stu-id="88614-104">Description</span></span>

<span data-ttu-id="88614-105">Preterido.</span><span class="sxs-lookup"><span data-stu-id="88614-105">Deprecated.</span></span> <span data-ttu-id="88614-106">Converte caracteres Unicode em bytes GB18030.</span><span class="sxs-lookup"><span data-stu-id="88614-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="88614-107">**Observação**  Ao converter caracteres Unicode em bytes do GB18030, um aplicativo a ser executado no Windows Vista e posterior deve usar a função [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .</span><span class="sxs-lookup"><span data-stu-id="88614-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="88614-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88614-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="88614-109">lpWideCharStr [in]</span><span class="sxs-lookup"><span data-stu-id="88614-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="88614-110">Ponteiro para a cadeia de caracteres Unicode a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="88614-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="88614-111">cchWideChar [in]</span><span class="sxs-lookup"><span data-stu-id="88614-111">cchWideChar [in]</span></span>

<span data-ttu-id="88614-112">Contagem de caracteres da cadeia de caracteres Unicode a ser convertida.</span><span class="sxs-lookup"><span data-stu-id="88614-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="88614-113">lpMultiByteStr [in]</span><span class="sxs-lookup"><span data-stu-id="88614-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="88614-114">Ponteiro para o buffer de multibyte de destino.</span><span class="sxs-lookup"><span data-stu-id="88614-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="88614-115">Se *lpMultiByteStr* for 0, a contagem de bytes do resultado GB18030 será retornada e nenhuma conversão será feita.</span><span class="sxs-lookup"><span data-stu-id="88614-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="88614-116">cchMultiByte [in]</span><span class="sxs-lookup"><span data-stu-id="88614-116">cchMultiByte [in]</span></span>

<span data-ttu-id="88614-117">Contagem de bytes do buffer de multibyte de destino.</span><span class="sxs-lookup"><span data-stu-id="88614-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="88614-118">Se *cchMultiByte* for 0, a contagem de bytes do resultado GB18030 será retornada e nenhuma conversão será feita.</span><span class="sxs-lookup"><span data-stu-id="88614-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="88614-119">Retornos</span><span class="sxs-lookup"><span data-stu-id="88614-119">Returns</span></span>

<span data-ttu-id="88614-120">Retorna a contagem de bytes dos caracteres multibyte gerados, se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="88614-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="88614-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="88614-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="88614-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="88614-122">See also</span></span>

[<span data-ttu-id="88614-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="88614-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="88614-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="88614-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
