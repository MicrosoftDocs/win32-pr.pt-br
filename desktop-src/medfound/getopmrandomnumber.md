---
description: Obtém um número aleatório de 128 bits, criptograficamente seguro, de um objeto de saída protegido.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: Função GetOPMRandomNumber
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296139"
---
# <a name="getopmrandomnumber-function"></a><span data-ttu-id="a6920-103">Função GetOPMRandomNumber</span><span class="sxs-lookup"><span data-stu-id="a6920-103">GetOPMRandomNumber function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a6920-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a6920-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="a6920-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="a6920-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="a6920-106">Obtém um número aleatório de 128 bits, criptograficamente seguro, de um objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="a6920-106">Gets a 128-bit, cryptographically secure random number from a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6920-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6920-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a><span data-ttu-id="a6920-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6920-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6920-109">*opoOPMProtectedOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a6920-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6920-110">Um identificador para o objeto de saída protegido.</span><span class="sxs-lookup"><span data-stu-id="a6920-110">A handle to the protected output object.</span></span> <span data-ttu-id="a6920-111">Esse identificador é obtido chamando [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="a6920-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="a6920-112">*prnRandomNumber* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a6920-112">*prnRandomNumber* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6920-113">Um ponteiro para uma estrutura de **\_ \_ \_ número aleatório DXGKMDT OPM** que recebe o número aleatório.</span><span class="sxs-lookup"><span data-stu-id="a6920-113">A pointer to a **DXGKMDT\_OPM\_RANDOM\_NUMBER** structure that receives the random number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6920-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6920-114">Return value</span></span>

<span data-ttu-id="a6920-115">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="a6920-115">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="a6920-116">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="a6920-116">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6920-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6920-117">Remarks</span></span>

<span data-ttu-id="a6920-118">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="a6920-118">This function has no associated import library.</span></span> <span data-ttu-id="a6920-119">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="a6920-119">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6920-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6920-120">Requirements</span></span>



| <span data-ttu-id="a6920-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6920-121">Requirement</span></span> | <span data-ttu-id="a6920-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a6920-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6920-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6920-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a6920-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6920-124">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6920-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6920-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a6920-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a6920-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a6920-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a6920-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6920-128"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6920-128"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6920-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6920-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6920-130">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="a6920-130">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="a6920-131">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="a6920-131">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
