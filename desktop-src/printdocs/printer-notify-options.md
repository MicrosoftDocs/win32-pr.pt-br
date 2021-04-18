---
description: A \_ \_ estrutura opções de notificação de impressora especifica opções para um objeto de notificação de alteração que monitora uma impressora ou um servidor de impressão.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Estrutura de PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785964"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="588a0-103">Estrutura de opções de \_ notificação de impressora \_</span><span class="sxs-lookup"><span data-stu-id="588a0-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="588a0-104">A **estrutura \_ \_ Opções** de notificação de impressora especifica opções para um objeto de notificação de alteração que monitora uma impressora ou um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="588a0-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="588a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="588a0-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="588a0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="588a0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="588a0-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="588a0-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="588a0-108">A versão desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="588a0-108">The version of this structure.</span></span> <span data-ttu-id="588a0-109">Defina esse membro como 2.</span><span class="sxs-lookup"><span data-stu-id="588a0-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="588a0-110">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="588a0-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="588a0-111">Um sinalizador de bits.</span><span class="sxs-lookup"><span data-stu-id="588a0-111">A bit flag.</span></span> <span data-ttu-id="588a0-112">Se você definir o \_ sinalizador de atualização de opções de notificação de impressora \_ \_ em uma chamada para a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , a função fornecerá dados atuais para todos os campos de informações de impressora monitorados.</span><span class="sxs-lookup"><span data-stu-id="588a0-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="588a0-113">A função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignora o membro **flags** .</span><span class="sxs-lookup"><span data-stu-id="588a0-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="588a0-114">**Count**</span><span class="sxs-lookup"><span data-stu-id="588a0-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="588a0-115">O número de elementos na matriz **pTypes** .</span><span class="sxs-lookup"><span data-stu-id="588a0-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="588a0-116">**pTypes**</span><span class="sxs-lookup"><span data-stu-id="588a0-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="588a0-117">Um ponteiro para uma matriz de [**Opções de notificação de impressora \_ \_ \_ tipo**](printer-notify-options-type.md) estruturas.</span><span class="sxs-lookup"><span data-stu-id="588a0-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="588a0-118">Use um elemento dessa matriz para especificar os campos de informações da impressora a serem monitorados e um elemento para especificar os campos de informações do trabalho a serem monitorados.</span><span class="sxs-lookup"><span data-stu-id="588a0-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="588a0-119">Você pode monitorar as informações da impressora, as informações do trabalho ou ambas.</span><span class="sxs-lookup"><span data-stu-id="588a0-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="588a0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="588a0-120">Remarks</span></span>

<span data-ttu-id="588a0-121">Use essa estrutura com a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) para especificar o conjunto de campos de informações da impressora ou do trabalho a ser monitorado para alteração.</span><span class="sxs-lookup"><span data-stu-id="588a0-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="588a0-122">Use essa estrutura com a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) para solicitar os dados atuais de todos os campos de impressora e de informações de trabalho monitorados.</span><span class="sxs-lookup"><span data-stu-id="588a0-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="588a0-123">Nesse caso, o membro **flags** especifica o sinalizador de \_ atualização de opções de notificação de impressora \_ \_ e a função ignora os outros membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="588a0-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="588a0-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="588a0-124">Requirements</span></span>



| <span data-ttu-id="588a0-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="588a0-125">Requirement</span></span> | <span data-ttu-id="588a0-126">Valor</span><span class="sxs-lookup"><span data-stu-id="588a0-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="588a0-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="588a0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="588a0-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="588a0-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="588a0-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="588a0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="588a0-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="588a0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="588a0-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="588a0-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="588a0-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="588a0-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="588a0-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="588a0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588a0-134">Impressão</span><span class="sxs-lookup"><span data-stu-id="588a0-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="588a0-135">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="588a0-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="588a0-136">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="588a0-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="588a0-137">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="588a0-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="588a0-138">**\_tipo de \_ Opções de notificação de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="588a0-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 




