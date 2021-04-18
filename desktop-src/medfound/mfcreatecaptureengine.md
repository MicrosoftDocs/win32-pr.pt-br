---
description: Cria uma instância do mecanismo de captura.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: Função MFCreateCaptureEngine
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766520"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="08a6f-103">Função MFCreateCaptureEngine</span><span class="sxs-lookup"><span data-stu-id="08a6f-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="08a6f-104">\[MFCreateCaptureEngine não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="08a6f-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="08a6f-105">\]</span><span class="sxs-lookup"><span data-stu-id="08a6f-105">\]</span></span>

<span data-ttu-id="08a6f-106">Cria uma instância do mecanismo de captura.</span><span class="sxs-lookup"><span data-stu-id="08a6f-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a6f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08a6f-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="08a6f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08a6f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a6f-109">*ppCaptureEngine* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="08a6f-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08a6f-110">Recebe um ponteiro para a interface [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) .</span><span class="sxs-lookup"><span data-stu-id="08a6f-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="08a6f-111">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="08a6f-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a6f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08a6f-112">Return value</span></span>

<span data-ttu-id="08a6f-113">Se a função for bem sucedido, ela retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08a6f-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="08a6f-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08a6f-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a6f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="08a6f-115">Remarks</span></span>

<span data-ttu-id="08a6f-116">Esta função não tem biblioteca de importação associada e não está declarada em um arquivo de cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="08a6f-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="08a6f-117">Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a MFCaptureEngine.dll.</span><span class="sxs-lookup"><span data-stu-id="08a6f-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a6f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08a6f-118">Requirements</span></span>



| <span data-ttu-id="08a6f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="08a6f-119">Requirement</span></span> | <span data-ttu-id="08a6f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="08a6f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08a6f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08a6f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="08a6f-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="08a6f-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08a6f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08a6f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="08a6f-124">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="08a6f-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08a6f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="08a6f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08a6f-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08a6f-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a6f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="08a6f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a6f-128">Funções de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08a6f-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
