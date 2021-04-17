---
description: Libera um objeto de saída protegido.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: Função DestroyOPMProtectedOutput
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813010"
---
# <a name="destroyopmprotectedoutput-function"></a><span data-ttu-id="14437-103">Função DestroyOPMProtectedOutput</span><span class="sxs-lookup"><span data-stu-id="14437-103">DestroyOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14437-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="14437-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="14437-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="14437-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="14437-106">Libera um objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="14437-106">Releases a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="14437-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14437-107">Syntax</span></span>


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a><span data-ttu-id="14437-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14437-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14437-109">*opoOPMProtectedOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="14437-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14437-110">Um identificador para o objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="14437-110">A handle to the protected output object.</span></span> <span data-ttu-id="14437-111">Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="14437-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14437-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14437-112">Return value</span></span>

<span data-ttu-id="14437-113">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="14437-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="14437-114">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="14437-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14437-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="14437-115">Remarks</span></span>

<span data-ttu-id="14437-116">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="14437-116">This function has no associated import library.</span></span> <span data-ttu-id="14437-117">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="14437-117">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="14437-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14437-118">Requirements</span></span>



| <span data-ttu-id="14437-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14437-119">Requirement</span></span> | <span data-ttu-id="14437-120">Valor</span><span class="sxs-lookup"><span data-stu-id="14437-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="14437-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14437-121">Minimum supported client</span></span><br/> | <span data-ttu-id="14437-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14437-122">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="14437-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14437-123">Minimum supported server</span></span><br/> | <span data-ttu-id="14437-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14437-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="14437-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14437-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14437-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14437-126"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14437-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="14437-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14437-128">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="14437-128">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="14437-129">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="14437-129">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
