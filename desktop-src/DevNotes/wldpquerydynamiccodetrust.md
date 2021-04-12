---
description: Recupera um valor que determina se o código dinâmico especificado na memória ou em disco do .NET CRL é confiável pela política de proteção do dispositivo.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Função WldpQueryDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500904"
---
# <a name="wldpquerydynamiccodetrust-function"></a><span data-ttu-id="65d22-103">Função WldpQueryDynamicCodeTrust</span><span class="sxs-lookup"><span data-stu-id="65d22-103">WldpQueryDynamicCodeTrust function</span></span>

<span data-ttu-id="65d22-104">Recupera um valor que determina se o código dinâmico especificado na memória ou em disco do .NET CRL é confiável pela política de proteção do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="65d22-104">Retrieves a value that determines if the specified in-memory or on-disk .NET CRL dynamic code is trusted by Device Guard policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d22-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65d22-105">Syntax</span></span>


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a><span data-ttu-id="65d22-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65d22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d22-107">*fileHandle*</span><span class="sxs-lookup"><span data-stu-id="65d22-107">*fileHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="65d22-108">Manipule o arquivo de código dinâmico em disco para verificar.</span><span class="sxs-lookup"><span data-stu-id="65d22-108">Handle to the on-disk dynamic code file to check.</span></span> <span data-ttu-id="65d22-109">Se *fileHandle* for não **nulo**, *baseImage* deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="65d22-109">If *fileHandle* is non-**NULL**, *baseImage* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65d22-110">*baseImage*</span><span class="sxs-lookup"><span data-stu-id="65d22-110">*baseImage*</span></span> 
</dt> <dd>

<span data-ttu-id="65d22-111">Ponteiro para o arquivo PE na memória a ser verificado.</span><span class="sxs-lookup"><span data-stu-id="65d22-111">Pointer to the in-memory PE file to check.</span></span> <span data-ttu-id="65d22-112">Se *baseImage* for não **nulo**, *fileHandle* deverá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="65d22-112">If *baseImage* is non-**NULL**, *FileHandle* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="65d22-113">*ImageSize*</span><span class="sxs-lookup"><span data-stu-id="65d22-113">*ImageSize*</span></span> 
</dt> <dd>

<span data-ttu-id="65d22-114">Quando *baseImage* é não **nulo**, indica o tamanho do buffer para o qual o *baseImage* aponta.</span><span class="sxs-lookup"><span data-stu-id="65d22-114">When *baseImage* is non-**NULL**, indicates the buffer size that *baseImage* points to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d22-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65d22-115">Return value</span></span>

<span data-ttu-id="65d22-116">Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.</span><span class="sxs-lookup"><span data-stu-id="65d22-116">This method returns **S\_OK** if successful or a failure code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="65d22-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d22-117">Requirements</span></span>



| <span data-ttu-id="65d22-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d22-118">Requirement</span></span> | <span data-ttu-id="65d22-119">Valor</span><span class="sxs-lookup"><span data-stu-id="65d22-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65d22-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d22-120">Minimum supported client</span></span><br/> | <span data-ttu-id="65d22-121">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="65d22-121">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="65d22-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65d22-122">Minimum supported server</span></span><br/> | <span data-ttu-id="65d22-123">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="65d22-123">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65d22-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65d22-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="65d22-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="65d22-125"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="65d22-126">DLL</span><span class="sxs-lookup"><span data-stu-id="65d22-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65d22-127"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65d22-127"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




