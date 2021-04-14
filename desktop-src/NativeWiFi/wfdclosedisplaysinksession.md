---
description: Limpa o estado da sessão que está sendo aberta ou a sessão aberta no momento.
ms.assetid: 8247AFA9-F471-4CCD-972D-D0C827E86880
title: Função WFDDisplaySinkCloseSession (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDCloseDisplaySinkSession
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 7697bc7ff1aa42569cf954b3f0b037f66ec67ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502358"
---
# <a name="wfddisplaysinkclosesession-function"></a><span data-ttu-id="39c0e-103">Função WFDDisplaySinkCloseSession</span><span class="sxs-lookup"><span data-stu-id="39c0e-103">WFDDisplaySinkCloseSession function</span></span>

<span data-ttu-id="39c0e-104">Limpa o estado da sessão que está sendo aberta ou a sessão aberta no momento.</span><span class="sxs-lookup"><span data-stu-id="39c0e-104">Cleans up the state for the session being opened, or the currently open session.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c0e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39c0e-105">Syntax</span></span>


```C++
DWORD WINAPI WFDCloseDisplaySinkSession(
  _In_ HANDLE hSessionHandle
);
```



## <a name="parameters"></a><span data-ttu-id="39c0e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39c0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c0e-107">*hSessionHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="39c0e-107">*hSessionHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c0e-108">O identificador recebido por meio da invocação de retorno de chamada de notificação do coletor de vídeo do WFD mais recente que incluiu um. [**\_ \_ \_ \_**](wfd-display-sink-notification-callback.md)</span><span class="sxs-lookup"><span data-stu-id="39c0e-108">The handle received via the most recent [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) invocation that included one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c0e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39c0e-109">Return value</span></span>

<span data-ttu-id="39c0e-110">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="39c0e-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c0e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="39c0e-111">Remarks</span></span>

<span data-ttu-id="39c0e-112">Seu aplicativo pode chamar essa função para encerrar a sessão Miracast por qualquer motivo.</span><span class="sxs-lookup"><span data-stu-id="39c0e-112">Your app can call this function to terminate the Miracast session for any reason.</span></span> <span data-ttu-id="39c0e-113">Seu aplicativo não precisa chamá-lo quando recebe o tipo **DisconnectedNotification** em seu retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="39c0e-113">Your app is not required to call it when it receives the **DisconnectedNotification** type in its callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c0e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c0e-114">Requirements</span></span>



| <span data-ttu-id="39c0e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c0e-115">Requirement</span></span> | <span data-ttu-id="39c0e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="39c0e-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c0e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39c0e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="39c0e-118">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="39c0e-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="39c0e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39c0e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="39c0e-120">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="39c0e-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39c0e-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="39c0e-121">End of client support</span></span><br/>    | <span data-ttu-id="39c0e-122">Windows 10</span><span class="sxs-lookup"><span data-stu-id="39c0e-122">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="39c0e-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="39c0e-123">End of server support</span></span><br/>    | <span data-ttu-id="39c0e-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="39c0e-124">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="39c0e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39c0e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c0e-126"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c0e-126"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="39c0e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39c0e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="39c0e-128"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39c0e-128"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="39c0e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="39c0e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39c0e-130"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c0e-130"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c0e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="39c0e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c0e-132">**\_retorno de \_ chamada de notificação do coletor de vídeo WFD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="39c0e-132">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




