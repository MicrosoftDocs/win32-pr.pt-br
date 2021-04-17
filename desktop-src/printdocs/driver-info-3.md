---
description: A \_ estrutura informações do driver \_ 3 contém informações de driver de impressora.
ms.assetid: ccf87319-0bcf-4f71-8de3-0190459d2b0e
title: Estrutura de DRIVER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_3
- _DRIVER_INFO_3A
- _DRIVER_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 64509977a85bc33cb13dac4e6ba2817502c06cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791432"
---
# <a name="driver_info_3-structure"></a><span data-ttu-id="9e0fe-103">Estrutura de informações do DRIVER \_ \_ 3</span><span class="sxs-lookup"><span data-stu-id="9e0fe-103">DRIVER\_INFO\_3 structure</span></span>

<span data-ttu-id="9e0fe-104">A **estrutura \_ informações \_ do Driver 3** contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-104">The **DRIVER\_INFO\_3** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e0fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e0fe-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_3 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
  LPTSTR pHelpFile;
  LPTSTR pDependentFiles;
  LPTSTR pMonitorName;
  LPTSTR pDefaultDataType;
} DRIVER_INFO_3, *PDRIVER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="9e0fe-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9e0fe-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9e0fe-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-108">A versão do sistema operacional para a qual o driver foi gravado.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="9e0fe-109">Os valores com suporte são 3 e 4, que representam os drivers v3 e v4, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-109">The supported values are 3 and 4, which represent the V3 and V4 drivers, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="9e0fe-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="9e0fe-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-115">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou caminho completo e nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, "C: \\ DRIVERS \\Pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="9e0fe-115">A pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "C:\\DRIVERS\\Pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, "C: \\ drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="9e0fe-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "C:\\DRIVERS\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-119">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, "C: \\ DRIVERS \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="9e0fe-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, "C:\\DRIVERS\\Pscrptui.dll").</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-121">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-123">Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="9e0fe-124">Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo do qual o driver depende.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="9e0fe-125">A sequência de cadeias de caracteres é terminada por uma cadeia de caracteres vazia e de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="9e0fe-126">Se **pDependentFiles** não for **nulo** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-128">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de idioma (por exemplo, "Monitor de PJL").</span><span class="sxs-lookup"><span data-stu-id="9e0fe-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="9e0fe-129">Esse membro pode ser **nulo** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.</span><span class="sxs-lookup"><span data-stu-id="9e0fe-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="9e0fe-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="9e0fe-131">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").</span><span class="sxs-lookup"><span data-stu-id="9e0fe-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9e0fe-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e0fe-132">Requirements</span></span>



| <span data-ttu-id="9e0fe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e0fe-133">Requirement</span></span> | <span data-ttu-id="9e0fe-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9e0fe-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e0fe-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e0fe-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0fe-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e0fe-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9e0fe-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e0fe-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0fe-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e0fe-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9e0fe-139">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e0fe-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e0fe-140"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e0fe-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9e0fe-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9e0fe-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9e0fe-142">Informações de **\_ Driver \_ \_ 3W** (Unicode) e **\_ info de driver \_ \_ 3a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9e0fe-142">**\_DRIVER\_INFO\_3W** (Unicode) and **\_DRIVER\_INFO\_3A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="9e0fe-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e0fe-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e0fe-144">Impressão</span><span class="sxs-lookup"><span data-stu-id="9e0fe-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9e0fe-145">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9e0fe-145">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9e0fe-146">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-146">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="9e0fe-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="9e0fe-148">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="9e0fe-148">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




