---
description: Executa a inicialização necessária para permitir que o aplicativo de chamada se torne um coletor de vídeo Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: Função WFDDisplaySinkStart (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502357"
---
# <a name="wfddisplaysinkstart-function"></a><span data-ttu-id="0ea57-103">Função WFDDisplaySinkStart</span><span class="sxs-lookup"><span data-stu-id="0ea57-103">WFDDisplaySinkStart function</span></span>

<span data-ttu-id="0ea57-104">Executa a inicialização necessária para permitir que o aplicativo de chamada se torne um coletor de vídeo Miracast.</span><span class="sxs-lookup"><span data-stu-id="0ea57-104">Performs the necessary initialization to allow the calling app to become a Miracast display sink.</span></span> <span data-ttu-id="0ea57-105">Seu aplicativo deve chamá-lo uma vez na inicialização.</span><span class="sxs-lookup"><span data-stu-id="0ea57-105">Your app should call this once on startup.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea57-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0ea57-106">Syntax</span></span>


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a><span data-ttu-id="0ea57-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ea57-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea57-108">*uDeviceCategory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0ea57-108">*uDeviceCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea57-109">A categoria do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ea57-109">The device category.</span></span>

</dd> <dt>

<span data-ttu-id="0ea57-110">*uSubCategory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0ea57-110">*uSubCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea57-111">A subcategoria do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ea57-111">The device subcategory.</span></span>

</dd> <dt>

<span data-ttu-id="0ea57-112">*pCallbackContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0ea57-112">*pCallbackContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea57-113">Um ponteiro de contexto opcional que é passado para a função de retorno de chamada especificada no parâmetro *pfnCallback* .</span><span class="sxs-lookup"><span data-stu-id="0ea57-113">An optional context pointer which is passed to the callback function specified in the *pfnCallback* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0ea57-114">*pfnCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0ea57-114">*pfnCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ea57-115">Um ponteiro para a função de retorno de chamada a ser chamado sempre que houver uma notificação para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0ea57-115">A pointer to the callback function to be called whenever there is a notification for the app.</span></span> <span data-ttu-id="0ea57-116">As notificações que podem ser enviadas são descritas em [**retorno de chamada de notificação do \_ coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="0ea57-116">Notifications that can be sent are described in [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea57-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ea57-117">Return value</span></span>

<span data-ttu-id="0ea57-118">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="0ea57-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0ea57-119">Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ea57-119">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="0ea57-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0ea57-120">Return code</span></span>                                                                                          | <span data-ttu-id="0ea57-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ea57-121">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="0ea57-122"><dt>**ERRO \_ sem \_ suporte**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea57-122"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="0ea57-123">Não há suporte para o coletor de vídeo neste hardware.</span><span class="sxs-lookup"><span data-stu-id="0ea57-123">The display sink is not supported on this hardware.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ea57-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ea57-124">Remarks</span></span>

<span data-ttu-id="0ea57-125">Essa função executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0ea57-125">This function performs the following tasks:</span></span>

-   <span data-ttu-id="0ea57-126">Torna o PC detectável</span><span class="sxs-lookup"><span data-stu-id="0ea57-126">Makes the PC discoverable</span></span>
-   <span data-ttu-id="0ea57-127">Define as informações do dispositivo P2P para refletir a categoria e a subcategoria especificadas</span><span class="sxs-lookup"><span data-stu-id="0ea57-127">Sets the P2P device info to reflect the category and sub category specified</span></span>
-   <span data-ttu-id="0ea57-128">Define o Miracast s em todos os Wi-Fi quadros diretos com o tipo de dispositivo como o coletor</span><span class="sxs-lookup"><span data-stu-id="0ea57-128">Sets the Miracast IEs on all Wi-Fi Direct frames with the device type as the sink</span></span>
-   <span data-ttu-id="0ea57-129">Registra o retorno de chamada especificado a ser invocado sempre que houver uma conexão de entrada</span><span class="sxs-lookup"><span data-stu-id="0ea57-129">Registers the specified callback to be invoked whenever there is an incoming connection</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea57-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ea57-130">Requirements</span></span>



| <span data-ttu-id="0ea57-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ea57-131">Requirement</span></span> | <span data-ttu-id="0ea57-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0ea57-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea57-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ea57-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea57-134">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0ea57-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0ea57-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ea57-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea57-136">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="0ea57-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0ea57-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="0ea57-137">End of client support</span></span><br/>    | <span data-ttu-id="0ea57-138">Windows 10</span><span class="sxs-lookup"><span data-stu-id="0ea57-138">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="0ea57-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0ea57-139">End of server support</span></span><br/>    | <span data-ttu-id="0ea57-140">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0ea57-140">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="0ea57-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ea57-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ea57-142"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea57-142"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="0ea57-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ea57-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="0ea57-144"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ea57-144"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="0ea57-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea57-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea57-146"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ea57-146"><dt>Wifidisplay.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ea57-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ea57-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea57-148">**\_retorno de \_ chamada de notificação do coletor de vídeo WFD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ea57-148">**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**</span></span>](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




