---
description: Obtém o tamanho da matriz que deve ser alocada antes de chamar CreateOPMProtectedOutputs.
ms.assetid: 65edce14-f225-4b7f-b953-32b085e1cabf
title: Função GetSuggestedOPMProtectedOutputArraySize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSuggestedOPMProtectedOutputArraySize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 87139f0b485ef3c01e5196db85b36faeb662e4d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089735"
---
# <a name="getsuggestedopmprotectedoutputarraysize-function"></a><span data-ttu-id="92e4c-103">Função GetSuggestedOPMProtectedOutputArraySize</span><span class="sxs-lookup"><span data-stu-id="92e4c-103">GetSuggestedOPMProtectedOutputArraySize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="92e4c-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="92e4c-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="92e4c-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="92e4c-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="92e4c-106">Obtém o tamanho da matriz que deve ser alocada antes de chamar [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="92e4c-106">Gets the size of the array that should be allocated before calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92e4c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92e4c-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetSuggestedOPMProtectedOutputArraySize(
  _In_  PUNICODE_STRING pstrDeviceName,
  _Out_ DWORD           *pdwSuggestedOPMProtectedOutputArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="92e4c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92e4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e4c-109">*pstrDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92e4c-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e4c-110">Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="92e4c-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="92e4c-111">*pdwSuggestedOPMProtectedOutputArraySize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="92e4c-111">*pdwSuggestedOPMProtectedOutputArraySize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92e4c-112">Recebe o tamanho que deve ser alocado para a matriz, em número de elementos da matriz.</span><span class="sxs-lookup"><span data-stu-id="92e4c-112">Receives the size that should be allocated for the array, in number of array elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e4c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92e4c-113">Return value</span></span>

<span data-ttu-id="92e4c-114">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="92e4c-114">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="92e4c-115">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="92e4c-115">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92e4c-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="92e4c-116">Remarks</span></span>

<span data-ttu-id="92e4c-117">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="92e4c-117">This function has no associated import library.</span></span> <span data-ttu-id="92e4c-118">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="92e4c-118">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e4c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e4c-119">Requirements</span></span>



| <span data-ttu-id="92e4c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e4c-120">Requirement</span></span> | <span data-ttu-id="92e4c-121">Valor</span><span class="sxs-lookup"><span data-stu-id="92e4c-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="92e4c-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92e4c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92e4c-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92e4c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="92e4c-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92e4c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92e4c-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92e4c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="92e4c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="92e4c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92e4c-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92e4c-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e4c-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="92e4c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e4c-129">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="92e4c-129">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="92e4c-130">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="92e4c-130">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
