---
description: A \_ estrutura informações da impressora \_ 9 especifica as configurações de impressora padrão por usuário.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Estrutura de PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793988"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="9c537-103">Estrutura de informações da impressora \_ \_ 9</span><span class="sxs-lookup"><span data-stu-id="9c537-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="9c537-104">A **estrutura \_ informações \_ da impressora 9** especifica as configurações de impressora padrão por usuário.</span><span class="sxs-lookup"><span data-stu-id="9c537-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c537-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c537-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="9c537-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9c537-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9c537-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="9c537-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="9c537-108">Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que define os dados de impressora padrão por usuário, como a orientação do papel e a resolução.</span><span class="sxs-lookup"><span data-stu-id="9c537-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="9c537-109">O **DEVMODE** é armazenado no registro do usuário.</span><span class="sxs-lookup"><span data-stu-id="9c537-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c537-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c537-110">Remarks</span></span>

<span data-ttu-id="9c537-111">Os padrões por usuário afetarão apenas um usuário específico ou qualquer pessoa que use o perfil.</span><span class="sxs-lookup"><span data-stu-id="9c537-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="9c537-112">Por outro lado, os padrões globais são definidos pelo administrador de uma impressora que pode ser usada por qualquer pessoa.</span><span class="sxs-lookup"><span data-stu-id="9c537-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="9c537-113">Para padrões globais, use as [**informações da impressora \_ \_ 8**](printer-info-8.md).</span><span class="sxs-lookup"><span data-stu-id="9c537-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c537-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c537-114">Requirements</span></span>



| <span data-ttu-id="9c537-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c537-115">Requirement</span></span> | <span data-ttu-id="9c537-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9c537-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c537-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c537-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9c537-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c537-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9c537-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9c537-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9c537-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9c537-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9c537-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9c537-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c537-122"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c537-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9c537-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9c537-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9c537-124">**\_ Informações de impressora \_ \_ 9W** (Unicode) e **\_ informações de impressora \_ \_ 9a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9c537-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="9c537-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c537-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c537-126">Impressão</span><span class="sxs-lookup"><span data-stu-id="9c537-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9c537-127">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9c537-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9c537-128">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="9c537-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="9c537-129">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="9c537-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="9c537-130">**Informações da impressora \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="9c537-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




