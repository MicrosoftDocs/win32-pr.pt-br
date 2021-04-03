---
description: A \_ estrutura informações sobre a impressora \_ 8 especifica as configurações de impressora padrão globais.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Estrutura de PRINTER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837050"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="a93f7-103">Estrutura de informações da impressora \_ \_ 8</span><span class="sxs-lookup"><span data-stu-id="a93f7-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="a93f7-104">A **estrutura \_ informações \_ sobre a impressora 8** especifica as configurações de impressora padrão globais.</span><span class="sxs-lookup"><span data-stu-id="a93f7-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="a93f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a93f7-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="a93f7-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a93f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a93f7-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="a93f7-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="a93f7-108">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define os dados de impressora padrão globais, como a orientação do papel e a resolução.</span><span class="sxs-lookup"><span data-stu-id="a93f7-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a93f7-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a93f7-109">Remarks</span></span>

<span data-ttu-id="a93f7-110">Os padrões globais são definidos pelo administrador de uma impressora que pode ser usada por qualquer pessoa.</span><span class="sxs-lookup"><span data-stu-id="a93f7-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="a93f7-111">Por outro lado, os padrões por usuário afetarão um usuário específico ou qualquer outra pessoa que use o perfil.</span><span class="sxs-lookup"><span data-stu-id="a93f7-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="a93f7-112">Para padrões por usuário, use as [**informações da \_ impressora \_ 9**](printer-info-9.md).</span><span class="sxs-lookup"><span data-stu-id="a93f7-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a93f7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a93f7-113">Requirements</span></span>



| <span data-ttu-id="a93f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a93f7-114">Requirement</span></span> | <span data-ttu-id="a93f7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a93f7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a93f7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a93f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a93f7-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a93f7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a93f7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a93f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a93f7-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a93f7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a93f7-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a93f7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a93f7-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a93f7-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a93f7-122">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a93f7-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a93f7-123">**\_ Informações de impressora \_ \_ 8W** (Unicode) e **\_ informações de impressora \_ \_ 8a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a93f7-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="a93f7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a93f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a93f7-125">Impressão</span><span class="sxs-lookup"><span data-stu-id="a93f7-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a93f7-126">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="a93f7-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a93f7-127">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="a93f7-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="a93f7-128">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="a93f7-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="a93f7-129">**Informações da impressora \_ \_ 9**</span><span class="sxs-lookup"><span data-stu-id="a93f7-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




