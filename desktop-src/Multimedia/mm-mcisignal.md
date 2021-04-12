---
title: Mensagem de MM_MCISIGNAL (mmsystem. h)
description: A \_ mensagem mm MCISIGNAL é enviada a uma janela para notificar um aplicativo de que um dispositivo MCI atingiu uma posição definida em um comando de sinal anterior ( \_ sinal MCI).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- Multimídia do Windows de mensagem MM_MCISIGNAL
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369797"
---
# <a name="mm_mcisignal-message"></a><span data-ttu-id="475cb-104">\_Mensagem mm MCISIGNAL</span><span class="sxs-lookup"><span data-stu-id="475cb-104">MM\_MCISIGNAL message</span></span>

<span data-ttu-id="475cb-105">A mensagem **mm \_ MCISIGNAL** é enviada a uma janela para notificar um aplicativo de que um dispositivo MCI atingiu uma posição definida em um comando de [**sinal**](signal.md) anterior ( [**\_ sinal MCI**](mci-signal.md)).</span><span class="sxs-lookup"><span data-stu-id="475cb-105">The **MM\_MCISIGNAL** message is sent to a window to notify an application that an MCI device has reached a position defined in a previous [**signal**](signal.md) ( [**MCI\_SIGNAL**](mci-signal.md)) command.</span></span>


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a><span data-ttu-id="475cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="475cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475cb-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span><span class="sxs-lookup"><span data-stu-id="475cb-107"><span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*</span></span>
</dt> <dd>

<span data-ttu-id="475cb-108">Identificador do dispositivo que inicia a mensagem de sinal.</span><span class="sxs-lookup"><span data-stu-id="475cb-108">Identifier of the device initiating the signal message.</span></span>

</dd> <dt>

<span data-ttu-id="475cb-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span><span class="sxs-lookup"><span data-stu-id="475cb-109"><span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*</span></span>
</dt> <dd>

<span data-ttu-id="475cb-110">Valor passado no membro **dwUserParm** da estrutura de **\_ parâmetros de \_ sinal \_ do MCI DGV** quando o comando de **sinal** definiu essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="475cb-110">Value passed in the **dwUserParm** member of the **MCI\_DGV\_SIGNAL\_PARAMS** structure when the **signal** command has defined this callback function.</span></span> <span data-ttu-id="475cb-111">Como alternativa, ele pode conter o valor da posição.</span><span class="sxs-lookup"><span data-stu-id="475cb-111">Alternatively, it might contain the position value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="475cb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="475cb-112">Requirements</span></span>



| <span data-ttu-id="475cb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="475cb-113">Requirement</span></span> | <span data-ttu-id="475cb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="475cb-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="475cb-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="475cb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="475cb-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="475cb-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="475cb-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="475cb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="475cb-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="475cb-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="475cb-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="475cb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="475cb-120"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="475cb-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="475cb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="475cb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475cb-122">MCI</span><span class="sxs-lookup"><span data-stu-id="475cb-122">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="475cb-123">Mensagens MCI</span><span class="sxs-lookup"><span data-stu-id="475cb-123">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="475cb-124">**aviso**</span><span class="sxs-lookup"><span data-stu-id="475cb-124">**signal**</span></span>](signal.md)
</dt> </dl>

 

 





