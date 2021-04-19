---
description: Interrompe o modo de coletor Miracast, desativa a descoberta e cancela o registro do retorno de chamada.
ms.assetid: 38AE60CB-F601-4C03-A725-9B802341B84B
title: Função WFDDisplaySinkStop (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStopDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: d1ebaa9920ca7d38cff22cef6383b37065faa2ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770152"
---
# <a name="wfddisplaysinkstop-function"></a><span data-ttu-id="6e68d-103">Função WFDDisplaySinkStop</span><span class="sxs-lookup"><span data-stu-id="6e68d-103">WFDDisplaySinkStop function</span></span>

<span data-ttu-id="6e68d-104">Interrompe o modo de coletor Miracast, desativa a descoberta e cancela o registro do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="6e68d-104">Stops the Miracast sink mode, turns off discoverability, and un-registers the callback.</span></span> <span data-ttu-id="6e68d-105">Seu aplicativo deve chamá-lo uma vez durante o desligamento.</span><span class="sxs-lookup"><span data-stu-id="6e68d-105">Your app should call this once on shutdown.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e68d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e68d-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStopDisplaySink(void);
```



## <a name="parameters"></a><span data-ttu-id="6e68d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e68d-107">Parameters</span></span>

<span data-ttu-id="6e68d-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6e68d-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e68d-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6e68d-109">Return value</span></span>

<span data-ttu-id="6e68d-110">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="6e68d-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e68d-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e68d-111">Remarks</span></span>

<span data-ttu-id="6e68d-112">Espera-se que seu aplicativo tenha desbloqueado quaisquer retornos de chamada em andamento antes de chamar **WFDStopDisplaySink**.</span><span class="sxs-lookup"><span data-stu-id="6e68d-112">It is expected that your app has unblocked any callbacks in progress before calling **WFDStopDisplaySink**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e68d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e68d-113">Requirements</span></span>



| <span data-ttu-id="6e68d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e68d-114">Requirement</span></span> | <span data-ttu-id="6e68d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6e68d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e68d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e68d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e68d-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e68d-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6e68d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e68d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e68d-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="6e68d-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6e68d-120">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="6e68d-120">End of client support</span></span><br/>    | <span data-ttu-id="6e68d-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="6e68d-121">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="6e68d-122">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="6e68d-122">End of server support</span></span><br/>    | <span data-ttu-id="6e68d-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6e68d-123">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="6e68d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e68d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e68d-125"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e68d-125"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="6e68d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e68d-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e68d-127"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e68d-127"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="6e68d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6e68d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e68d-129"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e68d-129"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




