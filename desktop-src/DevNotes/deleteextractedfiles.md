---
description: A função DeleteExtractedFiles exclui os arquivos extraídos pela função Extract.
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: Função DeleteExtractedFiles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 4ab032864e59d8e7379fe347d241874d9336e431
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753771"
---
# <a name="deleteextractedfiles-function"></a><span data-ttu-id="ec2c7-103">Função DeleteExtractedFiles</span><span class="sxs-lookup"><span data-stu-id="ec2c7-103">DeleteExtractedFiles function</span></span>

<span data-ttu-id="ec2c7-104">\[Essa função não é mais suportada, portanto, seu comportamento não pode ser garantido.\]</span><span class="sxs-lookup"><span data-stu-id="ec2c7-104">\[This function is no longer supported, so its behavior cannot be guaranteed.\]</span></span>

<span data-ttu-id="ec2c7-105">A função **DeleteExtractedFiles** exclui os arquivos extraídos pela função [**Extract**](extract.md) .</span><span class="sxs-lookup"><span data-stu-id="ec2c7-105">The **DeleteExtractedFiles** function deletes the files that were extracted by the [**Extract**](extract.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2c7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec2c7-106">Syntax</span></span>


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a><span data-ttu-id="ec2c7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec2c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec2c7-108">*profissionais*</span><span class="sxs-lookup"><span data-stu-id="ec2c7-108">*ps*</span></span> 
</dt> <dd>

<span data-ttu-id="ec2c7-109">Um ponteiro para uma estrutura de [**sessão**](session.md) que contém informações sobre a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-109">A pointer to a [**SESSION**](session.md) structure that contains information about the current session.</span></span>

<span data-ttu-id="ec2c7-110">Essa função libera a memória no membro **pFileList** dessa estrutura e define **pFileList** como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-110">This function frees the memory in the **pFileList** member of this structure and sets **pFileList** to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec2c7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec2c7-111">Return value</span></span>

<span data-ttu-id="ec2c7-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ec2c7-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec2c7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec2c7-113">Remarks</span></span>

<span data-ttu-id="ec2c7-114">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ec2c7-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec2c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec2c7-115">Requirements</span></span>



| <span data-ttu-id="ec2c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec2c7-116">Requirement</span></span> | <span data-ttu-id="ec2c7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ec2c7-117">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2c7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ec2c7-118">DLL</span></span><br/> | <dl> <span data-ttu-id="ec2c7-119"><dt>Cabinet.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec2c7-119"><dt>Cabinet.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec2c7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec2c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec2c7-121">**Extração**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-121">**Extract**</span></span>](extract.md)
</dt> <dt>

[<span data-ttu-id="ec2c7-122">**SESSÃO**</span><span class="sxs-lookup"><span data-stu-id="ec2c7-122">**SESSION**</span></span>](session.md)
</dt> </dl>

 

 
