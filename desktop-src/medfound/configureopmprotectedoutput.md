---
description: Configura um objeto de saída protegido.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: Função ConfigureOPMProtectedOutput
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370540"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="75bfb-103">Função ConfigureOPMProtectedOutput</span><span class="sxs-lookup"><span data-stu-id="75bfb-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75bfb-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="75bfb-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="75bfb-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="75bfb-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="75bfb-106">Configura um objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="75bfb-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="75bfb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75bfb-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="75bfb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75bfb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75bfb-109">*opoOPMProtectedOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75bfb-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75bfb-110">Um identificador para o objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="75bfb-110">A handle to the protected output object.</span></span> <span data-ttu-id="75bfb-111">Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="75bfb-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="75bfb-112">*pParameters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75bfb-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75bfb-113">Um ponteiro para uma estrutura **DXGKMDT \_ OPM \_ configure \_ Parameters** que contém o comando de configuração.</span><span class="sxs-lookup"><span data-stu-id="75bfb-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="75bfb-114">*ulAdditionalParametersSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75bfb-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75bfb-115">O tamanho do buffer *pbAdditionalParameters* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="75bfb-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="75bfb-116">*pbAdditionalParameters* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="75bfb-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75bfb-117">Um ponteiro para um buffer que contém informações adicionais para o comando.</span><span class="sxs-lookup"><span data-stu-id="75bfb-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75bfb-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75bfb-118">Return value</span></span>

<span data-ttu-id="75bfb-119">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="75bfb-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="75bfb-120">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="75bfb-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="75bfb-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="75bfb-121">Remarks</span></span>

<span data-ttu-id="75bfb-122">Os aplicativos devem chamar [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="75bfb-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="75bfb-123">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="75bfb-123">This function has no associated import library.</span></span> <span data-ttu-id="75bfb-124">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="75bfb-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="75bfb-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75bfb-125">Requirements</span></span>



| <span data-ttu-id="75bfb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="75bfb-126">Requirement</span></span> | <span data-ttu-id="75bfb-127">Valor</span><span class="sxs-lookup"><span data-stu-id="75bfb-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75bfb-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75bfb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75bfb-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75bfb-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="75bfb-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75bfb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75bfb-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75bfb-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75bfb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="75bfb-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75bfb-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75bfb-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75bfb-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="75bfb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bfb-135">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="75bfb-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="75bfb-136">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="75bfb-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
