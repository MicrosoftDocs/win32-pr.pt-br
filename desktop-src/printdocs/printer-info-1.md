---
description: A \_ estrutura informações da impressora \_ 1 especifica informações gerais sobre a impressora.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Estrutura de PRINTER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814570"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="ec78e-103">Estrutura de informações da impressora \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="ec78e-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="ec78e-104">A **estrutura \_ informações \_ da impressora 1** especifica informações gerais sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="ec78e-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec78e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec78e-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="ec78e-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ec78e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ec78e-107">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="ec78e-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-108">Especifica informações sobre os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="ec78e-108">Specifies information about the returned data.</span></span> <span data-ttu-id="ec78e-109">A seguir estão os valores para esse membro.</span><span class="sxs-lookup"><span data-stu-id="ec78e-109">Following are the values for this member.</span></span>



| <span data-ttu-id="ec78e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="ec78e-110">Value</span></span>                    | <span data-ttu-id="ec78e-111">Significado</span><span class="sxs-lookup"><span data-stu-id="ec78e-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec78e-112">\_expansão de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="ec78e-113">Um provedor de impressão pode definir esse sinalizador como uma dica para um aplicativo de chamada para enumerar esse objeto posteriormente se a expansão padrão estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="ec78e-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="ec78e-114">Por exemplo, quando os domínios são enumerados, um provedor de impressão pode indicar o domínio do usuário definindo esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="ec78e-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="ec78e-115">\_contêiner de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="ec78e-116">Se esse sinalizador for definido, o objeto de impressora poderá conter objetos enumeráveis.</span><span class="sxs-lookup"><span data-stu-id="ec78e-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="ec78e-117">Por exemplo, o objeto pode ser um servidor de impressão que contém impressoras.</span><span class="sxs-lookup"><span data-stu-id="ec78e-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="ec78e-118">\_ICON1 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="ec78e-119">Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um nome de rede de nível superior, como a rede do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ec78e-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="ec78e-120">\_ICON2 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="ec78e-121">Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um domínio de rede.</span><span class="sxs-lookup"><span data-stu-id="ec78e-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="ec78e-122">\_ICON3 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="ec78e-123">Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="ec78e-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="ec78e-124">\_ICON4 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="ec78e-125">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec78e-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ec78e-126">\_ICON5 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="ec78e-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec78e-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ec78e-128">\_ICON6 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="ec78e-129">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec78e-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ec78e-130">\_ICON7 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="ec78e-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ec78e-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="ec78e-132">\_ICON8 de enumeração de impressora \_</span><span class="sxs-lookup"><span data-stu-id="ec78e-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="ec78e-133">Indica que, quando apropriado, um aplicativo deve exibir um ícone que identifica o objeto como uma impressora.</span><span class="sxs-lookup"><span data-stu-id="ec78e-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="ec78e-134">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="ec78e-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-135">Ponteiro para uma cadeia de caracteres terminada em nulo que descreve o conteúdo da estrutura.</span><span class="sxs-lookup"><span data-stu-id="ec78e-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="ec78e-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-137">Ponteiro para uma cadeia de caracteres terminada em nulo que nomeia o conteúdo da estrutura.</span><span class="sxs-lookup"><span data-stu-id="ec78e-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="ec78e-138">**pComment**</span><span class="sxs-lookup"><span data-stu-id="ec78e-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="ec78e-139">Ponteiro para uma cadeia de caracteres terminada em nulo que contém dados adicionais que descrevem a estrutura.</span><span class="sxs-lookup"><span data-stu-id="ec78e-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec78e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec78e-140">Requirements</span></span>



| <span data-ttu-id="ec78e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec78e-141">Requirement</span></span> | <span data-ttu-id="ec78e-142">Valor</span><span class="sxs-lookup"><span data-stu-id="ec78e-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec78e-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec78e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ec78e-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec78e-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ec78e-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec78e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ec78e-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ec78e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ec78e-147">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ec78e-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec78e-148"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec78e-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ec78e-149">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ec78e-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ec78e-150">**\_ Informações de impressora \_ \_ 1W** (Unicode) e **\_ informações de impressora \_ \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ec78e-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ec78e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec78e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec78e-152">Impressão</span><span class="sxs-lookup"><span data-stu-id="ec78e-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ec78e-153">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="ec78e-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ec78e-154">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="ec78e-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ec78e-155">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="ec78e-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="ec78e-156">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ec78e-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="ec78e-157">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ec78e-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="ec78e-158">**Informações da impressora \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="ec78e-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




