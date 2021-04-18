---
title: Mensagem de MMIOM_CLOSE (mmsystem. h)
description: A \_ mensagem de fechamento MMIOM é enviada a um procedimento de e/s pela função mmioClose para solicitar que um arquivo seja fechado.
ms.assetid: 9d0dad5b-fd0a-4948-a4cf-9d138e353c76
keywords:
- Multimídia do Windows de mensagem MMIOM_CLOSE
topic_type:
- apiref
api_name:
- MMIOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7863698b99bcead8bc22e6194d213bbc663d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499860"
---
# <a name="mmiom_close-message"></a><span data-ttu-id="ea546-104">MMIOM \_ fechar mensagem</span><span class="sxs-lookup"><span data-stu-id="ea546-104">MMIOM\_CLOSE message</span></span>

<span data-ttu-id="ea546-105">A mensagem de **\_ fechamento MMIOM** é enviada a um procedimento de e/s pela função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) para solicitar que um arquivo seja fechado.</span><span class="sxs-lookup"><span data-stu-id="ea546-105">The **MMIOM\_CLOSE** message is sent to an I/O procedure by the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to request that a file be closed.</span></span>


```C++
MMIOM_CLOSE 
lParam1 = (LPARAM) lCloseFlags 
lParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="ea546-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea546-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea546-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span><span class="sxs-lookup"><span data-stu-id="ea546-107"><span id="lCloseFlags"></span><span id="lcloseflags"></span><span id="LCLOSEFLAGS"></span>*lCloseFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ea546-108">Sinalizadores contidos no parâmetro **wFlags** de **mmioClose**.</span><span class="sxs-lookup"><span data-stu-id="ea546-108">Flags contained in the **wFlags** parameter of **mmioClose**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea546-109">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ea546-109">Return Value</span></span>

<span data-ttu-id="ea546-110">Retornará zero se o arquivo for fechado com êxito ou se um erro for diferente.</span><span class="sxs-lookup"><span data-stu-id="ea546-110">Returns zero if the file is successfully closed or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea546-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea546-111">Requirements</span></span>



| <span data-ttu-id="ea546-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea546-112">Requirement</span></span> | <span data-ttu-id="ea546-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ea546-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea546-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea546-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ea546-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea546-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea546-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea546-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ea546-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ea546-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea546-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ea546-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea546-119"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea546-119"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



 

