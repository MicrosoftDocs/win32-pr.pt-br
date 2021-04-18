---
description: A \_ estrutura informações da impressora \_ 3 especifica as informações de segurança da impressora.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Estrutura de PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812398"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="c307b-103">Estrutura de informações da impressora \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="c307b-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="c307b-104">A **estrutura \_ informações \_ da impressora 3** especifica as informações de segurança da impressora.</span><span class="sxs-lookup"><span data-stu-id="c307b-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c307b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c307b-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="c307b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c307b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c307b-107">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c307b-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="c307b-108">Ponteiro para uma estrutura de [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que especifica as informações de segurança de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="c307b-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c307b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c307b-109">Remarks</span></span>

<span data-ttu-id="c307b-110">A **estrutura \_ informações \_ da impressora 3** permite que um aplicativo obtenha e defina o descritor de segurança de uma impressora.</span><span class="sxs-lookup"><span data-stu-id="c307b-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="c307b-111">O chamador pode fazer isso mesmo que não tenha permissões de impressora específicas, desde que tenha os direitos padrão descritos em [**Setprinter**](setprinter.md) e [**getprinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="c307b-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="c307b-112">Assim, um aplicativo pode negar temporariamente todo o acesso a uma impressora, enquanto permite que o proprietário da impressora tenha acesso à ACL discricionária da impressora.</span><span class="sxs-lookup"><span data-stu-id="c307b-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c307b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c307b-113">Requirements</span></span>



| <span data-ttu-id="c307b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c307b-114">Requirement</span></span> | <span data-ttu-id="c307b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c307b-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c307b-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c307b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c307b-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c307b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c307b-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c307b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c307b-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c307b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c307b-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c307b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c307b-121"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c307b-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c307b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c307b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c307b-123">Impressão</span><span class="sxs-lookup"><span data-stu-id="c307b-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c307b-124">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="c307b-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c307b-125">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="c307b-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="c307b-126">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="c307b-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="c307b-127">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c307b-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c307b-128">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c307b-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="c307b-129">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c307b-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="c307b-130">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="c307b-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

