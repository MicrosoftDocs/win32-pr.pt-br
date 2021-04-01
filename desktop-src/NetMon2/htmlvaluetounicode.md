---
description: A função HTMLValueToUnicode converte uma \_ cadeia de caracteres HTML CP UTF8 em uma cadeia de caracteres Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Função HTMLValueToUnicode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646791"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="93975-103">Função HTMLValueToUnicode</span><span class="sxs-lookup"><span data-stu-id="93975-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="93975-104">A função **HTMLValueToUnicode** converte uma \_ cadeia de caracteres HTML CP UTF8 em uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="93975-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="93975-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93975-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="93975-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93975-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93975-107">*valores* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="93975-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="93975-108">Na entrada, ponteiro para a cadeia de caracteres HTML fornecida pelo MCSVC.</span><span class="sxs-lookup"><span data-stu-id="93975-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="93975-109">Na saída, ponteiro para a cadeia de caracteres Unicode convertida.</span><span class="sxs-lookup"><span data-stu-id="93975-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93975-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93975-110">Return value</span></span>

<span data-ttu-id="93975-111">A função retorna o equivalente Unicode da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="93975-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="93975-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93975-112">Requirements</span></span>



| <span data-ttu-id="93975-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="93975-113">Requirement</span></span> | <span data-ttu-id="93975-114">Valor</span><span class="sxs-lookup"><span data-stu-id="93975-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93975-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93975-115">Minimum supported client</span></span><br/> | <span data-ttu-id="93975-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93975-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="93975-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93975-117">Minimum supported server</span></span><br/> | <span data-ttu-id="93975-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93975-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="93975-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="93975-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="93975-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="93975-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="93975-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93975-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="93975-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93975-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="93975-123">DLL</span><span class="sxs-lookup"><span data-stu-id="93975-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93975-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93975-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




