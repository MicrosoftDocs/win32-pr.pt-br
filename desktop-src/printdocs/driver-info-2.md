---
description: A \_ estrutura informações sobre o driver \_ 2 identifica um driver de impressora, o número de versão do driver, o ambiente para o qual o driver foi gravado, o nome do arquivo no qual o driver está armazenado e assim por diante.
ms.assetid: cca1227d-69b9-44df-8dac-384c2f8843ae
title: Estrutura de DRIVER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_2
- _DRIVER_INFO_2A
- _DRIVER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: a88caf5aa10828b81dccefbe8118b3a57aebce97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787616"
---
# <a name="driver_info_2-structure"></a><span data-ttu-id="28c6d-103">\_Estrutura informações do driver \_ 2</span><span class="sxs-lookup"><span data-stu-id="28c6d-103">DRIVER\_INFO\_2 structure</span></span>

<span data-ttu-id="28c6d-104">A **estrutura \_ informações \_ sobre o driver 2** identifica um driver de impressora, o número de versão do driver, o ambiente para o qual o driver foi gravado, o nome do arquivo no qual o driver está armazenado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="28c6d-104">The **DRIVER\_INFO\_2** structure identifies a printer driver, the driver version number, the environment for which the driver was written, the name of the file in which the driver is stored, and so on.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28c6d-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_2 {
  DWORD  cVersion;
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDriverPath;
  LPTSTR pDataFile;
  LPTSTR pConfigFile;
} DRIVER_INFO_2, *PDRIVER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="28c6d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="28c6d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="28c6d-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="28c6d-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="28c6d-108">A versão do sistema operacional para a qual o driver foi gravado.</span><span class="sxs-lookup"><span data-stu-id="28c6d-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="28c6d-109">O valor com suporte é 3.</span><span class="sxs-lookup"><span data-stu-id="28c6d-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="28c6d-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="28c6d-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="28c6d-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, "QMS 810").</span><span class="sxs-lookup"><span data-stu-id="28c6d-111">A pointer to a null-terminated string that specifies the name of the driver (for example, "QMS 810").</span></span>

</dd> <dt>

<span data-ttu-id="28c6d-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="28c6d-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="28c6d-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64).</span><span class="sxs-lookup"><span data-stu-id="28c6d-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64).</span></span>

</dd> <dt>

<span data-ttu-id="28c6d-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="28c6d-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="28c6d-115">Um ponteiro para cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou caminho completo e nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, "c: \\ drivers \\pscript.dll").</span><span class="sxs-lookup"><span data-stu-id="28c6d-115">A pointer to null-terminated string that specifies a file name or full path and file name for the file that contains the device driver (for example, "c:\\drivers\\pscript.dll").</span></span>

</dd> <dt>

<span data-ttu-id="28c6d-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="28c6d-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="28c6d-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, "c: \\ drivers \\ Qms810. PPD").</span><span class="sxs-lookup"><span data-stu-id="28c6d-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, "c:\\drivers\\Qms810.ppd").</span></span>

</dd> <dt>

<span data-ttu-id="28c6d-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="28c6d-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="28c6d-119">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o Configuration. dll do driver de dispositivo (por exemplo, "c: \\ drivers \\Pscrptui.dll").</span><span class="sxs-lookup"><span data-stu-id="28c6d-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device-driver's configuration .dll (for example, "c:\\drivers\\Pscrptui.dll").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="28c6d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28c6d-120">Requirements</span></span>



| <span data-ttu-id="28c6d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="28c6d-121">Requirement</span></span> | <span data-ttu-id="28c6d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="28c6d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c6d-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c6d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28c6d-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28c6d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="28c6d-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="28c6d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28c6d-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="28c6d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="28c6d-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="28c6d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="28c6d-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="28c6d-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="28c6d-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="28c6d-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="28c6d-130">Informações de driver **\_ \_ \_ 2W** (Unicode) e **\_ informações de driver \_ \_ 2a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="28c6d-130">**\_DRIVER\_INFO\_2W** (Unicode) and **\_DRIVER\_INFO\_2A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="28c6d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="28c6d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28c6d-132">Impressão</span><span class="sxs-lookup"><span data-stu-id="28c6d-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="28c6d-133">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="28c6d-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="28c6d-134">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="28c6d-134">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="28c6d-135">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="28c6d-135">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




