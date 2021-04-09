---
description: 'Saiba mais sobre: função EtwEventWrite'
title: EtwEventWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EtwEventWrite
api_type:
- HeaderDef
api_location:
- ntetw.h
ms.openlocfilehash: 149f611dfb298749befca805509e05fa2dec497a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010240"
---
# <a name="etweventwrite-function"></a><span data-ttu-id="efb00-103">Função EtwEventWrite</span><span class="sxs-lookup"><span data-stu-id="efb00-103">EtwEventWrite function</span></span>

<span data-ttu-id="efb00-104">[A função EtwEventWrite e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.]</span><span class="sxs-lookup"><span data-stu-id="efb00-104">[The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.]</span></span>

<span data-ttu-id="efb00-105">Grava um evento básico em uma sessão.</span><span class="sxs-lookup"><span data-stu-id="efb00-105">Writes a basic event to a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="efb00-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efb00-106">Syntax</span></span>

```C++
ULONG 
EVNTAPI
EtwEventWrite(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR EventDescriptor,
    __in ULONG UserDataCount,
    __in_ecount_opt(UserDataCount) PEVENT_DATA_DESCRIPTOR UserData
    );
```

## <a name="parameters"></a><span data-ttu-id="efb00-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efb00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb00-108">*RegHandle*</span><span class="sxs-lookup"><span data-stu-id="efb00-108">*RegHandle*</span></span>
</dt> <dd>

<span data-ttu-id="efb00-109">RegHandle para o provedor.</span><span class="sxs-lookup"><span data-stu-id="efb00-109">RegHandle for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="efb00-110">*EventDescriptor*</span><span class="sxs-lookup"><span data-stu-id="efb00-110">*EventDescriptor*</span></span>
</dt> <dd>

<span data-ttu-id="efb00-111">Descritor de evento do evento a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="efb00-111">Event descriptor of the event to log.</span></span>

</dd> <dt>

<span data-ttu-id="efb00-112">*UserDataCount*</span><span class="sxs-lookup"><span data-stu-id="efb00-112">*UserDataCount*</span></span>
</dt> <dd>

<span data-ttu-id="efb00-113">Número de itens de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="efb00-113">Number of user data items.</span></span>

</dd> <dt>

<span data-ttu-id="efb00-114">*UserData*</span><span class="sxs-lookup"><span data-stu-id="efb00-114">*UserData*</span></span>
</dt> <dd>

<span data-ttu-id="efb00-115">Ponteiro para uma matriz de itens de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="efb00-115">Pointer to an array of user data items.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efb00-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efb00-116">Return value</span></span>

<span data-ttu-id="efb00-117">Um código de erro Win32.</span><span class="sxs-lookup"><span data-stu-id="efb00-117">A Win32 error code.</span></span>


## <a name="remarks"></a><span data-ttu-id="efb00-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="efb00-118">Remarks</span></span>

<span data-ttu-id="efb00-119">A função EtwEventWrite e as estruturas que ela retorna são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para outra.</span><span class="sxs-lookup"><span data-stu-id="efb00-119">The EtwEventWrite function and the structures that it returns are internal to the operating system and subject to change from one release of Windows to another.</span></span> <span data-ttu-id="efb00-120">Para manter a compatibilidade do seu aplicativo, é melhor usar funções públicas em vez disso.</span><span class="sxs-lookup"><span data-stu-id="efb00-120">To maintain the compatibility of your application, it is better to use public functions instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb00-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efb00-121">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="efb00-122">**Plataforma de Destino**</span><span class="sxs-lookup"><span data-stu-id="efb00-122">**Target Platform**</span></span> | <span data-ttu-id="efb00-123">Windows</span><span class="sxs-lookup"><span data-stu-id="efb00-123">Windows</span></span> |
| <span data-ttu-id="efb00-124">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="efb00-124">**Header**</span></span> | <span data-ttu-id="efb00-125">ntetw. h</span><span class="sxs-lookup"><span data-stu-id="efb00-125">ntetw.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="efb00-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="efb00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb00-127">EventWrite</span><span class="sxs-lookup"><span data-stu-id="efb00-127">EventWrite</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)
</dt> <dt>

[<span data-ttu-id="efb00-128">EventWriteEx</span><span class="sxs-lookup"><span data-stu-id="efb00-128">EventWriteEx</span></span>](/windows/desktop/api/evntprov/nf-evntprov-eventwriteex)
</dt></dl>
