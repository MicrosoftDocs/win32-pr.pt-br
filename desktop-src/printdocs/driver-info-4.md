---
description: A \_ estrutura informações sobre o driver \_ 4 contém informações de driver de impressora.
ms.assetid: 63000de6-74e7-4427-98d7-7bbd2dd61080
title: Estrutura de DRIVER_INFO_4 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_4
- _DRIVER_INFO_4A
- _DRIVER_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b737947b19e93a6b8de0563128a0f1be412101ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169344"
---
# <a name="driver_info_4-structure"></a><span data-ttu-id="ad154-103">Estrutura de informações de DRIVER \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="ad154-103">DRIVER\_INFO\_4 structure</span></span>

<span data-ttu-id="ad154-104">A **estrutura \_ informações \_ sobre o driver 4** contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="ad154-104">The **DRIVER\_INFO\_4** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad154-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad154-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_4 {
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
  LPTSTR pszzPreviousNames;
} DRIVER_INFO_4, *PDRIVER_INFO_4;
```



## <a name="members"></a><span data-ttu-id="ad154-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ad154-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad154-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="ad154-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-108">A versão do sistema operacional para a qual o driver foi gravado.</span><span class="sxs-lookup"><span data-stu-id="ad154-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="ad154-109">O valor com suporte é 3.</span><span class="sxs-lookup"><span data-stu-id="ad154-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="ad154-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="ad154-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-111">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="ad154-111">Pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="ad154-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="ad154-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-113">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="ad154-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="ad154-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="ad154-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-115">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou caminho completo e nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="ad154-115">Pointer to a null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ad154-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="ad154-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-117">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="ad154-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="ad154-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="ad154-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-119">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="ad154-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="ad154-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="ad154-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-121">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ad154-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file.</span></span>

</dd> <dt>

<span data-ttu-id="ad154-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="ad154-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-123">Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="ad154-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="ad154-124">Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo do qual o driver depende.</span><span class="sxs-lookup"><span data-stu-id="ad154-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="ad154-125">A sequência de cadeias de caracteres é terminada por uma cadeia de caracteres vazia e de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="ad154-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="ad154-126">Se **pDependentFiles** não for **nulo** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.</span><span class="sxs-lookup"><span data-stu-id="ad154-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="ad154-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="ad154-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-128">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de idioma (por exemplo, um monitor de PJL).</span><span class="sxs-lookup"><span data-stu-id="ad154-128">A pointer to a null-terminated string that specifies a language monitor (for example, PJL monitor).</span></span> <span data-ttu-id="ad154-129">Esse membro pode ser **nulo** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.</span><span class="sxs-lookup"><span data-stu-id="ad154-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="ad154-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="ad154-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-131">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, EMF).</span><span class="sxs-lookup"><span data-stu-id="ad154-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, EMF).</span></span>

</dd> <dt>

<span data-ttu-id="ad154-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="ad154-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="ad154-133">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores que são compatíveis com este driver.</span><span class="sxs-lookup"><span data-stu-id="ad154-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="ad154-134">Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="ad154-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad154-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad154-135">Requirements</span></span>



| <span data-ttu-id="ad154-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad154-136">Requirement</span></span> | <span data-ttu-id="ad154-137">Valor</span><span class="sxs-lookup"><span data-stu-id="ad154-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad154-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad154-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ad154-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ad154-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ad154-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad154-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ad154-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ad154-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ad154-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ad154-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad154-143"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad154-143"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ad154-144">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ad154-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ad154-145">Informações do **\_ Driver \_ \_ 4W** (Unicode) e **\_ info do driver \_ \_ 4a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ad154-145">**\_DRIVER\_INFO\_4W** (Unicode) and **\_DRIVER\_INFO\_4A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ad154-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad154-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad154-147">Impressão</span><span class="sxs-lookup"><span data-stu-id="ad154-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ad154-148">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="ad154-148">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ad154-149">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ad154-149">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="ad154-150">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ad154-150">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="ad154-151">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="ad154-151">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




