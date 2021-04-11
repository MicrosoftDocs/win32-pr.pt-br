---
description: Envia uma solicitação de status de COPP (protocolo de proteção de saída) para um objeto de saída protegido.
ms.assetid: 24300591-c0c0-48a2-99d3-be98c0c1492a
title: Função GetCOPPCompatibleOPMInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCOPPCompatibleOPMInformation
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 7e5eac24dfcf08e45ce414090835792e594d7c37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164185"
---
# <a name="getcoppcompatibleopminformation-function"></a><span data-ttu-id="e166d-103">Função GetCOPPCompatibleOPMInformation</span><span class="sxs-lookup"><span data-stu-id="e166d-103">GetCOPPCompatibleOPMInformation function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e166d-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e166d-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e166d-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="e166d-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e166d-106">Envia uma solicitação de status de COPP (protocolo de proteção de saída) para um objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="e166d-106">Sends a Certified Output Protection Protocol (COPP) status request to a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e166d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e166d-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCOPPCompatibleOPMInformation(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE                     opoOPMProtectedOutput,
  _In_  DXGKMDT_OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
  _Out_ DXGKMDT_OPM_REQUESTED_INFORMATION               *pRequestedInformation
);
```



## <a name="parameters"></a><span data-ttu-id="e166d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e166d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e166d-109">*opoOPMProtectedOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e166d-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e166d-110">Um identificador para o objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="e166d-110">A handle to the protected output object.</span></span> <span data-ttu-id="e166d-111">Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="e166d-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="e166d-112">*pParameters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e166d-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e166d-113">Um ponteiro para uma estrutura de **\_ \_ \_ \_ \_ \_ parâmetros Get Info compatível com o DXGKMDT OPM Copp** que contém dados de entrada para a solicitação de status.</span><span class="sxs-lookup"><span data-stu-id="e166d-113">A pointer to a **DXGKMDT\_OPM\_COPP\_COMPATIBLE\_GET\_INFO\_PARAMETERS** structure that contains input data for the status request.</span></span>

</dd> <dt>

<span data-ttu-id="e166d-114">*pRequestedInformation* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e166d-114">*pRequestedInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e166d-115">Um ponteiro para um **DXGKMDT \_ OPM \_ solicitou \_** a estrutura de informações que recebe os resultados da solicitação de status.</span><span class="sxs-lookup"><span data-stu-id="e166d-115">A pointer to a **DXGKMDT\_OPM\_REQUESTED\_INFORMATION** structure that receives the results of the status request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e166d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e166d-116">Return value</span></span>

<span data-ttu-id="e166d-117">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="e166d-117">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e166d-118">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e166d-118">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e166d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e166d-119">Remarks</span></span>

<span data-ttu-id="e166d-120">Os aplicativos devem chamar [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="e166d-120">Applications should call [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) instead of calling this function.</span></span>

<span data-ttu-id="e166d-121">O objeto de saída protegido deve ser criado com semântica COPP.</span><span class="sxs-lookup"><span data-stu-id="e166d-121">The protected output object must be created with COPP semantics.</span></span> <span data-ttu-id="e166d-122">Consulte [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="e166d-122">See [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

<span data-ttu-id="e166d-123">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="e166d-123">This function has no associated import library.</span></span> <span data-ttu-id="e166d-124">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e166d-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e166d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e166d-125">Requirements</span></span>



| <span data-ttu-id="e166d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e166d-126">Requirement</span></span> | <span data-ttu-id="e166d-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e166d-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e166d-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e166d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e166d-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e166d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e166d-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e166d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e166d-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e166d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e166d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e166d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e166d-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e166d-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e166d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e166d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e166d-135">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="e166d-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e166d-136">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="e166d-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
