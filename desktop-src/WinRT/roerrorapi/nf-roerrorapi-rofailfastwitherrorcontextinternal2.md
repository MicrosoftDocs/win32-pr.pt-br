---
title: Função RoFailFastWithErrorContextInternal2
description: Gera uma exceção não continuável no processo atual e também permite que você inclua o contexto de erro adicional ainda não capturado pelo sistema operacional.
ms.localizationpriority: low
ms.topic: reference
ms.date: 03/13/2020
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- ComBase.dll
api_name:
- RoFailFastWithErrorContextInternal2
targetos: Windows
ms.openlocfilehash: 84584c339851ecbf8df5d6dbda2aaa575ca6487b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105780749"
---
# <a name="rofailfastwitherrorcontextinternal2-function"></a><span data-ttu-id="ab5a9-103">Função RoFailFastWithErrorContextInternal2</span><span class="sxs-lookup"><span data-stu-id="ab5a9-103">RoFailFastWithErrorContextInternal2 function</span></span>

<span data-ttu-id="ab5a9-104">Gera uma exceção não continuável no processo atual e também permite que você inclua o contexto de erro adicional ainda não capturado pelo sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="ab5a9-104">Raises a non-continuable exception in the current process, and also allows you to include additional error context not already captured by the operating system (OS).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5a9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab5a9-105">Syntax</span></span>

```cpp
void WINAPI RoFailFastWithErrorContextInternal2(
  HRESULT hrError,
  ULONG cStowedExceptions,
  _In_reads_opt_(cStowedExceptions) PSTOWED_EXCEPTION_INFORMATION_V2 aStowedExceptionPointers[]
);
```

## <a name="parameters"></a><span data-ttu-id="ab5a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab5a9-106">Parameters</span></span>

`hrError`

<span data-ttu-id="ab5a9-107">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-107">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="ab5a9-108">O **HRESULT** associado ao erro atual.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-108">The **HRESULT** associated with the current error.</span></span> <span data-ttu-id="ab5a9-109">A exceção é gerada para qualquer valor de *hrError*.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-109">The exception is raised for any value of *hrError*.</span></span>

`cStowedExceptions`

<span data-ttu-id="ab5a9-110">Tipo: **[ULONG](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-110">Type: **[ULONG](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab5a9-111">O número de elementos na matriz *aStowedExceptionPointers* .</span><span class="sxs-lookup"><span data-stu-id="ab5a9-111">The number of elements in the *aStowedExceptionPointers* array.</span></span>

`aStowedExceptionPointers`

<span data-ttu-id="ab5a9-112">Tipo: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-112">Type: **[PSTOWED_EXCEPTION_INFORMATION_V2](../../wer/stowed-exception-information-v2.md)\[\]**</span></span>

<span data-ttu-id="ab5a9-113">Uma matriz de ponteiros para [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) estruturas.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-113">An array of pointers to [**STOWED_EXCEPTION_INFORMATION_V2**](../../wer/stowed-exception-information-v2.md) structures.</span></span> <span data-ttu-id="ab5a9-114">Cada estrutura contém informações que descrevem uma exceção dedevida.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-114">Each structure contains info describing a stowed exception.</span></span> <span data-ttu-id="ab5a9-115">As informações nessas estruturas são enviadas para Relatório de Erros do Windows (WER) junto com as informações de exceção decorrida que foram capturadas pela plataforma.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-115">The info in these structures is then submitted to Windows Error Reporting (WER) along with the stowed exception information that was captured by the platform.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab5a9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab5a9-116">Return value</span></span>

<span data-ttu-id="ab5a9-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-117">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab5a9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab5a9-118">Remarks</span></span>

<span data-ttu-id="ab5a9-119">**RoFailFastWithErrorContextInternal2** não está associado a uma biblioteca de importação nem a um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-119">**RoFailFastWithErrorContextInternal2** isn't associated with an import library nor a header file.</span></span> <span data-ttu-id="ab5a9-120">Você pode chamá-lo primeiro usando a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) (para carregar `ComBase.dll` ) e, em seguida, chamando a função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar o endereço de **RoFailFastWithErrorContextInternal2**.</span><span class="sxs-lookup"><span data-stu-id="ab5a9-120">You can call it by first using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryw) function (to load `ComBase.dll`), and then by calling the [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve the address of **RoFailFastWithErrorContextInternal2**.</span></span>

<span data-ttu-id="ab5a9-121">Para obter mais informações, consulte a [função RoFailFastWithErrorContext](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span><span class="sxs-lookup"><span data-stu-id="ab5a9-121">For more info, see [RoFailFastWithErrorContext function](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5a9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab5a9-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ab5a9-123">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-123">**Target Platform**</span></span> | <span data-ttu-id="ab5a9-124">Windows</span><span class="sxs-lookup"><span data-stu-id="ab5a9-124">Windows</span></span> |
| <span data-ttu-id="ab5a9-125">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-125">**Header**</span></span> | <span data-ttu-id="ab5a9-126">N/D</span><span class="sxs-lookup"><span data-stu-id="ab5a9-126">N/A</span></span> |
| <span data-ttu-id="ab5a9-127">**Biblioteca**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-127">**Library**</span></span> | <span data-ttu-id="ab5a9-128">N/D</span><span class="sxs-lookup"><span data-stu-id="ab5a9-128">N/A</span></span> |
| <span data-ttu-id="ab5a9-129">**DLL**</span><span class="sxs-lookup"><span data-stu-id="ab5a9-129">**DLL**</span></span> | <span data-ttu-id="ab5a9-130">ComBase.dll</span><span class="sxs-lookup"><span data-stu-id="ab5a9-130">ComBase.dll</span></span> |

## <a name="see-also"></a><span data-ttu-id="ab5a9-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab5a9-131">See also</span></span>

* [<span data-ttu-id="ab5a9-132">Função RoFailFastWithErrorContext</span><span class="sxs-lookup"><span data-stu-id="ab5a9-132">RoFailFastWithErrorContext function</span></span>](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext)