---
description: A função Extract extrai arquivos de um gabinete.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extrair Função
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 2e1096cdb7909f49fbcac7c32891210b25637c90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747882"
---
# <a name="extract-function"></a><span data-ttu-id="a9c94-103">Extrair Função</span><span class="sxs-lookup"><span data-stu-id="a9c94-103">Extract function</span></span>

<span data-ttu-id="a9c94-104">\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.\]</span><span class="sxs-lookup"><span data-stu-id="a9c94-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="a9c94-105">A função **Extract** extrai arquivos de um gabinete.</span><span class="sxs-lookup"><span data-stu-id="a9c94-105">The **Extract** function extracts files from a cabinet.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c94-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9c94-106">Syntax</span></span>


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a><span data-ttu-id="a9c94-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9c94-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c94-108">*profissionais*</span><span class="sxs-lookup"><span data-stu-id="a9c94-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c94-109">Ponteiro para uma estrutura de [**sessão**](session.md) que contém informações sobre a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="a9c94-109">Pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

</dd> <dt>

<span data-ttu-id="a9c94-110">*lpCabName*</span><span class="sxs-lookup"><span data-stu-id="a9c94-110">*lpCabName*</span></span> 
</dt> <dd>

<span data-ttu-id="a9c94-111">Ponteiro para o nome do gabinete do qual os arquivos devem ser extraídos.</span><span class="sxs-lookup"><span data-stu-id="a9c94-111">Pointer to the name of the cabinet from which files are to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c94-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9c94-112">Return value</span></span>

<span data-ttu-id="a9c94-113">Se a função for bem sucedido, ela retornará **S \_ OK**; caso contrário, retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="a9c94-113">If the function succeeds, it returns **S\_OK**; otherwise, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9c94-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9c94-114">Remarks</span></span>

<span data-ttu-id="a9c94-115">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a9c94-115">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c94-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c94-116">Requirements</span></span>



| <span data-ttu-id="a9c94-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c94-117">Requirement</span></span> | <span data-ttu-id="a9c94-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a9c94-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c94-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a9c94-119">DLL</span></span><br/> | <dl> <span data-ttu-id="a9c94-120"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9c94-120"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c94-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9c94-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c94-122">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="a9c94-122">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
</dt> <dt>

[<span data-ttu-id="a9c94-123">**ERF**</span><span class="sxs-lookup"><span data-stu-id="a9c94-123">**ERF**</span></span>](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[<span data-ttu-id="a9c94-124">**SESSÃO**</span><span class="sxs-lookup"><span data-stu-id="a9c94-124">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
