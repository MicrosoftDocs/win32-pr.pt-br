---
title: Mensagem de MMIOM_READ (mmsystem. h)
description: A \_ mensagem de leitura MMIOM é enviada a um procedimento de e/s pela função mmioRead para solicitar que um número especificado de bytes seja lido a partir de um arquivo aberto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- Multimídia do Windows de mensagem MMIOM_READ
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456032"
---
# <a name="mmiom_read-message"></a><span data-ttu-id="6c5d7-104">MMIOM \_ ler mensagem</span><span class="sxs-lookup"><span data-stu-id="6c5d7-104">MMIOM\_READ message</span></span>

<span data-ttu-id="6c5d7-105">A mensagem de **\_ leitura MMIOM** é enviada a um procedimento de e/s pela função [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) para solicitar que um número especificado de bytes seja lido a partir de um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-105">The **MMIOM\_READ** message is sent to an I/O procedure by the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) function to request that a specified number of bytes be read from an open file.</span></span>


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a><span data-ttu-id="6c5d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c5d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5d7-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span><span class="sxs-lookup"><span data-stu-id="6c5d7-107"><span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*</span></span>
</dt> <dd>

<span data-ttu-id="6c5d7-108">Ponteiro para o buffer a ser preenchido com dados lidos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-108">Pointer to the buffer to be filled with data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="6c5d7-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span><span class="sxs-lookup"><span data-stu-id="6c5d7-109"><span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*</span></span>
</dt> <dd>

<span data-ttu-id="6c5d7-110">Número de bytes a serem lidos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-110">Number of bytes to read from file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5d7-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="6c5d7-111">Return Value</span></span>

<span data-ttu-id="6c5d7-112">Retorna o número de bytes realmente lidos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-112">Returns the number of bytes actually read from the file.</span></span> <span data-ttu-id="6c5d7-113">Se não for possível ler mais bytes, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-113">If no more bytes can be read, the return value is 0.</span></span> <span data-ttu-id="6c5d7-114">Se houver um erro, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-114">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c5d7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c5d7-115">Remarks</span></span>

<span data-ttu-id="6c5d7-116">O procedimento de e/s é responsável por atualizar o membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para refletir a nova posição do arquivo após a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="6c5d7-116">The I/O procedure is responsible for updating the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to reflect the new file position after the read operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5d7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c5d7-117">Requirements</span></span>



| <span data-ttu-id="6c5d7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c5d7-118">Requirement</span></span> | <span data-ttu-id="6c5d7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6c5d7-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5d7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c5d7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5d7-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c5d7-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c5d7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c5d7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5d7-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6c5d7-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c5d7-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6c5d7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5d7-125"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c5d7-125"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

