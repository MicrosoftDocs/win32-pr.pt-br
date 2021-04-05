---
title: Mensagem de MMIOM_WRITE (mmsystem. h)
description: A \_ mensagem de gravação MMIOM é enviada a um procedimento de e/s pela função mmioWrite para solicitar que os dados sejam gravados em um arquivo aberto.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- Multimídia do Windows de mensagem MMIOM_WRITE
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919066"
---
# <a name="mmiom_write-message"></a><span data-ttu-id="fdd3e-104">MMIOM \_ gravar mensagem</span><span class="sxs-lookup"><span data-stu-id="fdd3e-104">MMIOM\_WRITE message</span></span>

<span data-ttu-id="fdd3e-105">A mensagem de **\_ gravação MMIOM** é enviada a um procedimento de e/s pela função [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) para solicitar que os dados sejam gravados em um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-105">The **MMIOM\_WRITE** message is sent to an I/O procedure by the [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) function to request that data be written to an open file.</span></span>


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a><span data-ttu-id="fdd3e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fdd3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd3e-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span><span class="sxs-lookup"><span data-stu-id="fdd3e-107"><span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="fdd3e-108">Ponteiro para um buffer que contém os dados a serem gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-108">Pointer to a buffer containing the data to write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="fdd3e-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span><span class="sxs-lookup"><span data-stu-id="fdd3e-109"><span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*</span></span>
</dt> <dd>

<span data-ttu-id="fdd3e-110">Número de bytes a serem gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-110">Number of bytes to write to file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd3e-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fdd3e-111">Return Value</span></span>

<span data-ttu-id="fdd3e-112">Retorna o número de bytes realmente gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-112">Returns the number of bytes actually written to the file.</span></span> <span data-ttu-id="fdd3e-113">Se houver um erro, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-113">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd3e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fdd3e-114">Remarks</span></span>

<span data-ttu-id="fdd3e-115">O procedimento de e/s é responsável por atualizar o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para refletir a nova posição do arquivo após a operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="fdd3e-115">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the write operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd3e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdd3e-116">Requirements</span></span>



| <span data-ttu-id="fdd3e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdd3e-117">Requirement</span></span> | <span data-ttu-id="fdd3e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fdd3e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd3e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdd3e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd3e-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fdd3e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fdd3e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fdd3e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd3e-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fdd3e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fdd3e-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fdd3e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdd3e-124"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fdd3e-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

