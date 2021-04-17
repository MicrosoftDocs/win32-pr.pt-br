---
title: Mensagem de MMIOM_SEEK (mmsystem. h)
description: A mensagem de busca do MMIOM \_ é enviada a um procedimento de e/s pela função mmioSeek para solicitar que a posição atual do arquivo seja movida.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- Multimídia do Windows de mensagem MMIOM_SEEK
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761891"
---
# <a name="mmiom_seek-message"></a><span data-ttu-id="2a121-104">Mensagem de busca do MMIOM \_</span><span class="sxs-lookup"><span data-stu-id="2a121-104">MMIOM\_SEEK message</span></span>

<span data-ttu-id="2a121-105">A mensagem de **\_ busca do MMIOM** é enviada a um procedimento de e/s pela função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) para solicitar que a posição atual do arquivo seja movida.</span><span class="sxs-lookup"><span data-stu-id="2a121-105">The **MMIOM\_SEEK** message is sent to an I/O procedure by the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function to request that the current file position be moved.</span></span>


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a><span data-ttu-id="2a121-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a121-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a121-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span><span class="sxs-lookup"><span data-stu-id="2a121-107"><span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="2a121-108">Nova posição do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a121-108">New file position.</span></span> <span data-ttu-id="2a121-109">O significado desse valor é dependente do sinalizador especificado em **lChangeFlag**.</span><span class="sxs-lookup"><span data-stu-id="2a121-109">The meaning of this value is dependent on the flag specified in **lChangeFlag**.</span></span>

</dd> <dt>

<span data-ttu-id="2a121-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span><span class="sxs-lookup"><span data-stu-id="2a121-110"><span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*</span></span>
</dt> <dd>

<span data-ttu-id="2a121-111">Sinalizador que especifica como a posição do arquivo é alterada.</span><span class="sxs-lookup"><span data-stu-id="2a121-111">Flag specifying how the file position is changed.</span></span> <span data-ttu-id="2a121-112">Os seguintes valores são definidos:</span><span class="sxs-lookup"><span data-stu-id="2a121-112">The following values are defined:</span></span>



| <span data-ttu-id="2a121-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a121-113">Requirement</span></span> | <span data-ttu-id="2a121-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2a121-114">Value</span></span> |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a121-115">BUSCAR em \_ cur</span><span class="sxs-lookup"><span data-stu-id="2a121-115">SEEK\_CUR</span></span> | <span data-ttu-id="2a121-116">Mova a posição do arquivo para ser *lNewFilePos* bytes da posição atual.</span><span class="sxs-lookup"><span data-stu-id="2a121-116">Move the file position to be *lNewFilePos* bytes from the current position.</span></span> <span data-ttu-id="2a121-117">*lNewFilePos* pode ser positivo ou negativo.</span><span class="sxs-lookup"><span data-stu-id="2a121-117">*lNewFilePos* can be positive or negative.</span></span> |
| <span data-ttu-id="2a121-118">fim da busca \_</span><span class="sxs-lookup"><span data-stu-id="2a121-118">SEEK\_END</span></span> | <span data-ttu-id="2a121-119">Mova a posição do arquivo para ser *lNewFilePos* bytes do final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a121-119">Move the file position to be *lNewFilePos* bytes from the end of the file.</span></span>                                             |
| <span data-ttu-id="2a121-120">conjunto de busca \_</span><span class="sxs-lookup"><span data-stu-id="2a121-120">SEEK\_SET</span></span> | <span data-ttu-id="2a121-121">Mova a posição do arquivo para ser *lNewFilePos* bytes do início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a121-121">Move the file position to be *lNewFilePos* bytes from the beginning of the file.</span></span>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a121-122">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="2a121-122">Return Value</span></span>

<span data-ttu-id="2a121-123">Retorna a nova posição do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a121-123">Returns the new file position.</span></span> <span data-ttu-id="2a121-124">Se houver um erro, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="2a121-124">If there is an error, the return value is  1.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a121-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a121-125">Remarks</span></span>

<span data-ttu-id="2a121-126">O procedimento de e/s é responsável por manter a posição atual do arquivo no membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2a121-126">The I/O procedure is responsible for maintaining the current file position in the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a121-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a121-127">Requirements</span></span>



| <span data-ttu-id="2a121-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a121-128">Requirement</span></span> | <span data-ttu-id="2a121-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2a121-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a121-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a121-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a121-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a121-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2a121-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a121-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a121-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a121-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2a121-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a121-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a121-135"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a121-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

