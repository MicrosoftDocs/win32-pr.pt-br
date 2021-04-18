---
description: A \_ estrutura informações sobre o driver \_ 5 contém informações de driver de impressora.
ms.assetid: 6fb63a9f-5227-46a3-97dc-8de1968e9d63
title: Estrutura de DRIVER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_5
- _DRIVER_INFO_5A
- _DRIVER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 11281e69b70b2d87d354138a6313c8bca6673944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790546"
---
# <a name="driver_info_5-structure"></a><span data-ttu-id="53c01-103">Estrutura de informações de DRIVER \_ \_ 5</span><span class="sxs-lookup"><span data-stu-id="53c01-103">DRIVER\_INFO\_5 structure</span></span>

<span data-ttu-id="53c01-104">A **estrutura \_ informações \_ sobre o driver 5** contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="53c01-104">The **DRIVER\_INFO\_5** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="53c01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53c01-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_5 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  DWORD  dwDriverAttributes;
  DWORD  dwConfigVersion;
  DWORD  dwDriverVersion;
} DRIVER_INFO_5, *PDRIVER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="53c01-106">Membros</span><span class="sxs-lookup"><span data-stu-id="53c01-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53c01-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="53c01-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-108">A versão do sistema operacional para a qual o driver foi gravado.</span><span class="sxs-lookup"><span data-stu-id="53c01-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="53c01-109">O valor com suporte é 3.</span><span class="sxs-lookup"><span data-stu-id="53c01-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="53c01-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="53c01-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-111">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="53c01-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="53c01-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="53c01-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-113">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="53c01-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="53c01-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="53c01-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-115">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="53c01-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="53c01-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="53c01-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-117">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="53c01-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="53c01-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="53c01-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-119">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="53c01-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="53c01-120">**dwDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="53c01-120">**dwDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-121">Atributos de driver, como UMPD/KMPD.</span><span class="sxs-lookup"><span data-stu-id="53c01-121">Driver attributes, like UMPD/KMPD.</span></span>

</dd> <dt>

<span data-ttu-id="53c01-122">**dwConfigVersion**</span><span class="sxs-lookup"><span data-stu-id="53c01-122">**dwConfigVersion**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-123">Número de vezes que o arquivo de configuração para este driver foi atualizado ou downgrade desde a última reinicialização do spooler.</span><span class="sxs-lookup"><span data-stu-id="53c01-123">Number of times the configuration file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> <dt>

<span data-ttu-id="53c01-124">**dwDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="53c01-124">**dwDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="53c01-125">Número de vezes que o arquivo de driver para este driver foi atualizado ou downgrade desde a última reinicialização do spooler.</span><span class="sxs-lookup"><span data-stu-id="53c01-125">Number of times the driver file for this driver has been upgraded or downgraded since the last spooler restart.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53c01-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53c01-126">Requirements</span></span>



| <span data-ttu-id="53c01-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="53c01-127">Requirement</span></span> | <span data-ttu-id="53c01-128">Valor</span><span class="sxs-lookup"><span data-stu-id="53c01-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53c01-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53c01-129">Minimum supported client</span></span><br/> | <span data-ttu-id="53c01-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53c01-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53c01-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53c01-131">Minimum supported server</span></span><br/> | <span data-ttu-id="53c01-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53c01-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53c01-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="53c01-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="53c01-134"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53c01-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="53c01-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="53c01-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="53c01-136">**\_ Informações do driver \_ \_ 5W** (Unicode) e **\_ informações do driver \_ \_ 5a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="53c01-136">**\_DRIVER\_INFO\_5W** (Unicode) and **\_DRIVER\_INFO\_5A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="53c01-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="53c01-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c01-138">Impressão</span><span class="sxs-lookup"><span data-stu-id="53c01-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="53c01-139">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="53c01-139">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="53c01-140">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="53c01-140">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="53c01-141">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="53c01-141">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="53c01-142">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="53c01-142">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




