---
description: Define a chave de assinatura e dois números de sequência em um objeto de saída protegido.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: Função SetOPMSigningKeyAndSequenceNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164885"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="cfdd3-103">Função SetOPMSigningKeyAndSequenceNumbers</span><span class="sxs-lookup"><span data-stu-id="cfdd3-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cfdd3-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="cfdd3-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="cfdd3-106">Define a chave de assinatura e dois números de sequência em um objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfdd3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfdd3-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="cfdd3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfdd3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfdd3-109">*opoOPMProtectedOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cfdd3-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfdd3-110">Um identificador para o objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-110">A handle to the protected output object.</span></span> <span data-ttu-id="cfdd3-111">Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="cfdd3-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfdd3-112">*pParameters* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cfdd3-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfdd3-113">Um ponteiro para uma estrutura de [**\_ \_ \_ parâmetros criptografados DXGKMDT OPM**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) que contém uma matriz de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="cfdd3-114">Para obter mais informações sobre como inicializar essa matriz, consulte [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfdd3-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfdd3-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfdd3-115">Return value</span></span>

<span data-ttu-id="cfdd3-116">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="cfdd3-117">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="cfdd3-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfdd3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfdd3-118">Remarks</span></span>

<span data-ttu-id="cfdd3-119">Os aplicativos devem chamar [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="cfdd3-120">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-120">This function has no associated import library.</span></span> <span data-ttu-id="cfdd3-121">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="cfdd3-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfdd3-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfdd3-122">Requirements</span></span>



| <span data-ttu-id="cfdd3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfdd3-123">Requirement</span></span> | <span data-ttu-id="cfdd3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cfdd3-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cfdd3-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfdd3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfdd3-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfdd3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cfdd3-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfdd3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfdd3-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cfdd3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cfdd3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cfdd3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfdd3-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfdd3-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfdd3-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfdd3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfdd3-132">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="cfdd3-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="cfdd3-133">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="cfdd3-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
