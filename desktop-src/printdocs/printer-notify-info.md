---
description: A estrutura de informações de notificação de impressora \_ \_ contém informações de impressora retornadas pela função FindNextPrinterChangeNotification. A função retorna essas informações depois que uma operação de espera em um objeto de notificação de alteração de impressora é satisfeita.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Estrutura de PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761302"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="c78c6-104">Estrutura de informações de \_ notificação de impressora \_</span><span class="sxs-lookup"><span data-stu-id="c78c6-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="c78c6-105">A estrutura de **\_ \_ informações de notificação de impressora** contém informações de impressora retornadas pela função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="c78c6-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="c78c6-106">A função retorna essas informações depois que uma operação de espera em um objeto de notificação de alteração de impressora é satisfeita.</span><span class="sxs-lookup"><span data-stu-id="c78c6-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="c78c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c78c6-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="c78c6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c78c6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c78c6-109">**Versão**</span><span class="sxs-lookup"><span data-stu-id="c78c6-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="c78c6-110">A versão desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="c78c6-110">The version of this structure.</span></span> <span data-ttu-id="c78c6-111">Defina esse membro como 2.</span><span class="sxs-lookup"><span data-stu-id="c78c6-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="c78c6-112">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="c78c6-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c78c6-113">Um sinalizador de bits que indica o estado da estrutura de notificação.</span><span class="sxs-lookup"><span data-stu-id="c78c6-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="c78c6-114">Se o bit de notificação de informação de impressora \_ \_ \_ descartada estiver definido, isso indica que algumas notificações precisaram ser descartadas.</span><span class="sxs-lookup"><span data-stu-id="c78c6-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="c78c6-115">**Count**</span><span class="sxs-lookup"><span data-stu-id="c78c6-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="c78c6-116">O número de elementos de dados de informações de notificação de impressora na matriz **aData** . [**\_ \_ \_**](printer-notify-info-data.md)</span><span class="sxs-lookup"><span data-stu-id="c78c6-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="c78c6-117">**aData**</span><span class="sxs-lookup"><span data-stu-id="c78c6-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="c78c6-118">Uma matriz de estruturas de [**dados de informações de notificação de impressora \_ \_ \_**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="c78c6-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="c78c6-119">Cada elemento da matriz identifica um único trabalho ou campo de informações de impressora e fornece os dados atuais para esse campo.</span><span class="sxs-lookup"><span data-stu-id="c78c6-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c78c6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c78c6-120">Remarks</span></span>

<span data-ttu-id="c78c6-121">Se o membro **flags** tiver o conjunto de bits de informações de notificação de impressora \_ \_ \_ descartado, isso indicará que ocorreu um estouro ou erro, e as notificações podem ter sido perdidas.</span><span class="sxs-lookup"><span data-stu-id="c78c6-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="c78c6-122">Nesse caso, você deve chamar [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) e especificar o sinalizador de \_ atualização de opções de notificação de impressora \_ \_ para recuperar todas as informações atuais.</span><span class="sxs-lookup"><span data-stu-id="c78c6-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="c78c6-123">Até que você solicite essa operação de atualização, o sistema não enviará notificações adicionais para esse objeto de notificação de alteração.</span><span class="sxs-lookup"><span data-stu-id="c78c6-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c78c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c78c6-124">Requirements</span></span>



| <span data-ttu-id="c78c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c78c6-125">Requirement</span></span> | <span data-ttu-id="c78c6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="c78c6-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c78c6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c78c6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c78c6-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c78c6-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c78c6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c78c6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c78c6-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c78c6-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c78c6-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c78c6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c78c6-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c78c6-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c78c6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c78c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c78c6-134">Impressão</span><span class="sxs-lookup"><span data-stu-id="c78c6-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c78c6-135">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="c78c6-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c78c6-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="c78c6-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="c78c6-137">**\_dados de \_ informações de notificação da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="c78c6-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 




