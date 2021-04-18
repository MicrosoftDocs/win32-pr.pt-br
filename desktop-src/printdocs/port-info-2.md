---
description: A \_ estrutura informações sobre a porta \_ 2 identifica uma porta de impressora com suporte.
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: Estrutura de PORT_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813983"
---
# <a name="port_info_2-structure"></a><span data-ttu-id="3aa76-103">Estrutura de informações da porta \_ \_ 2</span><span class="sxs-lookup"><span data-stu-id="3aa76-103">PORT\_INFO\_2 structure</span></span>

<span data-ttu-id="3aa76-104">A **estrutura \_ informações \_ sobre a porta 2** identifica uma porta de impressora com suporte.</span><span class="sxs-lookup"><span data-stu-id="3aa76-104">The **PORT\_INFO\_2** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa76-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aa76-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a><span data-ttu-id="3aa76-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3aa76-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3aa76-107">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="3aa76-107">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="3aa76-108">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica uma porta de impressora com suporte (por exemplo, "LPT1:").</span><span class="sxs-lookup"><span data-stu-id="3aa76-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> <dt>

<span data-ttu-id="3aa76-109">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="3aa76-109">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="3aa76-110">Ponteiro para uma cadeia de caracteres terminada em nulo que identifica um monitor instalado (por exemplo, "Monitor de PJL").</span><span class="sxs-lookup"><span data-stu-id="3aa76-110">Pointer to a null-terminated string that identifies an installed monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="3aa76-111">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3aa76-111">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3aa76-112">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="3aa76-112">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="3aa76-113">Ponteiro para uma cadeia de caracteres terminada em nulo que descreve a porta com mais detalhes (por exemplo, se **pPortName** for "LPT1:", **pDescription** é "porta da impressora").</span><span class="sxs-lookup"><span data-stu-id="3aa76-113">Pointer to a null-terminated string that describes the port in more detail (for example, if **pPortName** is "LPT1:", **pDescription** is "printer port").</span></span> <span data-ttu-id="3aa76-114">Isso pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3aa76-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3aa76-115">**fPortType**</span><span class="sxs-lookup"><span data-stu-id="3aa76-115">**fPortType**</span></span>
</dt> <dd>

<span data-ttu-id="3aa76-116">Bitmask que descreve o tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="3aa76-116">Bitmask describing the type of port.</span></span> <span data-ttu-id="3aa76-117">Esse membro pode ser uma combinação dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3aa76-117">This member can be a combination of the following values:</span></span>

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

<span data-ttu-id="3aa76-118">**\_gravação de tipo de porta \_**</span><span class="sxs-lookup"><span data-stu-id="3aa76-118">**PORT\_TYPE\_WRITE**</span></span>
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

<span data-ttu-id="3aa76-119">**\_leitura do tipo de porta \_**</span><span class="sxs-lookup"><span data-stu-id="3aa76-119">**PORT\_TYPE\_READ**</span></span>
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

<span data-ttu-id="3aa76-120">**tipo de porta \_ \_ Redirecionado**</span><span class="sxs-lookup"><span data-stu-id="3aa76-120">**PORT\_TYPE\_REDIRECTED**</span></span>
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

<span data-ttu-id="3aa76-121">**tipo de porta \_ \_ rede \_ anexada**</span><span class="sxs-lookup"><span data-stu-id="3aa76-121">**PORT\_TYPE\_NET\_ATTACHED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3aa76-122">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3aa76-122">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3aa76-123">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3aa76-123">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3aa76-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aa76-124">Remarks</span></span>

<span data-ttu-id="3aa76-125">Use a **estrutura \_ informações \_ da porta 2** ao chamar [**EnumPorts**](enumports.md) se houver vários monitores instalados que ofereçam suporte às mesmas portas.</span><span class="sxs-lookup"><span data-stu-id="3aa76-125">Use the **PORT\_INFO\_2** structure when calling [**EnumPorts**](enumports.md) if there are multiple monitors installed that support the same ports.</span></span>

<span data-ttu-id="3aa76-126">O membro **fPortType** pode ser consultado para determinar informações sobre a porta.</span><span class="sxs-lookup"><span data-stu-id="3aa76-126">The **fPortType** member can be queried to determine information about the port.</span></span> <span data-ttu-id="3aa76-127">Observe que as configurações de porta não influenciam os atributos da impressora (como retornado pelo membro **Attributes** das [**informações da impressora \_ \_ 2**](printer-info-2.md)).</span><span class="sxs-lookup"><span data-stu-id="3aa76-127">Note that port settings do not influence printer attributes (as returned by the **Attributes** member of [**PRINTER\_INFO\_2**](printer-info-2.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa76-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aa76-128">Requirements</span></span>



| <span data-ttu-id="3aa76-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aa76-129">Requirement</span></span> | <span data-ttu-id="3aa76-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3aa76-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa76-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aa76-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa76-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3aa76-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3aa76-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aa76-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa76-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3aa76-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3aa76-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3aa76-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa76-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa76-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3aa76-137">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3aa76-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3aa76-138">Informações de porta **\_ \_ \_ 2W** (Unicode) e **\_ informação de porta \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3aa76-138">**\_PORT\_INFO\_2W** (Unicode) and **\_PORT\_INFO\_2A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="3aa76-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aa76-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa76-140">Impressão</span><span class="sxs-lookup"><span data-stu-id="3aa76-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3aa76-141">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3aa76-141">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="3aa76-142">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="3aa76-142">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




