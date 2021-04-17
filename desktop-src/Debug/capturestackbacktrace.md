---
UID: ''
title: Função CaptureStackBackTrace
description: Captura um rastreamento regressivo de pilha percorrendo a pilha.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2020
ms.locfileid: "105749659"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="74f36-103">Função CaptureStackBackTrace</span><span class="sxs-lookup"><span data-stu-id="74f36-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="74f36-104">Description</span><span class="sxs-lookup"><span data-stu-id="74f36-104">Description</span></span>

<span data-ttu-id="74f36-105">Captura um rastreamento regressivo de pilha percorrendo a pilha e registrando as informações de cada quadro.</span><span class="sxs-lookup"><span data-stu-id="74f36-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="74f36-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74f36-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="74f36-107">FramesToSkip [in]</span><span class="sxs-lookup"><span data-stu-id="74f36-107">FramesToSkip [in]</span></span>

<span data-ttu-id="74f36-108">O número de quadros a serem ignorados desde o início do rastreamento de fundo.</span><span class="sxs-lookup"><span data-stu-id="74f36-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="74f36-109">FramesToCapture [in]</span><span class="sxs-lookup"><span data-stu-id="74f36-109">FramesToCapture [in]</span></span>

<span data-ttu-id="74f36-110">O número de quadros a serem capturados.</span><span class="sxs-lookup"><span data-stu-id="74f36-110">The number of frames to be captured.</span></span>
<span data-ttu-id="74f36-111">Você pode capturar até quadros de **MAXUSHORT** .</span><span class="sxs-lookup"><span data-stu-id="74f36-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="74f36-112">**Windows Server 2003 e Windows XP:**  A soma dos parâmetros *FramesToSkip* e *FramesToCapture* deve ser menor que 63.</span><span class="sxs-lookup"><span data-stu-id="74f36-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="74f36-113">Backtrace [saída]</span><span class="sxs-lookup"><span data-stu-id="74f36-113">BackTrace [out]</span></span>

<span data-ttu-id="74f36-114">Uma matriz de ponteiros capturados do rastreamento de pilha atual.</span><span class="sxs-lookup"><span data-stu-id="74f36-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="74f36-115">BackTraceHash [saída, opcional]</span><span class="sxs-lookup"><span data-stu-id="74f36-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="74f36-116">Um valor que pode ser usado para organizar tabelas de hash.</span><span class="sxs-lookup"><span data-stu-id="74f36-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="74f36-117">Se esse parâmetro for **NULL**, nenhum valor de hash será computado.</span><span class="sxs-lookup"><span data-stu-id="74f36-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="74f36-118">Esse valor é calculado com base nos valores dos ponteiros retornados na matriz de backtrace.</span><span class="sxs-lookup"><span data-stu-id="74f36-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="74f36-119">Dois rastreamentos de pilha idênticos gerarão valores de hash idênticos.</span><span class="sxs-lookup"><span data-stu-id="74f36-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="74f36-120">Retornos</span><span class="sxs-lookup"><span data-stu-id="74f36-120">Returns</span></span>

<span data-ttu-id="74f36-121">O número de quadros capturados.</span><span class="sxs-lookup"><span data-stu-id="74f36-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f36-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="74f36-122">Remarks</span></span>

<span data-ttu-id="74f36-123">A função **CaptureStackBackTrace** é definida como a função **RtlCaptureStackBackTrace** (a definição é incluída no SDK do Windows a partir do Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="74f36-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="74f36-124">Para obter mais informações, consulte WinBase. h e WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="74f36-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="74f36-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="74f36-125">See also</span></span>
