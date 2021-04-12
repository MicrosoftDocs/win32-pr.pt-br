---
description: Contém informações de driver de impressora.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Estrutura de DRIVER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297467"
---
# <a name="driver_info_8-structure"></a><span data-ttu-id="7ed66-103">Estrutura de informações de DRIVER \_ \_ 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-103">DRIVER\_INFO\_8 structure</span></span>

<span data-ttu-id="7ed66-104">Contém informações de driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="7ed66-104">Contains printer driver information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ed66-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ed66-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_8 {
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
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="7ed66-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7ed66-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7ed66-107">**cVersion**</span><span class="sxs-lookup"><span data-stu-id="7ed66-107">**cVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-108">A versão do sistema operacional para a qual o driver foi gravado.</span><span class="sxs-lookup"><span data-stu-id="7ed66-108">The operating system version for which the driver was written.</span></span> <span data-ttu-id="7ed66-109">O valor com suporte é 3.</span><span class="sxs-lookup"><span data-stu-id="7ed66-109">The supported value is 3.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-110">**pName**</span><span class="sxs-lookup"><span data-stu-id="7ed66-110">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).</span><span class="sxs-lookup"><span data-stu-id="7ed66-111">A pointer to a null-terminated string that specifies the name of the driver (for example, QMS 810).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-112">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="7ed66-112">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64.</span><span class="sxs-lookup"><span data-stu-id="7ed66-113">A pointer to a null-terminated string that specifies the environment for which the driver was written (for example, Windows x86, Windows IA64, and Windows x64.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-114">**pDriverPath**</span><span class="sxs-lookup"><span data-stu-id="7ed66-114">**pDriverPath**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-115">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).</span><span class="sxs-lookup"><span data-stu-id="7ed66-115">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains the device driver (for example, C:\\DRIVERS\\Pscript.dll).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-116">**pDataFile**</span><span class="sxs-lookup"><span data-stu-id="7ed66-116">**pDataFile**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, C: \\ drivers \\ Qms810. PPD).</span><span class="sxs-lookup"><span data-stu-id="7ed66-117">A pointer to a null-terminated string that specifies a file name or a full path and file name for the file that contains driver data (for example, C:\\DRIVERS\\Qms810.ppd).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-118">**pConfigFile**</span><span class="sxs-lookup"><span data-stu-id="7ed66-118">**pConfigFile**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-119">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).</span><span class="sxs-lookup"><span data-stu-id="7ed66-119">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's configuration dynamic-link library (for example, C:\\DRIVERS\\Pscrptui.dll).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-120">**pHelpFile**</span><span class="sxs-lookup"><span data-stu-id="7ed66-120">**pHelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-121">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo (por exemplo, C: \\ drivers \\ pscrptui. hlp).</span><span class="sxs-lookup"><span data-stu-id="7ed66-121">A pointer to a null-terminated string that specifies a file name or a full path and file name for the device driver's help file (for example, C:\\DRIVERS\\Pscrptui.hlp).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-122">**pDependentFiles**</span><span class="sxs-lookup"><span data-stu-id="7ed66-122">**pDependentFiles**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-123">Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="7ed66-123">A pointer to a MultiSZ buffer that contains a sequence of null-terminated strings.</span></span> <span data-ttu-id="7ed66-124">Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo do qual o driver depende.</span><span class="sxs-lookup"><span data-stu-id="7ed66-124">Each null-terminated string in the buffer contains the name of a file the driver depends on.</span></span> <span data-ttu-id="7ed66-125">A sequência de cadeias de caracteres é terminada por uma cadeia de caracteres vazia e de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="7ed66-125">The sequence of strings is terminated by an empty, zero-length string.</span></span> <span data-ttu-id="7ed66-126">Se **pDependentFiles** não for **nulo** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.</span><span class="sxs-lookup"><span data-stu-id="7ed66-126">If **pDependentFiles** is not **NULL** and does not contain any file names, it will point to a buffer that contains two empty strings.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-127">**pMonitorName**</span><span class="sxs-lookup"><span data-stu-id="7ed66-127">**pMonitorName**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-128">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de idioma (por exemplo, "Monitor de PJL").</span><span class="sxs-lookup"><span data-stu-id="7ed66-128">A pointer to a null-terminated string that specifies a language monitor (for example, "PJL monitor").</span></span> <span data-ttu-id="7ed66-129">Esse membro pode ser **nulo** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.</span><span class="sxs-lookup"><span data-stu-id="7ed66-129">This member can be **NULL** and should be specified only for printers capable of bidirectional communication.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-130">**pDefaultDataType**</span><span class="sxs-lookup"><span data-stu-id="7ed66-130">**pDefaultDataType**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-131">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").</span><span class="sxs-lookup"><span data-stu-id="7ed66-131">A pointer to a null-terminated string that specifies the default data type of the print job (for example, "EMF").</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-132">**pszzPreviousNames**</span><span class="sxs-lookup"><span data-stu-id="7ed66-132">**pszzPreviousNames**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-133">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores que são compatíveis com este driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-133">A pointer to a null-terminated string that specifies previous printer driver names that are compatible with this driver.</span></span> <span data-ttu-id="7ed66-134">Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.</span><span class="sxs-lookup"><span data-stu-id="7ed66-134">For example, OldName1\\0OldName2\\0\\0.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-135">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="7ed66-135">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-136">A data do pacote de driver, conforme codificado nos arquivos de driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-136">The date of the driver package, as coded in the driver files.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-137">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="7ed66-137">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-138">O número de versão do driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-138">The version number of the driver.</span></span> <span data-ttu-id="7ed66-139">Isso é proveniente da estrutura de versão do driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-139">This comes from the version structure of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-140">**pszMfgName**</span><span class="sxs-lookup"><span data-stu-id="7ed66-140">**pszMfgName**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-141">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do fabricante.</span><span class="sxs-lookup"><span data-stu-id="7ed66-141">A pointer to a null-terminated string that specifies the manufacturer's name.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-142">**pszOEMUrl**</span><span class="sxs-lookup"><span data-stu-id="7ed66-142">**pszOEMUrl**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-143">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL para o fabricante.</span><span class="sxs-lookup"><span data-stu-id="7ed66-143">A pointer to a null-terminated string that specifies the URL for the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-144">**pszHardwareID**</span><span class="sxs-lookup"><span data-stu-id="7ed66-144">**pszHardwareID**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-145">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a ID de hardware para o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="7ed66-145">A pointer to a null-terminated string that specifies the hardware ID for the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-146">**pszProvider**</span><span class="sxs-lookup"><span data-stu-id="7ed66-146">**pszProvider**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-147">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o provedor do driver de impressora (por exemplo, "Microsoft Windows 2000").</span><span class="sxs-lookup"><span data-stu-id="7ed66-147">A pointer to a null-terminated string that specifies the provider of the printer driver (for example, "Microsoft Windows 2000").</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-148">**pszPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="7ed66-148">**pszPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-149">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o processador de impressão (por exemplo, "WinPrint").</span><span class="sxs-lookup"><span data-stu-id="7ed66-149">A pointer to a null-terminated string that specifies the print processor (for example, "WinPrint").</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-150">**pszVendorSetup**</span><span class="sxs-lookup"><span data-stu-id="7ed66-150">**pszVendorSetup**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-151">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a DLL de instalação do driver do fornecedor e o ponto de entrada.</span><span class="sxs-lookup"><span data-stu-id="7ed66-151">A pointer to a null-terminated string that specifies the vendor's driver setup DLL and entry point.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-152">**pszzColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="7ed66-152">**pszzColorProfiles**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-153">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os perfis de cor associados ao driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-153">A pointer to a null-terminated string that specifies the color profiles associated with the driver.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-154">**pszInfPath**</span><span class="sxs-lookup"><span data-stu-id="7ed66-154">**pszInfPath**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-155">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o caminho para o arquivo. inf do driver no repositório de drivers.</span><span class="sxs-lookup"><span data-stu-id="7ed66-155">A pointer to a null-terminated string that specifies the path to the driver's .inf file in the driver store.</span></span> <span data-ttu-id="7ed66-156">(Consulte comentários.) Isso deverá ser **nulo** se as informações do driver \_ \_ 8 estiverem sendo passadas para [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="7ed66-156">(See Remarks.) This must be **NULL** if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-157">**dwPrinterDriverAttributes**</span><span class="sxs-lookup"><span data-stu-id="7ed66-157">**dwPrinterDriverAttributes**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-158">Sinalizadores de atributo para drivers de impressora.</span><span class="sxs-lookup"><span data-stu-id="7ed66-158">Attribute flags for printer drivers.</span></span> <span data-ttu-id="7ed66-159">Isso deve ser 0 se as informações de DRIVER \_ \_ 8 estiverem sendo passadas para [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="7ed66-159">This must be 0 if the DRIVER\_INFO\_8 is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span> <span data-ttu-id="7ed66-160">Caso contrário, pode ser qualquer combinação dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="7ed66-160">Otherwise, it can be any combination of the following flags:</span></span>



| <span data-ttu-id="7ed66-161">Nome/valor do sinalizador</span><span class="sxs-lookup"><span data-stu-id="7ed66-161">Flag name/value</span></span>                                                         | <span data-ttu-id="7ed66-162">Significado</span><span class="sxs-lookup"><span data-stu-id="7ed66-162">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="7ed66-163">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="7ed66-163">Minimum OS</span></span>                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="7ed66-164">\_reconhecimento de \_ pacote de driver de impressora \_</span><span class="sxs-lookup"><span data-stu-id="7ed66-164">PRINTER\_DRIVER\_PACKAGE\_AWARE</span></span><br/> <span data-ttu-id="7ed66-165">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7ed66-165">0x00000001</span></span><br/>        | <span data-ttu-id="7ed66-166">O driver de impressora faz parte de um pacote de driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-166">The printer driver is part of a driver package.</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="7ed66-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ed66-167">Windows Vista</span></span>                                          |
| <span data-ttu-id="7ed66-168">Driver de impressora \_ \_ XPS</span><span class="sxs-lookup"><span data-stu-id="7ed66-168">PRINTER\_DRIVER\_XPS</span></span><br/> <span data-ttu-id="7ed66-169">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7ed66-169">0x00000002</span></span><br/>                   | <span data-ttu-id="7ed66-170">O driver de impressora dá suporte ao formato XPS da Microsoft descrito no [XML Paper Specification: visão geral](/previous-versions/windows/hardware/design/dn641615(v=vs.85))e também no [comportamento do produto, seção <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="7ed66-170">The printer driver supports the Microsoft XPS format described in the [XML Paper Specification: Overview](/previous-versions/windows/hardware/design/dn641615(v=vs.85)), and also in [Product Behavior, section <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span>                        | <span data-ttu-id="7ed66-171">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-171">Windows 8</span></span><br/> <span data-ttu-id="7ed66-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-172">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-173">\_área restrita do driver de impressora \_ \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="7ed66-173">PRINTER\_DRIVER\_SANDBOX\_ENABLED</span></span><br/> <span data-ttu-id="7ed66-174">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7ed66-174">0x00000004</span></span><br/>      | <span data-ttu-id="7ed66-175">O driver de impressora é compatível com o [isolamento de driver de impressora](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-175">The printer driver is compatible with [printer driver isolation](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span> <span data-ttu-id="7ed66-176">Para obter mais informações, consulte o [comportamento do produto, seção <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span><span class="sxs-lookup"><span data-stu-id="7ed66-176">For more information, see [Product Behavior, section <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).</span></span> | <span data-ttu-id="7ed66-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7ed66-177">Windows 7</span></span><br/> <span data-ttu-id="7ed66-178">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7ed66-178">Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="7ed66-179">\_classe de driver de impressora \_</span><span class="sxs-lookup"><span data-stu-id="7ed66-179">PRINTER\_DRIVER\_CLASS</span></span><br/> <span data-ttu-id="7ed66-180">0x00000008</span><span class="sxs-lookup"><span data-stu-id="7ed66-180">0x00000008</span></span><br/>                 | <span data-ttu-id="7ed66-181">O driver de impressora é um [Driver de impressora de classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-181">The printer driver is a [class printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                       | <span data-ttu-id="7ed66-182">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-182">Windows 8</span></span><br/> <span data-ttu-id="7ed66-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-183">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-184">Driver de impressora \_ \_ derivado</span><span class="sxs-lookup"><span data-stu-id="7ed66-184">PRINTER\_DRIVER\_DERIVED</span></span><br/> <span data-ttu-id="7ed66-185">0x00000010</span><span class="sxs-lookup"><span data-stu-id="7ed66-185">0x00000010</span></span><br/>               | <span data-ttu-id="7ed66-186">O driver de impressora é um [Driver de impressora derivado](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-186">The printer driver is a [derived printer driver](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                   | <span data-ttu-id="7ed66-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-187">Windows 8</span></span><br/> <span data-ttu-id="7ed66-188">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-188">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-189">Driver de impressora \_ \_ não \_ compartilhável</span><span class="sxs-lookup"><span data-stu-id="7ed66-189">PRINTER\_DRIVER\_NOT\_SHAREABLE</span></span><br/> <span data-ttu-id="7ed66-190">0x00000020</span><span class="sxs-lookup"><span data-stu-id="7ed66-190">0x00000020</span></span><br/>        | <span data-ttu-id="7ed66-191">As impressoras que usam este driver de impressora não podem ser compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="7ed66-191">Printers using this printer driver cannot be shared.</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="7ed66-192">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-192">Windows 8</span></span><br/> <span data-ttu-id="7ed66-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-193">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-194">\_fax de \_ categoria de driver de impressora \_</span><span class="sxs-lookup"><span data-stu-id="7ed66-194">PRINTER\_DRIVER\_CATEGORY\_FAX</span></span><br/> <span data-ttu-id="7ed66-195">0x00000040</span><span class="sxs-lookup"><span data-stu-id="7ed66-195">0x00000040</span></span><br/>         | <span data-ttu-id="7ed66-196">O driver de impressora destina-se ao uso com [impressoras de fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-196">The printer driver is intended for use with [fax printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                    | <span data-ttu-id="7ed66-197">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-197">Windows 8</span></span><br/> <span data-ttu-id="7ed66-198">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-198">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-199">\_arquivo de \_ categoria do driver de impressora \_</span><span class="sxs-lookup"><span data-stu-id="7ed66-199">PRINTER\_DRIVER\_CATEGORY\_FILE</span></span><br/> <span data-ttu-id="7ed66-200">0x00000080</span><span class="sxs-lookup"><span data-stu-id="7ed66-200">0x00000080</span></span><br/>        | <span data-ttu-id="7ed66-201">O driver de impressora destina-se ao uso com [impressoras de arquivo](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-201">The printer driver is intended for use with [file printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                                  | <span data-ttu-id="7ed66-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-202">Windows 8</span></span><br/> <span data-ttu-id="7ed66-203">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-203">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-204">Categoria de driver de impressora \_ \_ \_ virtual</span><span class="sxs-lookup"><span data-stu-id="7ed66-204">PRINTER\_DRIVER\_CATEGORY\_VIRTUAL</span></span><br/> <span data-ttu-id="7ed66-205">0x00000100</span><span class="sxs-lookup"><span data-stu-id="7ed66-205">0x00000100</span></span><br/>     | <span data-ttu-id="7ed66-206">O driver de impressora destina-se ao uso com [Impressoras virtuais](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-206">The printer driver is intended for use with [virtual printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="7ed66-207">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-207">Windows 8</span></span><br/> <span data-ttu-id="7ed66-208">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-208">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-209">\_serviço de \_ categoria de driver de impressora \_</span><span class="sxs-lookup"><span data-stu-id="7ed66-209">PRINTER\_DRIVER\_CATEGORY\_SERVICE</span></span><br/> <span data-ttu-id="7ed66-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="7ed66-210">0x00000200</span></span><br/>     | <span data-ttu-id="7ed66-211">O driver de impressora destina-se ao uso com [impressoras de serviço](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span><span class="sxs-lookup"><span data-stu-id="7ed66-211">The printer driver is intended for use with [service printers](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).</span></span>                                                                                                                                                                            | <span data-ttu-id="7ed66-212">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-212">Windows 8</span></span><br/> <span data-ttu-id="7ed66-213">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-213">Windows Server 2012</span></span><br/>    |
| <span data-ttu-id="7ed66-214">\_redefinição reversível de driver de impressora \_ \_ \_ necessária</span><span class="sxs-lookup"><span data-stu-id="7ed66-214">PRINTER\_DRIVER\_SOFT\_RESET\_REQUIRED</span></span><br/> <span data-ttu-id="7ed66-215">0x00000400</span><span class="sxs-lookup"><span data-stu-id="7ed66-215">0x00000400</span></span><br/> | <span data-ttu-id="7ed66-216">As impressoras que usam esse driver de impressora devem seguir as diretrizes descritas na definição de classe de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="7ed66-216">Printers that use this printer driver should follow the guidelines outlined in the USB Device Class Definition.</span></span> <span data-ttu-id="7ed66-217">Para obter mais informações, consulte o [comportamento do produto, seção <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span><span class="sxs-lookup"><span data-stu-id="7ed66-217">For more information, see [Product Behavior, section <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)</span></span>                                                                      | <span data-ttu-id="7ed66-218">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7ed66-218">Windows 8</span></span><br/> <span data-ttu-id="7ed66-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7ed66-219">Windows Server 2012</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="7ed66-220">**pszzCoreDriverDependencies**</span><span class="sxs-lookup"><span data-stu-id="7ed66-220">**pszzCoreDriverDependencies**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-221">Um ponteiro para uma cadeia de caracteres múltipla terminada em nulo que especifica todos os drivers de impressora principal dos quais o driver depende.</span><span class="sxs-lookup"><span data-stu-id="7ed66-221">A pointer to a null-terminated multi-string that specifies all the core printer drivers that the driver depends on.</span></span> <span data-ttu-id="7ed66-222">Isso deverá ser **nulo** se as **informações do driver \_ \_ 8** estiverem sendo passadas para [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).</span><span class="sxs-lookup"><span data-stu-id="7ed66-222">This must be **NULL** if the **DRIVER\_INFO\_8** is being passed to [**AddPrinterDriver**](addprinterdriver.md) or [**AddPrinterDriverEx**](addprinterdriverex.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-223">**ftMinInboxDriverVerDate**</span><span class="sxs-lookup"><span data-stu-id="7ed66-223">**ftMinInboxDriverVerDate**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-224">A data mais antiga permitida de quaisquer drivers fornecidos com o Windows e com os quais esse driver depende.</span><span class="sxs-lookup"><span data-stu-id="7ed66-224">The earliest allowed date of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> <dt>

<span data-ttu-id="7ed66-225">**dwlMinInboxDriverVerVersion**</span><span class="sxs-lookup"><span data-stu-id="7ed66-225">**dwlMinInboxDriverVerVersion**</span></span>
</dt> <dd>

<span data-ttu-id="7ed66-226">A versão mais antiga permitida de quaisquer drivers fornecidos com o Windows e com os quais esse driver depende.</span><span class="sxs-lookup"><span data-stu-id="7ed66-226">The earliest allowed version of any drivers that shipped with Windows and on which this driver depends.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ed66-227">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ed66-227">Remarks</span></span>

<span data-ttu-id="7ed66-228">As cadeias de caracteres para esses membros estão contidas no arquivo. inf que é usado para adicionar o driver.</span><span class="sxs-lookup"><span data-stu-id="7ed66-228">The strings for these members are contained in the .inf file that is used to add the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ed66-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ed66-229">Requirements</span></span>



| <span data-ttu-id="7ed66-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ed66-230">Requirement</span></span> | <span data-ttu-id="7ed66-231">Valor</span><span class="sxs-lookup"><span data-stu-id="7ed66-231">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed66-232">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ed66-232">Minimum supported client</span></span><br/> | <span data-ttu-id="7ed66-233">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ed66-233">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7ed66-234">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ed66-234">Minimum supported server</span></span><br/> | <span data-ttu-id="7ed66-235">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ed66-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ed66-236">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ed66-236">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ed66-237"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ed66-237"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7ed66-238">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7ed66-238">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7ed66-239">**\_ Informações do driver \_ \_ 8W** (Unicode) e **\_ informações do driver \_ \_ 8a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7ed66-239">**\_DRIVER\_INFO\_8W** (Unicode) and **\_DRIVER\_INFO\_8A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="7ed66-240">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ed66-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ed66-241">Impressão</span><span class="sxs-lookup"><span data-stu-id="7ed66-241">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7ed66-242">Estruturas de API do spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="7ed66-242">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7ed66-243">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="7ed66-243">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="7ed66-244">**AddPrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="7ed66-244">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> </dl>

 

