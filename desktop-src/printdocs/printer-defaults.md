---
description: A \_ estrutura padrões da impressora especifica o tipo de dados padrão, o ambiente, os dados de inicialização e os direitos de acesso de uma impressora.
ms.assetid: df29c3a6-b1d1-4d40-887d-5ffc032a5871
title: Estrutura de PRINTER_DEFAULTS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_DEFAULTS
- _PRINTER_DEFAULTSA
- _PRINTER_DEFAULTSW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: ad3f9b2a6647c620b2d947bca5ef5201076e23ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812866"
---
# <a name="printer_defaults-structure"></a><span data-ttu-id="28b01-103">Estrutura de padrões de impressora \_</span><span class="sxs-lookup"><span data-stu-id="28b01-103">PRINTER\_DEFAULTS structure</span></span>

<span data-ttu-id="28b01-104">A **estrutura \_ padrões da impressora** especifica o tipo de dados padrão, o ambiente, os dados de inicialização e os direitos de acesso de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="28b01-104">The **PRINTER\_DEFAULTS** structure specifies the default data type, environment, initialization data, and access rights for a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28b01-105">Syntax</span></span>


```C++
typedef struct _PRINTER_DEFAULTS {
  LPTSTR      pDatatype;
  LPDEVMODE   pDevMode;
  ACCESS_MASK DesiredAccess;
} PRINTER_DEFAULTS, *PPRINTER_DEFAULTS;
```



## <a name="members"></a><span data-ttu-id="28b01-106">Membros</span><span class="sxs-lookup"><span data-stu-id="28b01-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28b01-107">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="28b01-107">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="28b01-108">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="28b01-108">Pointer to a null-terminated string that specifies the default data type for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="28b01-109">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="28b01-109">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="28b01-110">Ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que identifica o ambiente padrão e os dados de inicialização para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="28b01-110">Pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that identifies the default environment and initialization data for a printer.</span></span>

</dd> <dt>

<span data-ttu-id="28b01-111">**DesiredAccess**</span><span class="sxs-lookup"><span data-stu-id="28b01-111">**DesiredAccess**</span></span>
</dt> <dd>

<span data-ttu-id="28b01-112">Especifica os direitos de acesso desejados para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="28b01-112">Specifies desired access rights for a printer.</span></span> <span data-ttu-id="28b01-113">A função [**OpenPrinter**](openprinter.md) usa esse membro para definir direitos de acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="28b01-113">The [**OpenPrinter**](openprinter.md) function uses this member to set access rights to the printer.</span></span> <span data-ttu-id="28b01-114">Esses direitos podem afetar a operação das funções [**Setprinter**](setprinter.md) e [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="28b01-114">These rights can affect the operation of the [**SetPrinter**](setprinter.md) and [**DeletePrinter**](deleteprinter.md) functions.</span></span> <span data-ttu-id="28b01-115">Os direitos de acesso podem ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="28b01-115">The access rights can be one of the following.</span></span>



| <span data-ttu-id="28b01-116">Valor</span><span class="sxs-lookup"><span data-stu-id="28b01-116">Value</span></span>                                       | <span data-ttu-id="28b01-117">Significado</span><span class="sxs-lookup"><span data-stu-id="28b01-117">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b01-118">acesso de impressora \_ \_ administrar</span><span class="sxs-lookup"><span data-stu-id="28b01-118">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="28b01-119">Para executar tarefas administrativas, como as fornecidas pelo [**Setprinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="28b01-119">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="28b01-120">\_uso de acesso à impressora \_</span><span class="sxs-lookup"><span data-stu-id="28b01-120">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="28b01-121">Para executar operações básicas de impressão.</span><span class="sxs-lookup"><span data-stu-id="28b01-121">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="28b01-122">\_Gerenciamento de acesso à impressora \_ \_ limitado</span><span class="sxs-lookup"><span data-stu-id="28b01-122">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="28b01-123">Para executar tarefas administrativas, como as fornecidas por [**Setprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="28b01-123">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="28b01-124">Esse valor está disponível a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="28b01-124">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="28b01-125">\_todos os \_ acessos à impressora</span><span class="sxs-lookup"><span data-stu-id="28b01-125">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="28b01-126">Para executar todas as tarefas administrativas e operações básicas de impressão, exceto para sincronizar (consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights) ).</span><span class="sxs-lookup"><span data-stu-id="28b01-126">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights) ).</span></span>                                   |
| <span data-ttu-id="28b01-127">valores de segurança genéricos, como gravar \_ DAC</span><span class="sxs-lookup"><span data-stu-id="28b01-127">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="28b01-128">Para permitir direitos de acesso de controle específico.</span><span class="sxs-lookup"><span data-stu-id="28b01-128">To allow specific control access rights.</span></span> <span data-ttu-id="28b01-129">Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="28b01-129">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28b01-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28b01-130">Requirements</span></span>



| <span data-ttu-id="28b01-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="28b01-131">Requirement</span></span> | <span data-ttu-id="28b01-132">Valor</span><span class="sxs-lookup"><span data-stu-id="28b01-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b01-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28b01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="28b01-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28b01-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="28b01-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28b01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="28b01-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28b01-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28b01-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28b01-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="28b01-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28b01-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="28b01-139">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="28b01-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="28b01-140">**\_ \_ DEFAULTSW de impressora** (Unicode) e **\_ \_ DEFAULTSA de impressora** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="28b01-140">**\_PRINTER\_DEFAULTSW** (Unicode) and **\_PRINTER\_DEFAULTSA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="28b01-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="28b01-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28b01-142">Impressão</span><span class="sxs-lookup"><span data-stu-id="28b01-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="28b01-143">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="28b01-143">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="28b01-144">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="28b01-144">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="28b01-145">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="28b01-145">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="28b01-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="28b01-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="28b01-147">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="28b01-147">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

