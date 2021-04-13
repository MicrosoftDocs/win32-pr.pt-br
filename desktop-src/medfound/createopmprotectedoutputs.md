---
description: Cria objetos de saída protegidos para um dispositivo de vídeo.
ms.assetid: 616ffb38-173b-48d0-9352-422a61e5bb15
title: Função CreateOPMProtectedOutputs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateOPMProtectedOutputs
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 215cff4a76e7eb36e516e8fd2db312302763198e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501192"
---
# <a name="createopmprotectedoutputs-function"></a><span data-ttu-id="5f264-103">Função CreateOPMProtectedOutputs</span><span class="sxs-lookup"><span data-stu-id="5f264-103">CreateOPMProtectedOutputs function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f264-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f264-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="5f264-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="5f264-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="5f264-106">Cria objetos de saída protegidos para um dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5f264-106">Creates protected output objects for a display device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f264-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f264-107">Syntax</span></span>


```C++
NTSTATUS WINAPI CreateOPMProtectedOutputs(
  _In_  PUNICODE_STRING                    pstrDeviceName,
  _In_  DXGKMDT_OPM_VIDEO_OUTPUT_SEMANTICS vos,
  _In_  DWORD                              dwOPMProtectedOutputArraySize,
  _Out_ DWORD                              *pdwNumOPMProtectedOutputsInArray,
  _Out_ OPM_PROTECTED_OUTPUT_HANDLE        *pohOPMProtectedOutputArray
);
```



## <a name="parameters"></a><span data-ttu-id="5f264-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f264-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f264-109">*pstrDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f264-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f264-110">Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="5f264-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="5f264-111">*vos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f264-111">*vos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f264-112">Um membro da enumeração **\_ semântica de \_ \_ saída \_ de vídeo DXGKMDT OPM** , especificando se a saída protegida terá semântica de Copp (protocolo de proteção de saída) ou semântica OPM.</span><span class="sxs-lookup"><span data-stu-id="5f264-112">A member of the **DXGKMDT\_OPM\_VIDEO\_OUTPUT\_SEMANTICS** enumeration, specifying whether the protected output will have Certified Output Protection Protocol (COPP) semantics or OPM semantics.</span></span>

</dd> <dt>

<span data-ttu-id="5f264-113">*dwOPMProtectedOutputArraySize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f264-113">*dwOPMProtectedOutputArraySize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f264-114">O número de elementos na matriz *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="5f264-114">The number of elements in the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="5f264-115">*pdwNumOPMProtectedOutputsInArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f264-115">*pdwNumOPMProtectedOutputsInArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f264-116">Recebe o número de itens que a função copia para a matriz *pohOPMProtectedOutputArray* .</span><span class="sxs-lookup"><span data-stu-id="5f264-116">Receives the number of items that the function copies to the *pohOPMProtectedOutputArray* array.</span></span>

</dd> <dt>

<span data-ttu-id="5f264-117">*pohOPMProtectedOutputArray* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5f264-117">*pohOPMProtectedOutputArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f264-118">Uma matriz que recebe identificadores para os objetos de saída protegidos.</span><span class="sxs-lookup"><span data-stu-id="5f264-118">An array that receives handles to the protected output objects.</span></span> <span data-ttu-id="5f264-119">Cada identificador deve ser liberado chamando [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span><span class="sxs-lookup"><span data-stu-id="5f264-119">Each handle must be released by calling [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f264-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f264-120">Return value</span></span>

<span data-ttu-id="5f264-121">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="5f264-121">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="5f264-122">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="5f264-122">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f264-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f264-123">Remarks</span></span>

<span data-ttu-id="5f264-124">Em vez de usar essa função, os aplicativos devem chamar uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="5f264-124">Instead of using this function, applications should call one of the following functions:</span></span>

-   [<span data-ttu-id="5f264-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="5f264-125">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object)
-   [<span data-ttu-id="5f264-126">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="5f264-126">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)

<span data-ttu-id="5f264-127">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="5f264-127">This function has no associated import library.</span></span> <span data-ttu-id="5f264-128">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="5f264-128">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f264-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f264-129">Requirements</span></span>



| <span data-ttu-id="5f264-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f264-130">Requirement</span></span> | <span data-ttu-id="5f264-131">Valor</span><span class="sxs-lookup"><span data-stu-id="5f264-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f264-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f264-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5f264-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5f264-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5f264-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f264-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5f264-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5f264-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5f264-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5f264-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f264-137"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f264-137"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f264-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f264-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f264-139">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="5f264-139">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="5f264-140">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="5f264-140">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
