---
description: Descreve o resultado que você pode definir opcionalmente depois de processar um coletor de exibição notificação na \_ função de retorno de chamada de notificação do coletor de vídeo WFD \_ \_ \_ .
ms.assetid: 6ED04294-2ED9-455B-9274-8C3DB06D4B21
title: Estrutura de WFD_DISPLAY_SINK_NOTIFICATION_RESULT (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFD_DISPLAY_SINK_NOTIFICATION
api_type:
- HeaderDef
api_location:
- wfdsink.h
ms.openlocfilehash: dc23416d4d13284862aea652dd71909e71879afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750794"
---
# <a name="wfd_display_sink_notification_result-structure"></a><span data-ttu-id="f6cbe-103">\_Estrutura de \_ resultados da notificação do coletor de vídeo WFD \_ \_</span><span class="sxs-lookup"><span data-stu-id="f6cbe-103">WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT structure</span></span>

<span data-ttu-id="f6cbe-104">A estrutura de **resultados da notificação do \_ coletor de vídeo \_ \_ \_ WFD** descreve o resultado que você pode definir opcionalmente após o processamento de um coletor de vídeo notificação na função de retorno de chamada de [**\_ notificação do coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md) .</span><span class="sxs-lookup"><span data-stu-id="f6cbe-104">The **WFD\_DISPLAY\_SINK\_NOTIFICATION\_RESULT** structure describes the result that you can optionally set after processing a display sink notfication in the [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_CALLBACK**](wfd-display-sink-notification-callback.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6cbe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6cbe-105">Syntax</span></span>


```C++
typedef struct _WFD_DISPLAY_SINK_NOTIFICATION {
  WFD_DISPLAY_SINK_OBJECT_HEADER     Header;
  WFD_DISPLAY_SINK_NOTIFICATION_TYPE type;
  union {
    struct {
      DOT11_WPS_CONFIG_METHOD ConfigMethod;
      UINT32                  uPassKeyLength;
      WCHAR                   Passkey[WFD_SINK_WPS_INFO_MAX_PASSKEY_LENGTH];
    } ProvisioningData;
    struct {
      PWSTR strProfile;
    } ReconnectData;
  };
} WFD_DISPLAY_SINK_NOTIFICATION, *PWFD_DISPLAY_SINK_NOTIFICATION;
```



## <a name="members"></a><span data-ttu-id="f6cbe-106">Membros</span><span class="sxs-lookup"><span data-stu-id="f6cbe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f6cbe-107">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-107">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-108">Um [**\_ cabeçalho de \_ \_ objeto do \_ coletor de vídeo WFD**](wfd-display-sink-object-header.md) que descreve os dados incluídos no resultado da notificação.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-108">A [**WFD\_DISPLAY\_SINK\_OBJECT\_HEADER**](wfd-display-sink-object-header.md) that describes the data included in the notification result.</span></span>

</dd> <dt>

<span data-ttu-id="f6cbe-109">**tipo**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-109">**type**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-110">Um valor de [**tipo de notificação do \_ coletor de vídeo \_ \_ \_ WFD**](wfd-display-sink-notification-type.md) que indica o tipo do resultado da notificação.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-110">A [**WFD\_DISPLAY\_SINK\_NOTIFICATION\_TYPE**](wfd-display-sink-notification-type.md) value that indicates the type of the notification result.</span></span> <span data-ttu-id="f6cbe-111">Esse parâmetro também determina quais informações usar na União abaixo.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-111">This parameter also determines which Info to use in the union below.</span></span>

</dd> <dt>

<span data-ttu-id="f6cbe-112">**ProvisioningData**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-112">**ProvisioningData**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-113">Informações sobre o resultado de uma solicitação de provisionamento.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-113">Info about the result of a provisioning request.</span></span> <span data-ttu-id="f6cbe-114">Use isto se o *tipo* tiver o valor **ProvisioningRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-114">Use this if *type* has the value **ProvisioningRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="f6cbe-115">**ConfigMethod**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-115">**ConfigMethod**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-116">O método para mostrar a interface do usuário para aceitação interativa.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-116">The method for showing UI for interactive acceptance.</span></span>

</dd> <dt>

<span data-ttu-id="f6cbe-117">**uPassKeyLength**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-117">**uPassKeyLength**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-118">O número de caracteres largos na *chave* de acesso, não contando nenhum terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-118">The number of wide characters in *Passkey*, not counting any NULL-terminator.</span></span>

</dd> <dt>

<span data-ttu-id="f6cbe-119">**Chave**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-119">**Passkey**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-120">Contém a chave de passagem como uma matriz de caracteres largos.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-120">Contains the pass key as an array of wide characters.</span></span> <span data-ttu-id="f6cbe-121">\_ \_ \_ \_ \_ \_ O comprimento máximo de chave de acesso de informações do WPS do coletor WFD é definido como o valor (8).</span><span class="sxs-lookup"><span data-stu-id="f6cbe-121">WFD\_SINK\_WPS\_INFO\_MAX\_PASSKEY\_LENGTH is defined as the value (8).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f6cbe-122">**ReconnectData**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-122">**ReconnectData**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-123">Informações sobre o resultado de uma solicitação de reconexão.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-123">Info about the result of a reconnect request.</span></span> <span data-ttu-id="f6cbe-124">Use isto se o *tipo* tiver o valor **ReconnectRequestNotification**.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-124">Use this if *type* has the value **ReconnectRequestNotification**.</span></span>

<dl> <dt>

<span data-ttu-id="f6cbe-125">**strProfile**</span><span class="sxs-lookup"><span data-stu-id="f6cbe-125">**strProfile**</span></span>
</dt> <dd>

<span data-ttu-id="f6cbe-126">Um ponteiro para uma cadeia de caracteres terminada em nulo que descreve o perfil.</span><span class="sxs-lookup"><span data-stu-id="f6cbe-126">A pointer to a NULL-terminated string describing the profile.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6cbe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6cbe-127">Requirements</span></span>



| <span data-ttu-id="f6cbe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6cbe-128">Requirement</span></span> | <span data-ttu-id="f6cbe-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f6cbe-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6cbe-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6cbe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f6cbe-131">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f6cbe-131">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6cbe-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6cbe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f6cbe-133">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f6cbe-133">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f6cbe-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6cbe-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6cbe-135"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6cbe-135"><dt>Wfdsink.h</dt></span></span> </dl> |



 

 




