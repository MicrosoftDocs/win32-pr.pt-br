---
description: Representa um driver de impressora no qual dependem outros drivers de impressora.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Estrutura de CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751940"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="1f2c3-103">Estrutura de driver de \_ impressora principal \_</span><span class="sxs-lookup"><span data-stu-id="1f2c3-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="1f2c3-104">Representa um driver de impressora no qual dependem outros drivers de impressora.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2c3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f2c3-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="1f2c3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1f2c3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1f2c3-107">**CoreDriverGUID**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="1f2c3-108">O GUID do driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1f2c3-109">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="1f2c3-110">A data e a hora da versão mais recente do driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1f2c3-111">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1f2c3-112">A ID da versão mais recente do driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1f2c3-113">**\[caminho máximo de szPackageID \_\]**</span><span class="sxs-lookup"><span data-stu-id="1f2c3-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="1f2c3-114">O caminho para o pacote de driver que contém o driver de impressora principal.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f2c3-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f2c3-115">Remarks</span></span>

<span data-ttu-id="1f2c3-116">Essa estrutura pode representar o driver base de um fabricante no qual os drivers para vários modelos de impressora são dependentes.</span><span class="sxs-lookup"><span data-stu-id="1f2c3-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2c3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f2c3-117">Requirements</span></span>



| <span data-ttu-id="1f2c3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f2c3-118">Requirement</span></span> | <span data-ttu-id="1f2c3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1f2c3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2c3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f2c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2c3-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f2c3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1f2c3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f2c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2c3-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f2c3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1f2c3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f2c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f2c3-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2c3-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1f2c3-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1f2c3-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1f2c3-127">**\_ \_ \_ DRIVERW de impressora principal** (Unicode) e **\_ \_ \_ Driver de impressora de núcleo** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1f2c3-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1f2c3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f2c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2c3-129">Impressão</span><span class="sxs-lookup"><span data-stu-id="1f2c3-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1f2c3-130">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1f2c3-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




