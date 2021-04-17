---
title: Mensagem de MMIOM_OPEN (mmsystem. h)
description: A \_ mensagem MMIOM Open é enviada a um procedimento de e/s pela função mmioOpen para solicitar que um arquivo seja aberto ou excluído.
ms.assetid: 02b2cf22-21a3-4f49-b90e-7b44478c0168
keywords:
- Multimídia do Windows de mensagem MMIOM_OPEN
topic_type:
- apiref
api_name:
- MMIOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9ea2b5ddc0c79cb3efe00038a628373ce3665bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748129"
---
# <a name="mmiom_open-message"></a><span data-ttu-id="9f254-104">MMIOM \_ Abrir mensagem</span><span class="sxs-lookup"><span data-stu-id="9f254-104">MMIOM\_OPEN message</span></span>

<span data-ttu-id="9f254-105">A mensagem **MMIOM \_ Open** é enviada a um procedimento de e/s pela função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) para solicitar que um arquivo seja aberto ou excluído.</span><span class="sxs-lookup"><span data-stu-id="9f254-105">The **MMIOM\_OPEN** message is sent to an I/O procedure by the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function to request that a file be opened or deleted.</span></span>


```C++
MMIOM_OPEN 
lParam1 = (LPARAM) lpszFileName 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="9f254-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f254-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span><span class="sxs-lookup"><span data-stu-id="9f254-107"><span id="lpszFileName"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFileName*</span></span>
</dt> <dd>

<span data-ttu-id="9f254-108">Cadeia de caracteres terminada em nulo que contém o nome do arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="9f254-108">Null-terminated string containing the name of the file to open.</span></span>

</dd> <dt>

<span data-ttu-id="9f254-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9f254-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9f254-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="9f254-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f254-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="9f254-111">Return Value</span></span>

<span data-ttu-id="9f254-112">Retorna MMSYSERR \_ NOERROR se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9f254-112">Returns MMSYSERR\_NOERROR if successful or an error otherwise.</span></span> <span data-ttu-id="9f254-113">Os possíveis valores de erro incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9f254-113">Possible error values include the following:</span></span>



| <span data-ttu-id="9f254-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f254-114">Requirement</span></span> | <span data-ttu-id="9f254-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9f254-115">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="9f254-116">MMIOM \_ CANNOTOPEN</span><span class="sxs-lookup"><span data-stu-id="9f254-116">MMIOM\_CANNOTOPEN</span></span>  | <span data-ttu-id="9f254-117">Não foi possível abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f254-117">The file could not be opened.</span></span>               |
| <span data-ttu-id="9f254-118">\_OUTOFMEMORY MMIOM</span><span class="sxs-lookup"><span data-stu-id="9f254-118">MMIOM\_OUTOFMEMORY</span></span> | <span data-ttu-id="9f254-119">Não há memória suficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="9f254-119">Not enough memory to perform the operation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9f254-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f254-120">Remarks</span></span>

<span data-ttu-id="9f254-121">O membro **dwFlags** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) contém sinalizadores passados para a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="9f254-121">The **dwFlags** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure contains flags passed to the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span>

<span data-ttu-id="9f254-122">O membro **lDiskOffset** da estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) é inicializado como zero.</span><span class="sxs-lookup"><span data-stu-id="9f254-122">The **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure is initialized to zero.</span></span> <span data-ttu-id="9f254-123">Se esse valor estiver incorreto, o procedimento de e/s deverá corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="9f254-123">If this value is incorrect, the I/O procedure must correct it.</span></span>

<span data-ttu-id="9f254-124">Se o aplicativo passasse uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), o valor de retorno será retornado no membro **wErrorRet** .</span><span class="sxs-lookup"><span data-stu-id="9f254-124">If the application passed an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure to [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen), the return value is returned in the **wErrorRet** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f254-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f254-125">Requirements</span></span>



| <span data-ttu-id="9f254-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f254-126">Requirement</span></span> | <span data-ttu-id="9f254-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9f254-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f254-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f254-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9f254-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f254-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f254-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f254-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9f254-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f254-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f254-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9f254-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f254-133"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f254-133"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

