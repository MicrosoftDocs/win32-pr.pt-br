---
description: A \_ estrutura informações sobre o driver \_ 6 contém informações de driver de impressora.
ms.assetid: 9771cbb5-caaa-4b7d-9a96-d24234440bac
title: Estrutura de DRIVER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_6
- _DRIVER_INFO_6A
- _DRIVER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20edef2aca2c6948984f5195b16711b78112354a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807266"
---
# <a name="driver_info_6-structure"></a><span data-ttu-id="1deba-103">Estrutura de informações do DRIVER \_ \_ 6</span><span class="sxs-lookup"><span data-stu-id="1deba-103">DRIVER\_INFO\_6 structure</span></span>

<span data-ttu-id="1deba-104">A **estrutura \_ informações \_ sobre o driver 6** contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1deba-104">The **DRIVER\_INFO\_6** structure contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1deba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1deba-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_6 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
} DRIVER_INFO_6, *PDRIVER_INFO_6, *LPDRIVER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="1deba-106">Membros</span><span class="sxs-lookup"><span data-stu-id="1deba-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1deba-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="1deba-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-108">A versão do sistema operacional para a qual o driver foi gravado.</span><span class="sxs-lookup"><span data-stu-id="1deba-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="1deba-109">O valor com suporte é 3.</span><span class="sxs-lookup"><span data-stu-id="1deba-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="1deba-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-111">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="1deba-111">Pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="1deba-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="1deba-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-113">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows NT x86, Windows IA64 e Windows x64.</span><span class="sxs-lookup"><span data-stu-id="1deba-113">Pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows NT x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="1deba-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-115">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="1deba-115">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="1deba-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="1deba-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-117">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="1deba-117">Pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="1deba-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="1deba-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-119">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="1deba-119">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="1deba-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="1deba-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-121">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo (por exemplo, C: \\ drivers \\ pscrptui. hlp).</span><span class="sxs-lookup"><span data-stu-id="1deba-121">Pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="1deba-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="1deba-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-123">Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="1deba-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="1deba-124">Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo do qual o driver depende.</span><span class="sxs-lookup"><span data-stu-id="1deba-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="1deba-125">A sequência de cadeias de caracteres é terminada por uma cadeia de caracteres vazia e de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="1deba-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="1deba-126">Se **pDependentFiles** não for **nulo** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.</span><span class="sxs-lookup"><span data-stu-id="1deba-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="1deba-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-128">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de idioma (por exemplo, "Monitor de PJL").</span><span class="sxs-lookup"><span data-stu-id="1deba-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="1deba-129">Esse membro pode ser **nulo** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.</span><span class="sxs-lookup"><span data-stu-id="1deba-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="1deba-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-131">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").</span><span class="sxs-lookup"><span data-stu-id="1deba-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="1deba-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="1deba-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-133">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores que são compatíveis com este driver.</span><span class="sxs-lookup"><span data-stu-id="1deba-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="1deba-134">Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="1deba-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="1deba-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-136">A data do pacote de driver, conforme codificado nos arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="1deba-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="1deba-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-138">Número de versão do driver.</span><span class="sxs-lookup"><span data-stu-id="1deba-138">Version number of the driver.</span></span> <span data-ttu-id="1deba-139">Isso sai da estrutura de versão do driver.</span><span class="sxs-lookup"><span data-stu-id="1deba-139">This comes out of the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="1deba-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-141">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="1deba-141">Pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="1deba-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-143">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="1deba-143">Pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="1deba-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-145">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica a ID de hardware para o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="1deba-145">Pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="1deba-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="1deba-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="1deba-147">Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o provedor do driver de impressora (por exemplo, "Microsoft Windows 2000")</span><span class="sxs-lookup"><span data-stu-id="1deba-147">Pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000")</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1deba-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="1deba-148">Remarks</span></span>

<span data-ttu-id="1deba-149">As cadeias de caracteres para esses membros estão contidas no arquivo. inf que é usado para adicionar o driver.</span><span class="sxs-lookup"><span data-stu-id="1deba-149">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

<span data-ttu-id="1deba-150">Se você chamar [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md) com *nível* diferente de 6 e, em seguida, chamar [**GetPrinterDriver**](getprinterdriver.md) ou [**EnumPrinterDrivers**](enumprinterdrivers.md) com o *nível* igual a 6, a estrutura **informações do driver \_ \_ 6** será retornada com **pszMfgName**, **pszOEMUrl**, **pszHardwareID** e **pszProvider** definida como **NULL**, **dwlDriverVersion** definida como 0 e **ftDriverDate** definida como (0, 0).</span><span class="sxs-lookup"><span data-stu-id="1deba-150">If you call [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md) with *Level* not equal to 6, and then you call [**GetPrinterDriver**](getprinterdriver.md) or [**EnumPrinterDrivers**](enumprinterdrivers.md) with *Level* equal to 6, the **DRIVER\_INFO\_6** structure is returned with **pszMfgName**, **pszOEMUrl**, **pszHardwareID**, and **pszProvider** set to **NULL**, **dwlDriverVersion** set to 0, and **ftDriverDate** set to (0,0).</span></span>

## <a name="requirements"></a><span data-ttu-id="1deba-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1deba-151">Requirements</span></span>



| <span data-ttu-id="1deba-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="1deba-152">Requirement</span></span> | <span data-ttu-id="1deba-153">Valor</span><span class="sxs-lookup"><span data-stu-id="1deba-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1deba-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1deba-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1deba-155">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1deba-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1deba-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1deba-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1deba-157">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1deba-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1deba-158">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1deba-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="1deba-159"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1deba-159"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1deba-160">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="1deba-160">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1deba-161">Informações do **\_ Driver \_ \_ 6W** (Unicode) e **\_ info do driver \_ \_ 6a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1deba-161">**\_DRIVER\_INFO\_6W** (Unicode) and **\_DRIVER\_INFO\_6A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="1deba-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="1deba-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1deba-163">Impressão</span><span class="sxs-lookup"><span data-stu-id="1deba-163">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1deba-164">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="1deba-164">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="1deba-165">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1deba-165">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="1deba-166">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="1deba-166">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="1deba-167">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="1deba-167">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="1deba-168">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="1deba-168">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

 




