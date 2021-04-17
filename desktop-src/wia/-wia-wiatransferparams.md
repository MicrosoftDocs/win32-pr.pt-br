---
description: 'O WiaTransferParams é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de execução da aquisição de imagens do Windows (WIA) para o método IWiaTransferCallback:: TransferCallback.'
ms.assetid: 4f1bbacf-e9fd-4129-ab05-3edaeecfaf43
title: Estrutura WiaTransferParams (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaTransferParams
api_type:
- HeaderDef
api_location:
- Wia.h
ms.openlocfilehash: 4c432cab14e08d89a49234dd7c6de059cc9d72c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783724"
---
# <a name="wiatransferparams-structure"></a><span data-ttu-id="78d01-103">Estrutura WiaTransferParams</span><span class="sxs-lookup"><span data-stu-id="78d01-103">WiaTransferParams structure</span></span>

<span data-ttu-id="78d01-104">O **WiaTransferParams** é transmitido para um aplicativo durante uma transferência de dados pelo sistema de tempo de execução da aquisição de imagens do Windows (WIA) para o método [**IWiaTransferCallback:: TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) .</span><span class="sxs-lookup"><span data-stu-id="78d01-104">The **WiaTransferParams** is transmitted to an application during a data transfer by the Windows Image Acquisition (WIA) run-time system to the [**IWiaTransferCallback::TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78d01-105">Syntax</span></span>


```C++
typedef struct _WiaTransferParams {
  LONG    lMessage;
  LONG    lPercentComplete;
  ULONG64 ulTransferredBytes;
  HRESULT hrErrorStatus;
} WiaTransferParams;
```



## <a name="members"></a><span data-ttu-id="78d01-106">Membros</span><span class="sxs-lookup"><span data-stu-id="78d01-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="78d01-107">**lMessage**</span><span class="sxs-lookup"><span data-stu-id="78d01-107">**lMessage**</span></span>
</dt> <dd>

<span data-ttu-id="78d01-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="78d01-108">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="78d01-109">Indica o status da transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="78d01-109">Indicates the status of the data transfer.</span></span>

<dt>

<span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>

<span data-ttu-id="78d01-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**\_status da \_ mensagem de transferência WIA \_**</span><span class="sxs-lookup"><span data-stu-id="78d01-110"><span id="WIA_TRANSFER_MSG_STATUS"></span><span id="wia_transfer_msg_status"></span>**WIA\_TRANSFER\_MSG\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>

<span data-ttu-id="78d01-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**\_ \_ \_ fim \_ do fluxo de mensagens de transferência WIA \_**</span><span class="sxs-lookup"><span data-stu-id="78d01-111"><span id="WIA_TRANSFER_MSG_END_OF_STREAM"></span><span id="wia_transfer_msg_end_of_stream"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_STREAM**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>

<span data-ttu-id="78d01-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**\_ \_ \_ fim \_ da mensagem de \_ transferência WIA**</span><span class="sxs-lookup"><span data-stu-id="78d01-112"><span id="WIA_TRANSFER_MSG_END_OF_TRANSFER"></span><span id="wia_transfer_msg_end_of_transfer"></span>**WIA\_TRANSFER\_MSG\_END\_OF\_TRANSFER**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>

<span data-ttu-id="78d01-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**\_status do \_ dispositivo de mensagens de transferência WIA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="78d01-113"><span id="WIA_TRANSFER_MSG_DEVICE_STATUS"></span><span id="wia_transfer_msg_device_status"></span>**WIA\_TRANSFER\_MSG\_DEVICE\_STATUS**</span></span>


</dt> <dd></dd> <dt>

<span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>

<span data-ttu-id="78d01-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**\_ \_ \_ nova página de mensagens de transferência WIA \_**</span><span class="sxs-lookup"><span data-stu-id="78d01-114"><span id="WIA_TRANSFER_MSG_NEW_PAGE"></span><span id="wia_transfer_msg_new_page"></span>**WIA\_TRANSFER\_MSG\_NEW\_PAGE**</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="78d01-115">**lPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="78d01-115">**lPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="78d01-116">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="78d01-116">Type: **LONG**</span></span>

</dd> <dd>

<span data-ttu-id="78d01-117">Indica o progresso da transferência de dados como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="78d01-117">Indicates the progress of the data transfer as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="78d01-118">**ulTransferredBytes**</span><span class="sxs-lookup"><span data-stu-id="78d01-118">**ulTransferredBytes**</span></span>
</dt> <dd>

<span data-ttu-id="78d01-119">Tipo: **ULONG64**</span><span class="sxs-lookup"><span data-stu-id="78d01-119">Type: **ULONG64**</span></span>

</dd> <dd>

<span data-ttu-id="78d01-120">Indica a quantidade de dados transferidos.</span><span class="sxs-lookup"><span data-stu-id="78d01-120">Indicates the amount of data transferred.</span></span>

</dd> <dt>

<span data-ttu-id="78d01-121">**hrErrorStatus**</span><span class="sxs-lookup"><span data-stu-id="78d01-121">**hrErrorStatus**</span></span>
</dt> <dd>

<span data-ttu-id="78d01-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="78d01-122">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="78d01-123">O status ou o estado de erro do dispositivo definido pelo driver; por exemplo, "aquecendo".</span><span class="sxs-lookup"><span data-stu-id="78d01-123">The status, or error state, of the device set by the driver; for example, "warming up".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="78d01-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78d01-124">Requirements</span></span>



| <span data-ttu-id="78d01-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="78d01-125">Requirement</span></span> | <span data-ttu-id="78d01-126">Valor</span><span class="sxs-lookup"><span data-stu-id="78d01-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="78d01-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78d01-127">Minimum supported client</span></span><br/> | <span data-ttu-id="78d01-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78d01-128">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="78d01-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78d01-129">Minimum supported server</span></span><br/> | <span data-ttu-id="78d01-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78d01-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="78d01-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78d01-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d01-132"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="78d01-132"><dt>Wia.h</dt></span></span> </dl> |



 

 




