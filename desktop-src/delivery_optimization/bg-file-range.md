---
title: Estrutura de BG_FILE_RANGE (Deliveryoptimization. h)
description: A estrutura de BG_FILE_RANGE identifica um intervalo de bytes para baixar de um arquivo.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- Estrutura de BG_FILE_RANGE
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369833"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="db200-104">Estrutura de BG_FILE_RANGE</span><span class="sxs-lookup"><span data-stu-id="db200-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="db200-105">A estrutura de **BG_FILE_RANGE** identifica um intervalo de bytes para baixar de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="db200-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="db200-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db200-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="db200-107">Membros</span><span class="sxs-lookup"><span data-stu-id="db200-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="db200-108">**InitialOffset**</span><span class="sxs-lookup"><span data-stu-id="db200-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="db200-109">Deslocamento de base zero para o início do intervalo de bytes a ser baixado de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="db200-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="db200-110">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="db200-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="db200-111">O comprimento do intervalo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="db200-111">The length of the range, in bytes.</span></span> <span data-ttu-id="db200-112">Não especifique um comprimento de byte zero.</span><span class="sxs-lookup"><span data-stu-id="db200-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="db200-113">Para indicar que o intervalo se estende até o final do arquivo, especifique **BG_LENGTH_TO_EOF**.</span><span class="sxs-lookup"><span data-stu-id="db200-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db200-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="db200-114">Remarks</span></span>

<span data-ttu-id="db200-115">O intervalo deve existir no arquivo ou gerar um erro de **DO_E_INVALID_RANGE** .</span><span class="sxs-lookup"><span data-stu-id="db200-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="db200-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db200-116">Requirements</span></span>



| <span data-ttu-id="db200-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db200-117">Requirement</span></span> | <span data-ttu-id="db200-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db200-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db200-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db200-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db200-120">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="db200-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="db200-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db200-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db200-122">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="db200-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db200-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db200-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db200-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="db200-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db200-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="db200-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db200-126">**IBackgroundCopyFile2::GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="db200-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





