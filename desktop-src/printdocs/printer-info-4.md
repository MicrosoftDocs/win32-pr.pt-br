---
description: A \_ estrutura informações da impressora \_ 4 especifica informações gerais sobre a impressora. A estrutura pode ser usada para recuperar informações de impressora mínimas em uma chamada para EnumPrinters.
ms.assetid: 81bd0eab-dc1e-4cf1-8f63-3686f1711c1f
title: Estrutura de PRINTER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_4
- _PRINTER_INFO_4A
- _PRINTER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9a1501008f0235ea303dd1457fc8756c28abc21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170878"
---
# <a name="printer_info_4-structure"></a><span data-ttu-id="ceadf-103">Estrutura de informações da impressora \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="ceadf-103">PRINTER\_INFO\_4 structure</span></span>

<span data-ttu-id="ceadf-104">A **estrutura \_ informações \_ da impressora 4** especifica informações gerais sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="ceadf-104">The **PRINTER\_INFO\_4** structure specifies general printer information.</span></span>

<span data-ttu-id="ceadf-105">A estrutura pode ser usada para recuperar informações de impressora mínimas em uma chamada para [**EnumPrinters**](enumprinters.md).</span><span class="sxs-lookup"><span data-stu-id="ceadf-105">The structure can be used to retrieve minimal printer information on a call to [**EnumPrinters**](enumprinters.md).</span></span> <span data-ttu-id="ceadf-106">Essa chamada é uma maneira rápida e fácil de recuperar os nomes e os atributos de todas as impressoras instaladas localmente em um sistema e todas as conexões de impressora remota que um usuário estabeleceu.</span><span class="sxs-lookup"><span data-stu-id="ceadf-106">Such a call is a fast and easy way to retrieve the names and attributes of all locally installed printers on a system and all remote printer connections that a user has established.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceadf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ceadf-107">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_4 {
  LPTSTR pPrinterName;
  LPTSTR pServerName;
  DWORD  Attributes;
} PRINTER_INFO_4, *PPRINTER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="ceadf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ceadf-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ceadf-109">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="ceadf-109">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="ceadf-110">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora (local ou remota).</span><span class="sxs-lookup"><span data-stu-id="ceadf-110">Pointer to a null-terminated string that specifies the name of the printer (local or remote).</span></span>

</dd> <dt>

<span data-ttu-id="ceadf-111">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="ceadf-111">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="ceadf-112">Ponteiro para uma cadeia de caracteres terminada em nulo que é o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="ceadf-112">Pointer to a null-terminated string that is the name of the server.</span></span>

</dd> <dt>

<span data-ttu-id="ceadf-113">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="ceadf-113">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="ceadf-114">Especifica informações sobre os dados retornados.</span><span class="sxs-lookup"><span data-stu-id="ceadf-114">Specifies information about the returned data.</span></span>



| <span data-ttu-id="ceadf-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ceadf-115">Value</span></span>                       | <span data-ttu-id="ceadf-116">Significado</span><span class="sxs-lookup"><span data-stu-id="ceadf-116">Meaning</span></span>                          |
|-----------------------------|----------------------------------|
| <span data-ttu-id="ceadf-117">atributo de impressora \_ \_ local</span><span class="sxs-lookup"><span data-stu-id="ceadf-117">PRINTER\_ATTRIBUTE\_LOCAL</span></span>   | <span data-ttu-id="ceadf-118">A impressora é uma impressora local.</span><span class="sxs-lookup"><span data-stu-id="ceadf-118">The printer is a local printer.</span></span>  |
| <span data-ttu-id="ceadf-119">\_rede de atributos da impressora \_</span><span class="sxs-lookup"><span data-stu-id="ceadf-119">PRINTER\_ATTRIBUTE\_NETWORK</span></span> | <span data-ttu-id="ceadf-120">A impressora é uma impressora remota.</span><span class="sxs-lookup"><span data-stu-id="ceadf-120">The printer is a remote printer.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ceadf-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceadf-121">Remarks</span></span>

<span data-ttu-id="ceadf-122">A **estrutura \_ informações \_ da impressora 4** fornece uma maneira fácil e rápida de recuperar os nomes das impressoras instaladas em um computador local, bem como as conexões remotas que um usuário estabeleceu.</span><span class="sxs-lookup"><span data-stu-id="ceadf-122">The **PRINTER\_INFO\_4** structure provides an easy and extremely fast way to retrieve the names of the printers installed on a local machine, as well as the remote connections that a user has established.</span></span> <span data-ttu-id="ceadf-123">Quando [**EnumPrinters**](enumprinters.md) é chamado com uma estrutura de dados de **informações de impressora \_ \_ 4** , essa função consulta o registro para obter as informações especificadas e retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="ceadf-123">When [**EnumPrinters**](enumprinters.md) is called with a **PRINTER\_INFO\_4** data structure, that function queries the registry for the specified information, then returns immediately.</span></span> <span data-ttu-id="ceadf-124">Isso difere do comportamento de **EnumPrinters** quando chamado com outros níveis de estruturas de dados de **informações de impressora \_ \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="ceadf-124">This differs from the behavior of **EnumPrinters** when called with other levels of **PRINTER\_INFO\_xxx** data structures.</span></span> <span data-ttu-id="ceadf-125">Em particular, quando **EnumPrinters** é chamado com uma estrutura de dados de nível 2 (**informações da impressora \_ \_ 2** ), ele executa uma chamada **OpenPrinter** em cada conexão remota.</span><span class="sxs-lookup"><span data-stu-id="ceadf-125">In particular, when **EnumPrinters** is called with a level 2 (**PRINTER\_INFO\_2** ) data structure, it performs an **OpenPrinter** call on each remote connection.</span></span> <span data-ttu-id="ceadf-126">Se uma conexão remota estiver inativa, se o servidor remoto não existir mais, ou se a impressora remota não existir mais, a função deverá aguardar o RPC atingir o tempo limite e, consequentemente, falhará na chamada **OpenPrinter** .</span><span class="sxs-lookup"><span data-stu-id="ceadf-126">If a remote connection is down, if the remote server no longer exists, or if the remote printer no longer exists, the function must wait for RPC to time out and consequently fail the **OpenPrinter** call.</span></span> <span data-ttu-id="ceadf-127">Isso pode levar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="ceadf-127">This can take a while.</span></span> <span data-ttu-id="ceadf-128">Passar uma estrutura de **\_ informações sobre a impressora \_ 4** permite que um aplicativo recupere um mínimo de informações necessárias. se forem desejadas informações mais detalhadas, uma chamada subsequente de **EnumPrinter** nível 2 poderá ser feita.</span><span class="sxs-lookup"><span data-stu-id="ceadf-128">Passing a **PRINTER\_INFO\_4** structure lets an application retrieve a bare minimum of required information; if more detailed information is desired, a subsequent **EnumPrinter** level 2 call can be made.</span></span>

<span data-ttu-id="ceadf-129">Os **atributos** também podem conter valores definidos no campo **atributos** das informações da **impressora \_ \_ 2**.</span><span class="sxs-lookup"><span data-stu-id="ceadf-129">**Attributes** can also contain values that are defined in the **Attributes** field of **PRINTER\_INFO\_2**.</span></span>

<span data-ttu-id="ceadf-130">Algumas configurações de impressora, como conexões de impressora para alguns servidores de impressão não baseados no Windows, podem retornar **o \_ atributo \_ de impressora local** e a **\_ \_ rede de atributos de impressora**.</span><span class="sxs-lookup"><span data-stu-id="ceadf-130">Some printer configurations, such as printer connections to some non-Windows-based print servers, might return both **PRINTER\_ATTRIBUTE\_LOCAL** and **PRINTER\_ATTRIBUTE\_NETWORK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ceadf-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ceadf-131">Requirements</span></span>



| <span data-ttu-id="ceadf-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ceadf-132">Requirement</span></span> | <span data-ttu-id="ceadf-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ceadf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceadf-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceadf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ceadf-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ceadf-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ceadf-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ceadf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ceadf-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ceadf-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ceadf-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ceadf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ceadf-139"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ceadf-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ceadf-140">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ceadf-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ceadf-141">Informações de **\_ impressora \_ \_ 4W** (Unicode) e **\_ informações de impressora \_ \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ceadf-141">**\_PRINTER\_INFO\_4W** (Unicode) and **\_PRINTER\_INFO\_4A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="ceadf-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="ceadf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceadf-143">Impressão</span><span class="sxs-lookup"><span data-stu-id="ceadf-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ceadf-144">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="ceadf-144">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ceadf-145">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="ceadf-145">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="ceadf-146">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="ceadf-146">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="ceadf-147">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ceadf-147">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="ceadf-148">**Informações da impressora \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="ceadf-148">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="ceadf-149">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ceadf-149">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="ceadf-150">**Informações da impressora \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="ceadf-150">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> </dl>

 

 




