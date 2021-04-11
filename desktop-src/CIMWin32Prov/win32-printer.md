---
description: Representa um dispositivo conectado a um computador que está sendo executado em um sistema operacional Microsoft Windows que pode produzir uma imagem ou um texto impresso no papel ou em outra mídia.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164039"
---
# <a name="win32_printer-class"></a><span data-ttu-id="080af-103">\_Classe de impressora Win32</span><span class="sxs-lookup"><span data-stu-id="080af-103">Win32\_Printer class</span></span>

<span data-ttu-id="080af-104">A [classe WMI](../wmisdk/retrieving-a-class.md) da **\_ impressora Win32** representa um dispositivo conectado a um computador executado em um sistema operacional Microsoft Windows que pode produzir uma imagem ou texto impresso no papel ou em outra mídia.</span><span class="sxs-lookup"><span data-stu-id="080af-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="080af-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="080af-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="080af-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="080af-106">Syntax</span></span>

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a><span data-ttu-id="080af-107">Membros</span><span class="sxs-lookup"><span data-stu-id="080af-107">Members</span></span>

<span data-ttu-id="080af-108">A classe de **\_ impressora do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="080af-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="080af-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="080af-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="080af-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="080af-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="080af-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="080af-111">Methods</span></span>

<span data-ttu-id="080af-112">A classe de **\_ impressora Win32** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="080af-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="080af-113">Método</span><span class="sxs-lookup"><span data-stu-id="080af-113">Method</span></span>                                                                               | <span data-ttu-id="080af-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="080af-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="080af-115">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="080af-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="080af-116">Adiciona uma conexão à impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="080af-117">**CancelAllJobs**</span><span class="sxs-lookup"><span data-stu-id="080af-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="080af-118">Cancela todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="080af-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="080af-119">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="080af-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="080af-120">Retorna o descritor de segurança que controla o acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="080af-121">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="080af-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="080af-122">Pausa a fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="080af-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="080af-123">**PrintTestPage**</span><span class="sxs-lookup"><span data-stu-id="080af-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="080af-124">Imprime uma página de teste.</span><span class="sxs-lookup"><span data-stu-id="080af-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="080af-125">**RenamePrinter**</span><span class="sxs-lookup"><span data-stu-id="080af-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="080af-126">Renomeia uma impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="080af-127">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="080af-127">**Reset**</span></span>                                                                            | <span data-ttu-id="080af-128">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="080af-128">Not implemented.</span></span> <span data-ttu-id="080af-129">Para obter mais informações sobre como implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) na [**\_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="080af-130">**Retomar**</span><span class="sxs-lookup"><span data-stu-id="080af-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="080af-131">Retoma a fila de impressão em pausa.</span><span class="sxs-lookup"><span data-stu-id="080af-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="080af-132">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="080af-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="080af-133">Define a impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="080af-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="080af-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="080af-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="080af-135">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="080af-135">Not implemented.</span></span> <span data-ttu-id="080af-136">Para obter mais informações sobre como implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) na [**\_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="080af-137">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="080af-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="080af-138">Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="080af-139">Propriedades</span><span class="sxs-lookup"><span data-stu-id="080af-139">Properties</span></span>

<span data-ttu-id="080af-140">A classe de **\_ impressora Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="080af-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="080af-141">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="080af-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-144">Bitmap de atributos para um dispositivo de impressão baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="080af-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="080af-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Impressora \_ ATRIBUTO \_ na fila** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="080af-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="080af-146">Em fila</span><span class="sxs-lookup"><span data-stu-id="080af-146">Queued</span></span>

<span data-ttu-id="080af-147">Os trabalhos de impressão são armazenados em buffer e colocados em fila.</span><span class="sxs-lookup"><span data-stu-id="080af-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="080af-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Impressora \_ ATRIBUTO \_ direto** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="080af-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="080af-149">Direto</span><span class="sxs-lookup"><span data-stu-id="080af-149">Direct</span></span>

<span data-ttu-id="080af-150">Documento a ser enviado diretamente para a impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="080af-151">Esse valor será usado se os trabalhos de impressão não estiverem na fila corretamente.</span><span class="sxs-lookup"><span data-stu-id="080af-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="080af-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Impressora \_ ATRIBUTO \_ padrão** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="080af-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="080af-153">Padrão</span><span class="sxs-lookup"><span data-stu-id="080af-153">Default</span></span>

<span data-ttu-id="080af-154">Impressora padrão em um computador.</span><span class="sxs-lookup"><span data-stu-id="080af-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="080af-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Impressora \_ ATRIBUTO \_ compartilhado** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="080af-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="080af-156">Compartilhado</span><span class="sxs-lookup"><span data-stu-id="080af-156">Shared</span></span>

<span data-ttu-id="080af-157">Disponível como um recurso de rede compartilhado.</span><span class="sxs-lookup"><span data-stu-id="080af-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="080af-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Impressora \_ \_Rede de atributos** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="080af-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="080af-159">Rede</span><span class="sxs-lookup"><span data-stu-id="080af-159">Network</span></span>

<span data-ttu-id="080af-160">Anexado a uma rede.</span><span class="sxs-lookup"><span data-stu-id="080af-160">Attached to a network.</span></span> <span data-ttu-id="080af-161">Se os bits locais e de rede estiverem definidos, isso indicará uma impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="080af-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Impressora \_ ATRIBUTO \_ oculto** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="080af-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="080af-163">Hidden</span><span class="sxs-lookup"><span data-stu-id="080af-163">Hidden</span></span>

<span data-ttu-id="080af-164">Oculto de alguns usuários na rede.</span><span class="sxs-lookup"><span data-stu-id="080af-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="080af-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Impressora \_ ATRIBUTO \_ local** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="080af-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="080af-166">Local</span><span class="sxs-lookup"><span data-stu-id="080af-166">Local</span></span>

<span data-ttu-id="080af-167">Conectado diretamente a um computador.</span><span class="sxs-lookup"><span data-stu-id="080af-167">Directly connected to a computer.</span></span> <span data-ttu-id="080af-168">Se os bits locais e de rede estiverem definidos, isso indicará uma impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="080af-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Impressora \_ ATRIBUTO \_ ENABLEDEVQ** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="080af-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="080af-170">EnableDevQ</span><span class="sxs-lookup"><span data-stu-id="080af-170">EnableDevQ</span></span>

<span data-ttu-id="080af-171">Habilite a fila na impressora, se disponível.</span><span class="sxs-lookup"><span data-stu-id="080af-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="080af-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Impressora \_ ATRIBUTO \_ KEEPPRINTEDJOBS** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="080af-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="080af-173">KeepPrintedJobs</span><span class="sxs-lookup"><span data-stu-id="080af-173">KeepPrintedJobs</span></span>

<span data-ttu-id="080af-174">O spooler não deve excluir documentos depois que eles são impressos.</span><span class="sxs-lookup"><span data-stu-id="080af-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="080af-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Impressora \_ O atributo é \_ \_ concluído \_ primeiro** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="080af-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="080af-176">DoCompleteFirst</span><span class="sxs-lookup"><span data-stu-id="080af-176">DoCompleteFirst</span></span>

<span data-ttu-id="080af-177">Inicie os trabalhos que concluíram o spool primeiro.</span><span class="sxs-lookup"><span data-stu-id="080af-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="080af-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Impressora \_ ATRIBUTO \_ trabalhar \_ OFFLINE** (1024 (0x400))</span><span class="sxs-lookup"><span data-stu-id="080af-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="080af-179">WorkOffline</span><span class="sxs-lookup"><span data-stu-id="080af-179">WorkOffline</span></span>

<span data-ttu-id="080af-180">Enfileirar trabalhos de impressão quando uma impressora não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="080af-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="080af-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Impressora \_ ATRIBUTO \_ Enable \_ BIDI** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="080af-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="080af-182">EnableBIDI</span><span class="sxs-lookup"><span data-stu-id="080af-182">EnableBIDI</span></span>

<span data-ttu-id="080af-183">Habilitar impressão bidirecional.</span><span class="sxs-lookup"><span data-stu-id="080af-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="080af-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Impressora \_ \_ \_ Somente de atributo bruto** (4096 (0x1000))</span><span class="sxs-lookup"><span data-stu-id="080af-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="080af-185">Permitir que somente trabalhos de tipo de dados brutos sejam colocados em spool.</span><span class="sxs-lookup"><span data-stu-id="080af-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="080af-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Impressora \_ ATRIBUTO \_ publicado** (8192 (0x2000))</span><span class="sxs-lookup"><span data-stu-id="080af-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="080af-187">Publicado</span><span class="sxs-lookup"><span data-stu-id="080af-187">Published</span></span>

<span data-ttu-id="080af-188">Publicado no serviço de diretório de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-189">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="080af-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-190">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-192">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="080af-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="080af-193">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-193">Availability and status of the device.</span></span>

<span data-ttu-id="080af-194">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="080af-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="080af-198">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="080af-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="080af-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="080af-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="080af-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="080af-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="080af-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="080af-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="080af-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="080af-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="080af-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="080af-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="080af-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="080af-209">O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="080af-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="080af-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="080af-211">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="080af-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="080af-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="080af-213">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="080af-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="080af-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="080af-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="080af-216">O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="080af-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="080af-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="080af-218">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="080af-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="080af-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="080af-220">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="080af-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="080af-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="080af-222">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="080af-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="080af-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="080af-224">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="080af-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-225">**AvailableJobSheets**</span><span class="sxs-lookup"><span data-stu-id="080af-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-226">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-228">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredJobSheets")</span><span class="sxs-lookup"><span data-stu-id="080af-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="080af-229">Matriz de todas as folhas de trabalhos disponíveis em uma impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="080af-230">Também pode ser usado para descrever a faixa que uma impressora pode fornecer no início de cada trabalho ou outras opções especificadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="080af-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="080af-231">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-232">**AveragePagesPerMinute**</span><span class="sxs-lookup"><span data-stu-id="080af-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-233">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-235">Taxa de impressão, em número médio de páginas por minuto, que uma impressora pode produzir saída.</span><span class="sxs-lookup"><span data-stu-id="080af-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="080af-236">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="080af-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-237">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-239">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ impressora CIM**](cim-printer.md). CapabilityDescriptions "," CIM \_ PrintJob. concluindo "," CIM \_ PrintCapabilities. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="080af-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="080af-240">Matriz de recursos de impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-240">Array of printer capabilities.</span></span>

<span data-ttu-id="080af-241">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="080af-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="080af-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="080af-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="080af-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="080af-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="080af-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="080af-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="080af-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="080af-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="080af-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="080af-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="080af-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="080af-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="080af-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="080af-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="080af-257">Two-Sided borda longa</span><span class="sxs-lookup"><span data-stu-id="080af-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="080af-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="080af-259">Two-Sided borda curta</span><span class="sxs-lookup"><span data-stu-id="080af-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="080af-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="080af-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="080af-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="080af-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="080af-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="080af-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="080af-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-267">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="080af-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-268">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-270">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ impressora CIM**](cim-printer.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="080af-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-271">Matriz de cadeias de caracteres de forma livre que fornecem explicações detalhadas para os recursos de impressora indicados na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="080af-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="080af-272">Cada entrada dessa matriz está relacionada a uma entrada na matriz de **recursos** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="080af-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="080af-273">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-274">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="080af-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-275">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-276">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-277">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="080af-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="080af-278">Breve descrição de um objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="080af-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="080af-279">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="080af-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-280">**CharSetsSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-281">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-283">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationCharacterSet ")</span><span class="sxs-lookup"><span data-stu-id="080af-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="080af-284">Matriz de conjuntos de caracteres disponíveis para saída.</span><span class="sxs-lookup"><span data-stu-id="080af-284">Array of available character sets for output.</span></span> <span data-ttu-id="080af-285">As cadeias de caracteres fornecidas nesta propriedade devem estar em conformidade com a semântica e a sintaxe especificadas pela seção 4.1.2 ("parâmetros de charset") na RFC 2046 (MIME parte 2) e contidas no registro de conjunto de caracteres IANA.</span><span class="sxs-lookup"><span data-stu-id="080af-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="080af-286">Os exemplos incluem "UTF-8", "US-ASCII" e "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="080af-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="080af-287">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-288">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="080af-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-290">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-291">Comentário de uma fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="080af-291">Comment for a print queue.</span></span>

<span data-ttu-id="080af-292">Exemplo: impressora colorida</span><span class="sxs-lookup"><span data-stu-id="080af-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="080af-293">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="080af-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-294">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-296">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="080af-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="080af-297">Código de erro do Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="080af-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="080af-298">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="080af-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="080af-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="080af-300"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="080af-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="080af-301">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="080af-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="080af-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="080af-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="080af-303">(1)</span><span class="sxs-lookup"><span data-stu-id="080af-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="080af-304">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="080af-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="080af-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="080af-306">(2)</span><span class="sxs-lookup"><span data-stu-id="080af-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="080af-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="080af-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="080af-308">(3)</span><span class="sxs-lookup"><span data-stu-id="080af-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="080af-309">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="080af-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="080af-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="080af-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="080af-311">(4)</span><span class="sxs-lookup"><span data-stu-id="080af-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="080af-312">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="080af-312">Device is not working properly.</span></span> <span data-ttu-id="080af-313">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="080af-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="080af-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="080af-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="080af-315">(5)</span><span class="sxs-lookup"><span data-stu-id="080af-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="080af-316">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="080af-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="080af-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="080af-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="080af-318"> (6)</span><span class="sxs-lookup"><span data-stu-id="080af-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="080af-319">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="080af-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="080af-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="080af-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="080af-321">(7)</span><span class="sxs-lookup"><span data-stu-id="080af-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="080af-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="080af-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="080af-323">(8)</span><span class="sxs-lookup"><span data-stu-id="080af-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="080af-324">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="080af-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="080af-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="080af-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="080af-326">(9)</span><span class="sxs-lookup"><span data-stu-id="080af-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="080af-327">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="080af-327">Device is not working properly.</span></span> <span data-ttu-id="080af-328">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="080af-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="080af-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="080af-330">(10)</span><span class="sxs-lookup"><span data-stu-id="080af-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="080af-331">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="080af-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="080af-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="080af-333">(11)</span><span class="sxs-lookup"><span data-stu-id="080af-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="080af-334">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="080af-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="080af-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="080af-336">12</span><span class="sxs-lookup"><span data-stu-id="080af-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="080af-337">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="080af-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="080af-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="080af-339">(13)</span><span class="sxs-lookup"><span data-stu-id="080af-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="080af-340">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="080af-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="080af-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="080af-342">(14)</span><span class="sxs-lookup"><span data-stu-id="080af-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="080af-343">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="080af-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="080af-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="080af-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="080af-345">(15)</span><span class="sxs-lookup"><span data-stu-id="080af-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="080af-346">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="080af-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="080af-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="080af-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="080af-348">(16)</span><span class="sxs-lookup"><span data-stu-id="080af-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="080af-349">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="080af-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="080af-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="080af-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="080af-351">(17)</span><span class="sxs-lookup"><span data-stu-id="080af-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="080af-352">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="080af-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="080af-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="080af-354">(18)</span><span class="sxs-lookup"><span data-stu-id="080af-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="080af-355">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="080af-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="080af-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="080af-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="080af-357">(19)</span><span class="sxs-lookup"><span data-stu-id="080af-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="080af-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="080af-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="080af-359">(20)</span><span class="sxs-lookup"><span data-stu-id="080af-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="080af-360">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="080af-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="080af-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="080af-362">(21)</span><span class="sxs-lookup"><span data-stu-id="080af-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="080af-363">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="080af-363">System failure.</span></span> <span data-ttu-id="080af-364">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="080af-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="080af-365">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="080af-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="080af-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="080af-367">(22)</span><span class="sxs-lookup"><span data-stu-id="080af-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="080af-368">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="080af-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="080af-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="080af-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="080af-370">(23)</span><span class="sxs-lookup"><span data-stu-id="080af-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="080af-371">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="080af-371">System failure.</span></span> <span data-ttu-id="080af-372">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="080af-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="080af-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="080af-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="080af-374">(24)</span><span class="sxs-lookup"><span data-stu-id="080af-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="080af-375">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="080af-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="080af-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="080af-377">(25)</span><span class="sxs-lookup"><span data-stu-id="080af-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="080af-378">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="080af-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="080af-380">(26)</span><span class="sxs-lookup"><span data-stu-id="080af-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="080af-381">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="080af-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="080af-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="080af-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="080af-383">(27)</span><span class="sxs-lookup"><span data-stu-id="080af-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="080af-384">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="080af-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="080af-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="080af-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="080af-386">(28)</span><span class="sxs-lookup"><span data-stu-id="080af-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="080af-387">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="080af-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="080af-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="080af-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="080af-389">(29)</span><span class="sxs-lookup"><span data-stu-id="080af-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="080af-390">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="080af-390">Device is disabled.</span></span> <span data-ttu-id="080af-391">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="080af-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="080af-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="080af-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="080af-393">(30)</span><span class="sxs-lookup"><span data-stu-id="080af-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="080af-394">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="080af-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="080af-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="080af-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="080af-396">(31)</span><span class="sxs-lookup"><span data-stu-id="080af-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="080af-397">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="080af-397">Device is not working properly.</span></span> <span data-ttu-id="080af-398">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="080af-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-399">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="080af-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-400">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-402">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="080af-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="080af-403">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="080af-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="080af-404">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-405">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="080af-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-408">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="080af-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="080af-409">Nome da primeira classe concreta a ser exibida na cadeia de herança usada para criar uma instância.</span><span class="sxs-lookup"><span data-stu-id="080af-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="080af-410">Quando usado com outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="080af-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="080af-411">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-412">**CurrentCapabilities**</span><span class="sxs-lookup"><span data-stu-id="080af-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-413">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-415">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="080af-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-416">Matriz de recursos de impressora que estão sendo usados no momento.</span><span class="sxs-lookup"><span data-stu-id="080af-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="080af-417">Uma entrada nessa propriedade também deve ser listada na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="080af-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="080af-418">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="080af-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="080af-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="080af-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="080af-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="080af-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="080af-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="080af-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="080af-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="080af-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="080af-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="080af-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="080af-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="080af-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="080af-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="080af-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="080af-434">Two-Sided borda longa</span><span class="sxs-lookup"><span data-stu-id="080af-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="080af-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="080af-436">Two-Sided borda curta</span><span class="sxs-lookup"><span data-stu-id="080af-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="080af-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="080af-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="080af-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="080af-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="080af-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="080af-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="080af-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-444">**CurrentCharSet**</span><span class="sxs-lookup"><span data-stu-id="080af-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-447">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**CharSetsSupported**")</span><span class="sxs-lookup"><span data-stu-id="080af-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-448">O conjunto de caracteres usado atualmente para saída.</span><span class="sxs-lookup"><span data-stu-id="080af-448">The character set currently used for output.</span></span> <span data-ttu-id="080af-449">As cadeias de caracteres fornecidas nesta propriedade devem estar em conformidade com a semântica e a sintaxe especificadas pela seção 4.1.2 ("parâmetros de charset") na RFC 2046 (MIME parte 2) e contidas no registro de conjunto de caracteres IANA.</span><span class="sxs-lookup"><span data-stu-id="080af-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="080af-450">Os exemplos incluem "UTF-8", "US-ASCII" e ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="080af-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="080af-451">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-452">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="080af-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-453">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-454">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-455">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md). LanguagesSupported ","**\_ impressora CIM**.**CurrentMimeType**")</span><span class="sxs-lookup"><span data-stu-id="080af-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-456">Idioma da impressora usado no momento.</span><span class="sxs-lookup"><span data-stu-id="080af-456">Printer language currently used.</span></span> <span data-ttu-id="080af-457">O idioma usado deve estar listado na propriedade **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="080af-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="080af-458">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="080af-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="080af-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="080af-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="080af-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="080af-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="080af-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="080af-467"><span id="PPDS"></span><span id="ppds"></span>**PPDs** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="080af-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="080af-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="080af-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="080af-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interoperação** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="080af-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="080af-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dados da linha** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="080af-474">LineData</span><span class="sxs-lookup"><span data-stu-id="080af-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="080af-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="080af-476">DODCA</span><span class="sxs-lookup"><span data-stu-id="080af-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="080af-477"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="080af-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="080af-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="080af-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="080af-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="080af-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="080af-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="080af-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="080af-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="080af-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="080af-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="080af-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="080af-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="080af-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="080af-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="080af-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="080af-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="080af-488"><span id="QUIC"></span><span id="quic"></span>**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="080af-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="080af-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="080af-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="080af-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="080af-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="080af-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simples** (31)</span><span class="sxs-lookup"><span data-stu-id="080af-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="080af-492">SimpleText</span><span class="sxs-lookup"><span data-stu-id="080af-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="080af-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="080af-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="080af-494"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="080af-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="080af-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="080af-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="080af-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="080af-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="080af-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="080af-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="080af-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="080af-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="080af-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático** (38)</span><span class="sxs-lookup"><span data-stu-id="080af-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="080af-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="080af-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="080af-501"><span id="LIPS"></span><span id="lips"></span>**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="080af-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="080af-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="080af-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="080af-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="080af-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="080af-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="080af-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="080af-505"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="080af-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="080af-506"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="080af-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="080af-507"><span id="XES"></span><span id="xes"></span>**CES** (46)</span><span class="sxs-lookup"><span data-stu-id="080af-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="080af-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="080af-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="080af-509">48</span><span class="sxs-lookup"><span data-stu-id="080af-509">48</span></span>
</dt> <dd>

<span data-ttu-id="080af-510">XPS</span><span class="sxs-lookup"><span data-stu-id="080af-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="080af-511">49</span><span class="sxs-lookup"><span data-stu-id="080af-511">49</span></span>
</dt> <dd>

<span data-ttu-id="080af-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="080af-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="080af-513">50</span><span class="sxs-lookup"><span data-stu-id="080af-513">50</span></span>
</dt> <dd>

<span data-ttu-id="080af-514">PCLXL</span><span class="sxs-lookup"><span data-stu-id="080af-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-515">**CurrentMimeType**</span><span class="sxs-lookup"><span data-stu-id="080af-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-516">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-517">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-518">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**CurrentLanguage**")</span><span class="sxs-lookup"><span data-stu-id="080af-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-519">Tipo MIME que está sendo usado no momento se **CurrentLanguage** for um tipo MIME (valor = 47).</span><span class="sxs-lookup"><span data-stu-id="080af-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="080af-520">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-521">**CurrentNaturalLanguage**</span><span class="sxs-lookup"><span data-stu-id="080af-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-522">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-523">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-524">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**NaturalLanguagesSupported**")</span><span class="sxs-lookup"><span data-stu-id="080af-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-525">Idioma que a impressora está usando para o gerenciamento no momento.</span><span class="sxs-lookup"><span data-stu-id="080af-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="080af-526">A linguagem listada aqui também deve ser listada na propriedade **NaturalLanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="080af-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="080af-527">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-528">**CurrentPaperType**</span><span class="sxs-lookup"><span data-stu-id="080af-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-529">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-530">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-531">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="080af-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-532">Tipo de papel que a impressora está usando.</span><span class="sxs-lookup"><span data-stu-id="080af-532">Type of paper the printer is using.</span></span> <span data-ttu-id="080af-533">Deve ser expresso no formato especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que é resumido no Apêndice C do RFC 1759 (MIB de impressora).</span><span class="sxs-lookup"><span data-stu-id="080af-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="080af-534">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-535">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="080af-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-536">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-537">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-538">Se for **true**, a impressora será a impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="080af-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="080af-539">**Funções de recursos**</span><span class="sxs-lookup"><span data-stu-id="080af-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-540">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-541">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-542">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="080af-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-543">Matriz dos recursos de impressora usados por padrão.</span><span class="sxs-lookup"><span data-stu-id="080af-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="080af-544">Cada entrada na matriz **defaultcapabilities** também deve ser listada na matriz **Capabilities** .</span><span class="sxs-lookup"><span data-stu-id="080af-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="080af-545">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="080af-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="080af-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="080af-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="080af-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="080af-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="080af-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="080af-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="080af-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="080af-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="080af-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="080af-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="080af-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="080af-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="080af-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="080af-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="080af-561">Two-Sided borda longa</span><span class="sxs-lookup"><span data-stu-id="080af-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="080af-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="080af-563">Two-Sided borda curta</span><span class="sxs-lookup"><span data-stu-id="080af-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="080af-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="080af-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="080af-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="080af-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="080af-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="080af-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="080af-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-571">**Defaultcopies**</span><span class="sxs-lookup"><span data-stu-id="080af-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-572">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-573">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-574">Número de cópias produzidas para um trabalho — a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="080af-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="080af-575">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="080af-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-577">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-578">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-579">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md). LanguagesSupported ","**\_ impressora CIM**.**Defaultmimetype**")</span><span class="sxs-lookup"><span data-stu-id="080af-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-580">Idioma padrão da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-580">Default printer language.</span></span> <span data-ttu-id="080af-581">A linguagem listada aqui também deve ser listada na propriedade **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="080af-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="080af-582">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="080af-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="080af-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="080af-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="080af-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="080af-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="080af-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="080af-591"><span id="PPDS"></span><span id="ppds"></span>**PPDs** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="080af-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="080af-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="080af-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="080af-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interoperação** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="080af-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="080af-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dados da linha** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="080af-598">LineData</span><span class="sxs-lookup"><span data-stu-id="080af-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="080af-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="080af-600">DODCA</span><span class="sxs-lookup"><span data-stu-id="080af-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="080af-601"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="080af-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="080af-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="080af-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="080af-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="080af-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="080af-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="080af-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="080af-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="080af-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="080af-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="080af-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="080af-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="080af-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="080af-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="080af-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="080af-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="080af-612"><span id="QUIC"></span><span id="quic"></span>**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="080af-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="080af-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="080af-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="080af-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="080af-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="080af-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simples** (31)</span><span class="sxs-lookup"><span data-stu-id="080af-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="080af-616">SimpleText</span><span class="sxs-lookup"><span data-stu-id="080af-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="080af-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="080af-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="080af-618"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="080af-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="080af-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="080af-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="080af-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="080af-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="080af-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="080af-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="080af-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="080af-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="080af-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático** (38)</span><span class="sxs-lookup"><span data-stu-id="080af-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="080af-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="080af-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="080af-625"><span id="LIPS"></span><span id="lips"></span>**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="080af-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="080af-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="080af-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="080af-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="080af-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="080af-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="080af-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="080af-629"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="080af-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="080af-630"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="080af-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="080af-631"><span id="XES"></span><span id="xes"></span>**CES** (46)</span><span class="sxs-lookup"><span data-stu-id="080af-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="080af-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="080af-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="080af-633">48</span><span class="sxs-lookup"><span data-stu-id="080af-633">48</span></span>
</dt> <dd>

<span data-ttu-id="080af-634">XPS</span><span class="sxs-lookup"><span data-stu-id="080af-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="080af-635">49</span><span class="sxs-lookup"><span data-stu-id="080af-635">49</span></span>
</dt> <dd>

<span data-ttu-id="080af-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="080af-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="080af-637">50</span><span class="sxs-lookup"><span data-stu-id="080af-637">50</span></span>
</dt> <dd>

<span data-ttu-id="080af-638">PCLXL</span><span class="sxs-lookup"><span data-stu-id="080af-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-639">**Defaultmimetype**</span><span class="sxs-lookup"><span data-stu-id="080af-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-640">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-641">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-642">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="080af-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-643">Tipo MIME que está sendo usado no momento, se o valor de **DefaultLanguage** for um tipo MIME (valor = 47).</span><span class="sxs-lookup"><span data-stu-id="080af-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="080af-644">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-645">**DefaultNumberUp**</span><span class="sxs-lookup"><span data-stu-id="080af-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-646">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-647">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-648">Número de páginas de fluxo de impressão que a impressora renderiza em uma folha de mídia — a menos que um trabalho especifique o contrário.</span><span class="sxs-lookup"><span data-stu-id="080af-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="080af-649">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-650">**Defaultpapertype**</span><span class="sxs-lookup"><span data-stu-id="080af-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-651">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-652">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-653">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**PaperTypesAvailable**")</span><span class="sxs-lookup"><span data-stu-id="080af-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-654">Tipo de papel usado pela impressora — a menos que um trabalho de impressão especifique um tipo de papel diferente.</span><span class="sxs-lookup"><span data-stu-id="080af-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="080af-655">A cadeia de caracteres deve ser expressa no formulário especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 1017, que é resumido no Apêndice C do [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (MIB de impressora).</span><span class="sxs-lookup"><span data-stu-id="080af-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="080af-656">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-657">**Defaultanteriority**</span><span class="sxs-lookup"><span data-stu-id="080af-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-658">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-659">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-660">Valor de prioridade padrão atribuído a cada trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="080af-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="080af-661">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="080af-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-662">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-663">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-664">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="080af-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="080af-665">Descrição de um objeto.</span><span class="sxs-lookup"><span data-stu-id="080af-665">Description of an object.</span></span>

<span data-ttu-id="080af-666">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="080af-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-667">**DetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="080af-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-668">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-669">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-670">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")</span><span class="sxs-lookup"><span data-stu-id="080af-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="080af-671">Informações de erro da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-671">Printer error information.</span></span>

<span data-ttu-id="080af-672">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-673">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="080af-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-674">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="080af-675">**Sem erro** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="080af-676">**Papel baixo** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="080af-677">**Sem papel** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="080af-678">**Toner baixo** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="080af-679">**Sem toner** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="080af-680">**Porta aberta** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="080af-681">**Emperrado** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="080af-682">**Offline** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="080af-683">**Serviço solicitado** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="080af-684">**Escaninho de saída cheio** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-685">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="080af-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-686">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-687">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-688">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="080af-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="080af-689">Identificador exclusivo da impressora em um sistema.</span><span class="sxs-lookup"><span data-stu-id="080af-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="080af-690">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-691">**Direto**</span><span class="sxs-lookup"><span data-stu-id="080af-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-692">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-693">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-694">Se **for true**, o trabalho de impressão será enviado diretamente para a impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="080af-695">Se for **false**, o trabalho de impressão será colocado no spool.</span><span class="sxs-lookup"><span data-stu-id="080af-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="080af-696">**DoCompleteFirst**</span><span class="sxs-lookup"><span data-stu-id="080af-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-697">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-698">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-699">Se **for true**, a impressora iniciará trabalhos que concluíram o spool.</span><span class="sxs-lookup"><span data-stu-id="080af-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="080af-700">Se **for false**, a impressora iniciará trabalhos na ordem em que os trabalhos são recebidos.</span><span class="sxs-lookup"><span data-stu-id="080af-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="080af-701">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="080af-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-702">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-703">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-704">Nome do driver de impressora do Windows.</span><span class="sxs-lookup"><span data-stu-id="080af-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="080af-705">Exemplo: driver de fax do Windows</span><span class="sxs-lookup"><span data-stu-id="080af-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="080af-706">**EnableBIDI**</span><span class="sxs-lookup"><span data-stu-id="080af-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-707">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-708">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-709">Se **for true**, a impressora poderá imprimir bidirecionalmente.</span><span class="sxs-lookup"><span data-stu-id="080af-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="080af-710">**EnableDevQueryPrint**</span><span class="sxs-lookup"><span data-stu-id="080af-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-711">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-712">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-713">Se **for true**, a impressora manterá os documentos na fila quando as configurações de documento e impressora não corresponderem.</span><span class="sxs-lookup"><span data-stu-id="080af-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="080af-714">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="080af-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-715">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-716">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-717">Se **for true**, o erro relatado em **LastErrorCode** foi limpo.</span><span class="sxs-lookup"><span data-stu-id="080af-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="080af-718">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="080af-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-720">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-721">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-722">Informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="080af-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="080af-723">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-724">**ErrorInformation**</span><span class="sxs-lookup"><span data-stu-id="080af-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-725">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-726">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="080af-727">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md).**DetectedErrorState**")</span><span class="sxs-lookup"><span data-stu-id="080af-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="080af-728">Matriz de informações complementares para o estado de erro atual indicado em **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="080af-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="080af-729">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-730">**ExtendedDetectedErrorState**</span><span class="sxs-lookup"><span data-stu-id="080af-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-731">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-732">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-733">Relata informações de erro padrão.</span><span class="sxs-lookup"><span data-stu-id="080af-733">Reports standard error information.</span></span> <span data-ttu-id="080af-734">Informações adicionais devem ser registradas em **DetectedErrorState**.</span><span class="sxs-lookup"><span data-stu-id="080af-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="080af-735">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="080af-735">Values are:</span></span>

<dt>

<span data-ttu-id="080af-736">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="080af-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="080af-737">Unknown</span><span class="sxs-lookup"><span data-stu-id="080af-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="080af-738">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="080af-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="080af-739">Outro</span><span class="sxs-lookup"><span data-stu-id="080af-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="080af-740">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="080af-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="080af-741">Sem erros</span><span class="sxs-lookup"><span data-stu-id="080af-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="080af-742">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="080af-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="080af-743">Pouco Papel</span><span class="sxs-lookup"><span data-stu-id="080af-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="080af-744">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="080af-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="080af-745">Sem Papel</span><span class="sxs-lookup"><span data-stu-id="080af-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="080af-746">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="080af-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="080af-747">Toner Baixo</span><span class="sxs-lookup"><span data-stu-id="080af-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="080af-748">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="080af-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="080af-749">Sem Toner</span><span class="sxs-lookup"><span data-stu-id="080af-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="080af-750">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="080af-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="080af-751">Porta Aberta</span><span class="sxs-lookup"><span data-stu-id="080af-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="080af-752">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="080af-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="080af-753">Obstruído</span><span class="sxs-lookup"><span data-stu-id="080af-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="080af-754">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="080af-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="080af-755">Serviço Solicitado</span><span class="sxs-lookup"><span data-stu-id="080af-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="080af-756">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="080af-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="080af-757">Bandeja de Saída Cheia</span><span class="sxs-lookup"><span data-stu-id="080af-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="080af-758">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="080af-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="080af-759">Problema de papel</span><span class="sxs-lookup"><span data-stu-id="080af-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="080af-760">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="080af-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="080af-761">Não é possível imprimir a página</span><span class="sxs-lookup"><span data-stu-id="080af-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="080af-762">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="080af-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="080af-763">Intervenção do usuário necessária</span><span class="sxs-lookup"><span data-stu-id="080af-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="080af-764">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="080af-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="080af-765">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="080af-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="080af-766">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="080af-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="080af-767">Servidor desconhecido</span><span class="sxs-lookup"><span data-stu-id="080af-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-768">**ExtendedPrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="080af-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-769">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-770">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-771">Informações de status para uma impressora que é diferente das informações especificadas na propriedade de **disponibilidade** .</span><span class="sxs-lookup"><span data-stu-id="080af-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="080af-772">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="080af-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="080af-773">Outro</span><span class="sxs-lookup"><span data-stu-id="080af-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="080af-774">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="080af-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="080af-775">Unknown</span><span class="sxs-lookup"><span data-stu-id="080af-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="080af-776">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="080af-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="080af-777">Ocioso</span><span class="sxs-lookup"><span data-stu-id="080af-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="080af-778">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="080af-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="080af-779">Imprimindo</span><span class="sxs-lookup"><span data-stu-id="080af-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="080af-780">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="080af-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="080af-781">Aquecendo</span><span class="sxs-lookup"><span data-stu-id="080af-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="080af-782">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="080af-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="080af-783">Impressão parada</span><span class="sxs-lookup"><span data-stu-id="080af-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="080af-784">7</span><span class="sxs-lookup"><span data-stu-id="080af-784">7</span></span>
</dt> <dd>

<span data-ttu-id="080af-785">Offline</span><span class="sxs-lookup"><span data-stu-id="080af-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="080af-786">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="080af-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="080af-787">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="080af-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="080af-788">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="080af-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="080af-789">Erro</span><span class="sxs-lookup"><span data-stu-id="080af-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="080af-790">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="080af-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="080af-791">Ocupado</span><span class="sxs-lookup"><span data-stu-id="080af-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="080af-792">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="080af-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="080af-793">Não disponível</span><span class="sxs-lookup"><span data-stu-id="080af-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="080af-794">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="080af-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="080af-795">Aguardando</span><span class="sxs-lookup"><span data-stu-id="080af-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="080af-796">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="080af-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="080af-797">Processing</span><span class="sxs-lookup"><span data-stu-id="080af-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="080af-798">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="080af-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="080af-799">Inicialização</span><span class="sxs-lookup"><span data-stu-id="080af-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="080af-800">15</span><span class="sxs-lookup"><span data-stu-id="080af-800">15</span></span>
</dt> <dd>

<span data-ttu-id="080af-801">Economia de energia</span><span class="sxs-lookup"><span data-stu-id="080af-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="080af-802">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="080af-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="080af-803">Exclusão pendente</span><span class="sxs-lookup"><span data-stu-id="080af-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="080af-804">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="080af-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="080af-805">E/s ativa</span><span class="sxs-lookup"><span data-stu-id="080af-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="080af-806">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="080af-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="080af-807">Feed manual</span><span class="sxs-lookup"><span data-stu-id="080af-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-808">**Oculto**</span><span class="sxs-lookup"><span data-stu-id="080af-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-809">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-810">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-811">Se for **true**, a impressora ficará oculta dos usuários da rede.</span><span class="sxs-lookup"><span data-stu-id="080af-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="080af-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="080af-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-813">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-814">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-815">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](../wmisdk/standard-qualifiers.md) ("pixels por polegada")</span><span class="sxs-lookup"><span data-stu-id="080af-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="080af-816">Resolução horizontal da impressora — em pixels por polegada.</span><span class="sxs-lookup"><span data-stu-id="080af-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="080af-817">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="080af-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-819">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080af-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080af-820">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-821">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="080af-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="080af-822">Data e hora em que um objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="080af-822">Date and time an object was installed.</span></span> <span data-ttu-id="080af-823">O objeto pode ser instalado sem que um valor seja gravado nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="080af-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="080af-824">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="080af-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-825">**JobCountSinceLastReset**</span><span class="sxs-lookup"><span data-stu-id="080af-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-826">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-827">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-828">Qualificadores: **contador**</span><span class="sxs-lookup"><span data-stu-id="080af-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="080af-829">Número de trabalhos de impressão desde a última redefinição da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="080af-830">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-831">**KeepPrintedJobs**</span><span class="sxs-lookup"><span data-stu-id="080af-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-832">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-833">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-834">Se **for true**, o spooler de impressão não excluirá os trabalhos concluídos.</span><span class="sxs-lookup"><span data-stu-id="080af-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="080af-835">**LanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-836">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-837">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-838">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md). MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ reservice. LanguagesSupported ")</span><span class="sxs-lookup"><span data-stu-id="080af-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="080af-839">Matriz de idiomas de impressão com suporte nativo.</span><span class="sxs-lookup"><span data-stu-id="080af-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="080af-840">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="080af-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="080af-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="080af-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="080af-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="080af-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="080af-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="080af-849"><span id="PPDS"></span><span id="ppds"></span>**PPDs** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="080af-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="080af-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="080af-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="080af-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interoperação** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="080af-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="080af-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Dados da linha** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="080af-856">LineData</span><span class="sxs-lookup"><span data-stu-id="080af-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="080af-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="080af-858">DODCA</span><span class="sxs-lookup"><span data-stu-id="080af-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="080af-859"><span id="REGIS"></span><span id="regis"></span>**Regis** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="080af-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="080af-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="080af-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="080af-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="080af-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span><span class="sxs-lookup"><span data-stu-id="080af-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="080af-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span><span class="sxs-lookup"><span data-stu-id="080af-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="080af-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span><span class="sxs-lookup"><span data-stu-id="080af-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="080af-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="080af-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="080af-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="080af-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="080af-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="080af-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="080af-870"><span id="QUIC"></span><span id="quic"></span>**Quic** (28)</span><span class="sxs-lookup"><span data-stu-id="080af-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="080af-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span><span class="sxs-lookup"><span data-stu-id="080af-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="080af-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span><span class="sxs-lookup"><span data-stu-id="080af-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="080af-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Texto simples** (31)</span><span class="sxs-lookup"><span data-stu-id="080af-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="080af-874">SimpleText</span><span class="sxs-lookup"><span data-stu-id="080af-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="080af-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span><span class="sxs-lookup"><span data-stu-id="080af-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="080af-876"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="080af-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="080af-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="080af-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="080af-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span><span class="sxs-lookup"><span data-stu-id="080af-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="080af-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span><span class="sxs-lookup"><span data-stu-id="080af-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="080af-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="080af-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="080af-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automático** (38)</span><span class="sxs-lookup"><span data-stu-id="080af-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="080af-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Páginas** (39)</span><span class="sxs-lookup"><span data-stu-id="080af-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="080af-883"><span id="LIPS"></span><span id="lips"></span>**Lips** (40)</span><span class="sxs-lookup"><span data-stu-id="080af-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="080af-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="080af-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="080af-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (42)</span><span class="sxs-lookup"><span data-stu-id="080af-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="080af-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span><span class="sxs-lookup"><span data-stu-id="080af-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="080af-887"><span id="EXCL"></span><span id="excl"></span>**Excl** (44)</span><span class="sxs-lookup"><span data-stu-id="080af-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="080af-888"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="080af-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="080af-889"><span id="XES"></span><span id="xes"></span>**CES** (46)</span><span class="sxs-lookup"><span data-stu-id="080af-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="080af-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="080af-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="080af-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="080af-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="080af-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="080af-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="080af-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span><span class="sxs-lookup"><span data-stu-id="080af-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-894">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="080af-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-895">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-896">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-897">Último código de erro que o dispositivo lógico relata.</span><span class="sxs-lookup"><span data-stu-id="080af-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="080af-898">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-899">**Local**</span><span class="sxs-lookup"><span data-stu-id="080af-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-900">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-901">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-902">Se **for true**, a impressora não será conectada a uma rede.</span><span class="sxs-lookup"><span data-stu-id="080af-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="080af-903">Se as propriedades **local** e de **rede** estiverem definidas como **true**, a impressora será uma impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="080af-904">**Localidade**</span><span class="sxs-lookup"><span data-stu-id="080af-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-905">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-906">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-907">Local físico da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-907">Physical location of the printer.</span></span>

<span data-ttu-id="080af-908">Exemplo: Bldg.</span><span class="sxs-lookup"><span data-stu-id="080af-908">Example: Bldg.</span></span> <span data-ttu-id="080af-909">38, sala 1164</span><span class="sxs-lookup"><span data-stu-id="080af-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="080af-910">**MarkingTechnology**</span><span class="sxs-lookup"><span data-stu-id="080af-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-911">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-912">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-913">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")</span><span class="sxs-lookup"><span data-stu-id="080af-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="080af-914">Marcando a tecnologia que a impressora usa.</span><span class="sxs-lookup"><span data-stu-id="080af-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="080af-915">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-916">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-917">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="080af-918">**LED de Electrophotographic** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="080af-919">**Electrophotographic laser** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="080af-920">**Electrophotographic outro** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="080af-921">**Impacto ao mover matriz de ponto de cabeçalho 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="080af-922">**Impacto ao mover matriz de ponto de cabeçalho 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="080af-923">**Impacto ao mover matriz de ponto de cabeçalho outro** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="080af-924">**Cabeçalho de movimentação de impacto totalmente formado** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="080af-925">**Faixa de impacto** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="080af-926">**Outro impacto** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="080af-927">**Jato de aqueous** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="080af-928">**Jato de radiosolid** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="080af-929">**Outro jato** de Radio(14)</span><span class="sxs-lookup"><span data-stu-id="080af-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="080af-930">**Caneta** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="080af-931">**Transferência térmica** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="080af-932">**Sensível à térmica** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="080af-933">**Difusão térmica** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="080af-934">**Outros térmicas** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="080af-935">**Electroerosion** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="080af-936">**Eletrostática** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="080af-937">**Microfilme fotográfico** (22)</span><span class="sxs-lookup"><span data-stu-id="080af-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="080af-938">**Fotocompositora fotográfica** (23)</span><span class="sxs-lookup"><span data-stu-id="080af-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="080af-939">**Outro fotográfico** (24)</span><span class="sxs-lookup"><span data-stu-id="080af-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="080af-940">**Desposição de íon** (25)</span><span class="sxs-lookup"><span data-stu-id="080af-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="080af-941">**eBeam** (26)</span><span class="sxs-lookup"><span data-stu-id="080af-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="080af-942">**Typesetter** (27)</span><span class="sxs-lookup"><span data-stu-id="080af-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-943">**MaxCopies**</span><span class="sxs-lookup"><span data-stu-id="080af-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-944">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-945">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-946">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Copies")</span><span class="sxs-lookup"><span data-stu-id="080af-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="080af-947">Número máximo de cópias que a impressora pode produzir para um trabalho.</span><span class="sxs-lookup"><span data-stu-id="080af-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="080af-948">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-949">**MaxNumberUp**</span><span class="sxs-lookup"><span data-stu-id="080af-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-950">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-951">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-952">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. NumberUp")</span><span class="sxs-lookup"><span data-stu-id="080af-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="080af-953">Número máximo de páginas de fluxo de impressão que a impressora pode processar em uma folha de mídia, como papel.</span><span class="sxs-lookup"><span data-stu-id="080af-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="080af-954">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-955">**MaxSizeSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-956">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-957">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-958">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. Jobs"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span><span class="sxs-lookup"><span data-stu-id="080af-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="080af-959">O maior trabalho como um fluxo de bytes, em quilobytes, que a impressora pode aceitar.</span><span class="sxs-lookup"><span data-stu-id="080af-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="080af-960">Um valor de 0 (zero) indica que nenhum limite está definido.</span><span class="sxs-lookup"><span data-stu-id="080af-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="080af-961">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-962">**MimeTypesSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-963">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-964">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-965">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ impressora CIM**](cim-printer.md). LanguagesSupported "," CIM \_ PrintJob. mimeTypes "," CIM \_ Autoservice. MimeTypesSupported ")</span><span class="sxs-lookup"><span data-stu-id="080af-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="080af-966">Matriz de explicações de tipo MIME detalhadas às quais a impressora dá suporte.</span><span class="sxs-lookup"><span data-stu-id="080af-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="080af-967">Se os dados forem fornecidos, o valor 47 ("MIME") deverá ser incluído na propriedade **LanguagesSupported** .</span><span class="sxs-lookup"><span data-stu-id="080af-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="080af-968">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-969">**Nome**</span><span class="sxs-lookup"><span data-stu-id="080af-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-970">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-971">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-972">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="080af-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="080af-973">Nome da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-973">Name of the printer.</span></span>

<span data-ttu-id="080af-974">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="080af-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-975">**NaturalLanguagesSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-976">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-977">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-978">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtLocalizationLanguage "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. NaturalLanguage ")</span><span class="sxs-lookup"><span data-stu-id="080af-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="080af-979">Matriz de idiomas com suporte para cadeias de caracteres que a impressora usa para a saída de informações de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="080af-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="080af-980">Deve estar em conformidade com a [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span><span class="sxs-lookup"><span data-stu-id="080af-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="080af-981">Por exemplo, "en" é usado para inglês.</span><span class="sxs-lookup"><span data-stu-id="080af-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="080af-982">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-983">**Rede**</span><span class="sxs-lookup"><span data-stu-id="080af-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-984">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-985">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-986">Se for **true**, a impressora será uma impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="080af-987">Se as propriedades **local** e de **rede** estiverem definidas como **true**, a impressora será uma impressora de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="080af-988">**PaperSizesSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-989">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-990">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-991">Matriz dos tipos de papel aos quais a impressora dá suporte.</span><span class="sxs-lookup"><span data-stu-id="080af-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="080af-992">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="080af-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="080af-995"><span id="A"></span><span id="a"></span>**A** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="080af-996"><span id="B"></span><span id="b"></span>**B** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="080af-997"><span id="C"></span><span id="c"></span>**C** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="080af-998"><span id="D"></span><span id="d"></span>**D** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="080af-999"><span id="E"></span><span id="e"></span>**E** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="080af-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letra** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="080af-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Ofício** (8)</span><span class="sxs-lookup"><span data-stu-id="080af-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="080af-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-envelope** (9)</span><span class="sxs-lookup"><span data-stu-id="080af-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="080af-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Na-9x12-envelope** (10)</span><span class="sxs-lookup"><span data-stu-id="080af-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="080af-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-número-10-envelope** (11)</span><span class="sxs-lookup"><span data-stu-id="080af-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="080af-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Na-7x9-envelope** (12)</span><span class="sxs-lookup"><span data-stu-id="080af-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="080af-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Na-9x11-envelope** (13)</span><span class="sxs-lookup"><span data-stu-id="080af-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="080af-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Na-10x14-envelope** (14)</span><span class="sxs-lookup"><span data-stu-id="080af-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="080af-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-número-9-envelope** (15)</span><span class="sxs-lookup"><span data-stu-id="080af-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="080af-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-envelope** (16)</span><span class="sxs-lookup"><span data-stu-id="080af-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="080af-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Na-10x15-envelope** (17)</span><span class="sxs-lookup"><span data-stu-id="080af-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="080af-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="080af-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="080af-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="080af-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="080af-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="080af-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="080af-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="080af-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="080af-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="080af-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="080af-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="080af-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="080af-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="080af-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="080af-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="080af-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="080af-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="080af-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="080af-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="080af-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="080af-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="080af-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="080af-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="080af-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="080af-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="080af-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="080af-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="080af-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="080af-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="080af-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="080af-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="080af-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="080af-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="080af-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="080af-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="080af-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="080af-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="080af-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="080af-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="080af-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="080af-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="080af-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="080af-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="080af-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="080af-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="080af-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="080af-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="080af-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1035">C2</span><span class="sxs-lookup"><span data-stu-id="080af-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="080af-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="080af-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1037">C3</span><span class="sxs-lookup"><span data-stu-id="080af-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="080af-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="080af-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1039">C4</span><span class="sxs-lookup"><span data-stu-id="080af-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="080af-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="080af-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1041">C5</span><span class="sxs-lookup"><span data-stu-id="080af-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="080af-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="080af-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1043">C6</span><span class="sxs-lookup"><span data-stu-id="080af-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="080af-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="080af-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1045">C7</span><span class="sxs-lookup"><span data-stu-id="080af-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="080af-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Designado por ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="080af-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1047">C8</span><span class="sxs-lookup"><span data-stu-id="080af-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="080af-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="080af-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="080af-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="080af-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="080af-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="080af-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="080af-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="080af-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="080af-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="080af-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="080af-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="080af-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="080af-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="080af-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="080af-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="080af-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="080af-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="080af-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="080af-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="080af-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="080af-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="080af-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="080af-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="080af-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="080af-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="080af-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="080af-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="080af-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="080af-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1067">B8 JIS</span><span class="sxs-lookup"><span data-stu-id="080af-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="080af-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="080af-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1069">B9 JIS</span><span class="sxs-lookup"><span data-stu-id="080af-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="080af-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Na-letra** (59)</span><span class="sxs-lookup"><span data-stu-id="080af-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1071">JIS B10</span><span class="sxs-lookup"><span data-stu-id="080af-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="080af-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-ofício** (60)</span><span class="sxs-lookup"><span data-stu-id="080af-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="080af-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-envelope** (61)</span><span class="sxs-lookup"><span data-stu-id="080af-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="080af-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-envelope** (62)</span><span class="sxs-lookup"><span data-stu-id="080af-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="080af-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-envelope** (63)</span><span class="sxs-lookup"><span data-stu-id="080af-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="080af-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-envelope** (64)</span><span class="sxs-lookup"><span data-stu-id="080af-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="080af-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-envelope** (65)</span><span class="sxs-lookup"><span data-stu-id="080af-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="080af-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-envelope** (66)</span><span class="sxs-lookup"><span data-stu-id="080af-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="080af-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designado – envelope longo** (67)</span><span class="sxs-lookup"><span data-stu-id="080af-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="080af-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-envelope** (68)</span><span class="sxs-lookup"><span data-stu-id="080af-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="080af-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executivo** (69)</span><span class="sxs-lookup"><span data-stu-id="080af-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="080af-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Fólio** (70)</span><span class="sxs-lookup"><span data-stu-id="080af-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="080af-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Fatura** (71)</span><span class="sxs-lookup"><span data-stu-id="080af-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="080af-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Razão** (72)</span><span class="sxs-lookup"><span data-stu-id="080af-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="080af-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span><span class="sxs-lookup"><span data-stu-id="080af-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-1086">**PaperTypesAvailable**</span><span class="sxs-lookup"><span data-stu-id="080af-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1087">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-1088">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1089">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. RequiredPaperType", "CIM \_ reservice. PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. prtInputMediaName ")</span><span class="sxs-lookup"><span data-stu-id="080af-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="080af-1090">Matriz de tipos de papel que estão disponíveis atualmente na impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="080af-1091">Cada cadeia de caracteres deve ser expressa no formato especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que é resumido no Apêndice C do [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (MIB de impressora).</span><span class="sxs-lookup"><span data-stu-id="080af-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="080af-1092">Qualquer tamanho de papel identificado nessa propriedade também deve aparecer na propriedade **PaperSizesSupported** .</span><span class="sxs-lookup"><span data-stu-id="080af-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="080af-1093">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="080af-1094">Exemplo: ISO-A4-colorido</span><span class="sxs-lookup"><span data-stu-id="080af-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="080af-1095">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="080af-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1096">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1097">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1098">Parâmetros opcionais para o processador de impressão.</span><span class="sxs-lookup"><span data-stu-id="080af-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="080af-1099">Exemplo: "cópias = 2"</span><span class="sxs-lookup"><span data-stu-id="080af-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="080af-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="080af-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1101">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1102">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1103">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="080af-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="080af-1104">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="080af-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="080af-1105">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="080af-1106">Exemplo: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="080af-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="080af-1107">**Portaname**</span><span class="sxs-lookup"><span data-stu-id="080af-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1108">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1109">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1110">Porta usada para transmitir dados para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="080af-1111">Se uma impressora estiver conectada a mais de uma porta, os nomes de cada porta serão separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="080af-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="080af-1112">Exemplo: LPT1:, LPT2:, LPT3:</span><span class="sxs-lookup"><span data-stu-id="080af-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="080af-1113">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="080af-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1114">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-1115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-1116">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="080af-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="080af-1117">Essa propriedade é herdada **de \_ LogicalDevice CIM**.</span><span class="sxs-lookup"><span data-stu-id="080af-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="080af-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="080af-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="080af-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="080af-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1122">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="080af-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="080af-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1124">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="080af-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="080af-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1126">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="080af-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="080af-1127">Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="080af-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="080af-1128">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="080af-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1130">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="080af-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="080af-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1132">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="080af-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="080af-1133">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="080af-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-1134">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="080af-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1135">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-1137">Se **for true**, o poder do dispositivo poderá ser gerenciado, o que significa que ele pode ser colocado no modo de suspensão.</span><span class="sxs-lookup"><span data-stu-id="080af-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="080af-1138">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="080af-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="080af-1139">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1140">**PrinterPaperNames**</span><span class="sxs-lookup"><span data-stu-id="080af-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1141">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="080af-1142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-1143">Matriz de tamanhos de papel com suporte da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="080af-1144">Os nomes especificados pela impressora são usados para representar tamanhos de papel com suporte.</span><span class="sxs-lookup"><span data-stu-id="080af-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="080af-1145">Exemplo: B5 (JIS)</span><span class="sxs-lookup"><span data-stu-id="080af-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="080af-1146">**Impressora.**</span><span class="sxs-lookup"><span data-stu-id="080af-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1147">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1149">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="080af-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="080af-1150">Um dos possíveis estados relacionados a essa impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="080af-1151">Esta propriedade está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="080af-1151">This property is obsolete.</span></span> <span data-ttu-id="080af-1152">No lugar dessa propriedade, use **PrinterStatus**.</span><span class="sxs-lookup"><span data-stu-id="080af-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="080af-1153">0</span><span class="sxs-lookup"><span data-stu-id="080af-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="080af-1154">Ocioso-para obter mais informações, consulte a seção comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="080af-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1155">1</span><span class="sxs-lookup"><span data-stu-id="080af-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="080af-1156">Em Pausa</span><span class="sxs-lookup"><span data-stu-id="080af-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="080af-1157">2</span><span class="sxs-lookup"><span data-stu-id="080af-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="080af-1158">Erro</span><span class="sxs-lookup"><span data-stu-id="080af-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="080af-1159">3</span><span class="sxs-lookup"><span data-stu-id="080af-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="080af-1160">Exclusão pendente</span><span class="sxs-lookup"><span data-stu-id="080af-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="080af-1161">4</span><span class="sxs-lookup"><span data-stu-id="080af-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="080af-1162">Obstrução de papel</span><span class="sxs-lookup"><span data-stu-id="080af-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="080af-1163">5</span><span class="sxs-lookup"><span data-stu-id="080af-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="080af-1164">Saída de papel</span><span class="sxs-lookup"><span data-stu-id="080af-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="080af-1165">6</span><span class="sxs-lookup"><span data-stu-id="080af-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="080af-1166">Feed manual</span><span class="sxs-lookup"><span data-stu-id="080af-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="080af-1167">7</span><span class="sxs-lookup"><span data-stu-id="080af-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="080af-1168">Problema de papel</span><span class="sxs-lookup"><span data-stu-id="080af-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="080af-1169">8</span><span class="sxs-lookup"><span data-stu-id="080af-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="080af-1170">Offline</span><span class="sxs-lookup"><span data-stu-id="080af-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="080af-1171">9</span><span class="sxs-lookup"><span data-stu-id="080af-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="080af-1172">E/s ativa</span><span class="sxs-lookup"><span data-stu-id="080af-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="080af-1173">10</span><span class="sxs-lookup"><span data-stu-id="080af-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="080af-1174">Ocupado</span><span class="sxs-lookup"><span data-stu-id="080af-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="080af-1175">11</span><span class="sxs-lookup"><span data-stu-id="080af-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="080af-1176">Imprimindo</span><span class="sxs-lookup"><span data-stu-id="080af-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="080af-1177">12</span><span class="sxs-lookup"><span data-stu-id="080af-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="080af-1178">Bandeja de Saída Cheia</span><span class="sxs-lookup"><span data-stu-id="080af-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="080af-1179">13</span><span class="sxs-lookup"><span data-stu-id="080af-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="080af-1180">Não disponível</span><span class="sxs-lookup"><span data-stu-id="080af-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="080af-1181">14</span><span class="sxs-lookup"><span data-stu-id="080af-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="080af-1182">Aguardando</span><span class="sxs-lookup"><span data-stu-id="080af-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="080af-1183">15</span><span class="sxs-lookup"><span data-stu-id="080af-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="080af-1184">Processing</span><span class="sxs-lookup"><span data-stu-id="080af-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="080af-1185">16</span><span class="sxs-lookup"><span data-stu-id="080af-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="080af-1186">Inicialização</span><span class="sxs-lookup"><span data-stu-id="080af-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="080af-1187">17</span><span class="sxs-lookup"><span data-stu-id="080af-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="080af-1188">Aquecendo</span><span class="sxs-lookup"><span data-stu-id="080af-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="080af-1189">18</span><span class="sxs-lookup"><span data-stu-id="080af-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="080af-1190">Toner baixo</span><span class="sxs-lookup"><span data-stu-id="080af-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="080af-1191">19</span><span class="sxs-lookup"><span data-stu-id="080af-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="080af-1192">Sem Toner</span><span class="sxs-lookup"><span data-stu-id="080af-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="080af-1193">20</span><span class="sxs-lookup"><span data-stu-id="080af-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="080af-1194">Apontador de página</span><span class="sxs-lookup"><span data-stu-id="080af-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="080af-1195">21</span><span class="sxs-lookup"><span data-stu-id="080af-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="080af-1196">Intervenção do usuário necessária</span><span class="sxs-lookup"><span data-stu-id="080af-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="080af-1197">22</span><span class="sxs-lookup"><span data-stu-id="080af-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="080af-1198">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="080af-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="080af-1199">23</span><span class="sxs-lookup"><span data-stu-id="080af-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="080af-1200">Porta Aberta</span><span class="sxs-lookup"><span data-stu-id="080af-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="080af-1201">24</span><span class="sxs-lookup"><span data-stu-id="080af-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="080af-1202">Servidor \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="080af-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="080af-1203">25</span><span class="sxs-lookup"><span data-stu-id="080af-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="080af-1204">Economia de energia</span><span class="sxs-lookup"><span data-stu-id="080af-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-1205">**PrinterStatus**</span><span class="sxs-lookup"><span data-stu-id="080af-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1206">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1208">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. hrPrinterStatus ")</span><span class="sxs-lookup"><span data-stu-id="080af-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="080af-1209">Informações de status para uma impressora que é diferente das informações especificadas na propriedade de **disponibilidade** do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="080af-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="080af-1210">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="080af-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Ocioso** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1214">Ocioso-para obter mais informações, consulte a seção comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="080af-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="080af-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Impressão** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="080af-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Aquecimento** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="080af-1217">Aquecendo</span><span class="sxs-lookup"><span data-stu-id="080af-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="080af-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Impressão interrompida** (6)</span><span class="sxs-lookup"><span data-stu-id="080af-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="080af-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span><span class="sxs-lookup"><span data-stu-id="080af-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-1220">**PrintJobDataType**</span><span class="sxs-lookup"><span data-stu-id="080af-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1222">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1223">Tipo de dados de um trabalho de impressão aguardando o dispositivo de impressão baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="080af-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1224">**Multiprocessador**</span><span class="sxs-lookup"><span data-stu-id="080af-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1225">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1226">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1227">Nome do spooler de impressão que lida com trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="080af-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="080af-1228">Exemplo: SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="080af-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="080af-1229">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="080af-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1230">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1231">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1232">Prioridade da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1232">Priority of the printer.</span></span> <span data-ttu-id="080af-1233">Os trabalhos em uma impressora de prioridade mais alta são agendados primeiro.</span><span class="sxs-lookup"><span data-stu-id="080af-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1234">**Checked**</span><span class="sxs-lookup"><span data-stu-id="080af-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1235">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1236">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1237">Se for **true**, a impressora será publicada no serviço de diretório de rede.</span><span class="sxs-lookup"><span data-stu-id="080af-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1238">**Em fila**</span><span class="sxs-lookup"><span data-stu-id="080af-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1239">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1240">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1241">Se **for true**, a impressora armazena em buffer e enfileira trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="080af-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1242">**RawOnly**</span><span class="sxs-lookup"><span data-stu-id="080af-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1243">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1244">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1245">Se **for true**, a impressora aceitará que apenas os dados brutos sejam colocados em spool.</span><span class="sxs-lookup"><span data-stu-id="080af-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1246">**Separador**</span><span class="sxs-lookup"><span data-stu-id="080af-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1247">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1248">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1249">Nome do arquivo usado para criar uma página separadora.</span><span class="sxs-lookup"><span data-stu-id="080af-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="080af-1250">Esta página é usada para separar trabalhos de impressão enviados para a impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="080af-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1252">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-1254">Nome do servidor que controla a impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="080af-1255">Se essa cadeia de caracteres for **nula**, a impressora será controlada localmente.</span><span class="sxs-lookup"><span data-stu-id="080af-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1256">**Compartilhado**</span><span class="sxs-lookup"><span data-stu-id="080af-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1257">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1258">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1259">Se for **true**, a impressora estará disponível como um recurso de rede compartilhado.</span><span class="sxs-lookup"><span data-stu-id="080af-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1260">**ShareName**</span><span class="sxs-lookup"><span data-stu-id="080af-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1262">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1263">Nome do compartilhamento do dispositivo de impressão baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="080af-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="080af-1264">Exemplo: " \\ \\ PRINTER2 de fotoserver1 \\ "</span><span class="sxs-lookup"><span data-stu-id="080af-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="080af-1265">**SpoolEnabled**</span><span class="sxs-lookup"><span data-stu-id="080af-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1266">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1268">Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="080af-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="080af-1269">Esta propriedade é obsoleta; Não use.</span><span class="sxs-lookup"><span data-stu-id="080af-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="080af-1270">Se for **true**, o spooling será habilitado para a impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="080af-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="080af-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1272">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080af-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1273">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1274">Data e hora em que uma impressora pode começar a imprimir um trabalho — se a impressora estiver limitada a imprimir em horários específicos.</span><span class="sxs-lookup"><span data-stu-id="080af-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="080af-1275">Esse valor é expresso como o tempo decorrido desde 12:00 AM GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="080af-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1276">**Status**</span><span class="sxs-lookup"><span data-stu-id="080af-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1279">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="080af-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="080af-1280">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="080af-1280">Current status of the object.</span></span> <span data-ttu-id="080af-1281">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="080af-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="080af-1282">Os status operacionais incluem: **OK**, **degradado** e **Pred falha** (um elemento, como uma unidade de disco rígido habilitada para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="080af-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="080af-1283">Os status não operacionais incluem: **erro**, **início**, **interrupção** e **serviço**.</span><span class="sxs-lookup"><span data-stu-id="080af-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="080af-1284">O último, **serviço**, pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="080af-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="080af-1285">Nem todo esse trabalho está online, ainda que o elemento gerenciado não seja **OK** nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="080af-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="080af-1286">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="080af-1287">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="080af-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="080af-1288">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="080af-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="080af-1289">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="080af-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="080af-1290">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="080af-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-1291">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="080af-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="080af-1292">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="080af-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="080af-1293">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="080af-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="080af-1294">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="080af-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="080af-1295">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="080af-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="080af-1296">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="080af-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="080af-1297">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="080af-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="080af-1298">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="080af-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="080af-1299">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="080af-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="080af-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1301">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="080af-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1302">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1303">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="080af-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="080af-1304">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="080af-1304">State of the logical device.</span></span> <span data-ttu-id="080af-1305">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (**não aplicável**) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="080af-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="080af-1306">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="080af-1307">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="080af-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="080af-1308">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="080af-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="080af-1309">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="080af-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="080af-1310">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="080af-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="080af-1311">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="080af-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="080af-1312">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="080af-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1313">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1315">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="080af-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="080af-1316">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="080af-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="080af-1317">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1318">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="080af-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1319">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="080af-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1320">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1321">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="080af-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="080af-1322">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="080af-1322">Name of the scoping system.</span></span>

<span data-ttu-id="080af-1323">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1324">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="080af-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1325">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080af-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1326">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="080af-1327">Data e hora da última redefinição da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="080af-1328">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1329">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="080af-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1330">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="080af-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1331">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1332">Data e hora em que uma impressora pode imprimir o último trabalho — se a impressora estiver limitada a imprimir em horários específicos.</span><span class="sxs-lookup"><span data-stu-id="080af-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="080af-1333">Esse valor é expresso como o tempo decorrido desde 12:00 AM GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="080af-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="080af-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1335">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="080af-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="080af-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="080af-1337">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](../wmisdk/standard-qualifiers.md) ("pixels por polegada")</span><span class="sxs-lookup"><span data-stu-id="080af-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="080af-1338">Resolução vertical, em pixels por polegada, da impressora.</span><span class="sxs-lookup"><span data-stu-id="080af-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="080af-1339">Essa propriedade é herdada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="080af-1340">**WorkOffline**</span><span class="sxs-lookup"><span data-stu-id="080af-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="080af-1341">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="080af-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="080af-1342">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="080af-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="080af-1343">Se **for true**, você poderá enfileirar trabalhos de impressão no computador quando a impressora estiver offline.</span><span class="sxs-lookup"><span data-stu-id="080af-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="080af-1344">Comentários</span><span class="sxs-lookup"><span data-stu-id="080af-1344">Remarks</span></span>

<span data-ttu-id="080af-1345">A classe de **\_ impressora Win32** é derivada [**da \_ impressora CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="080af-1346">Antes de chamar [**SWbemObject. \_ Put**](../wmisdk/swbemobject-put-.md) ou [**IWbemServices::P utinstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) para uma instância de **\_ impressora Win32** , o privilégio **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** para Visual Basic e o LoadDriver para os identificadores de script) deve ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="080af-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="080af-1347">Para obter mais informações, consulte [**constantes de privilégio**](../wmisdk/privilege-constants.md) e [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="080af-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="080af-1348">O exemplo de código VBScript a seguir mostra como habilitar o privilégio **SetLoadDriverPrivilege** no script.</span><span class="sxs-lookup"><span data-stu-id="080af-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="080af-1349">Para trabalhar com clusters de impressora do MSCS, use o assembly prnadmin.dll, ou então o namespace .NET Framework [System. Printing](/dotnet/api/system.printing) .</span><span class="sxs-lookup"><span data-stu-id="080af-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="080af-1350">O Windows usa as credenciais do usuário que está executando o script para determinar quais são as impressoras disponíveis.</span><span class="sxs-lookup"><span data-stu-id="080af-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="080af-1351">Portanto, se você estiver executando um script remotamente, você só poderá acessar qualquer impressora disponível para sua conta de usuário nesse sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="080af-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="080af-1352">Você não pode usar a classe de **\_ impressora do Win32** para impressoras em um cluster de impressão do MSCS.</span><span class="sxs-lookup"><span data-stu-id="080af-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="080af-1353">Em vez disso, talvez seja necessário usar a ferramenta PrinterAdmin (PrnAdmin.dll) ou o namespace .NET Framework [System. Printing](/dotnet/api/system.printing) .</span><span class="sxs-lookup"><span data-stu-id="080af-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="080af-1354">Se você estiver recuperando **PrinterStatus** = 3 ou **printerstate** = 0, talvez o driver de impressora não esteja alimentando informações precisas no WMI.</span><span class="sxs-lookup"><span data-stu-id="080af-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="080af-1355">O WMI recupera as informações da impressora do processo de spoolsv.exe.</span><span class="sxs-lookup"><span data-stu-id="080af-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="080af-1356">É possível que o driver de impressora não relate seu status ao spooler.</span><span class="sxs-lookup"><span data-stu-id="080af-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="080af-1357">Nesse caso, a **\_ impressora Win32** relata a impressora como **ociosa**.</span><span class="sxs-lookup"><span data-stu-id="080af-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="080af-1358">Exemplos</span><span class="sxs-lookup"><span data-stu-id="080af-1358">Examples</span></span>

<span data-ttu-id="080af-1359">O exemplo de [desenho de configuração de computador do PS usando](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) o PowerShell do Visio na galeria do TechNet usa a **\_ impressora Win32** para interagir com o modelo de automação do Visio para criar um desenho do Visio.</span><span class="sxs-lookup"><span data-stu-id="080af-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="080af-1360">O [script de informações do PC remoto do PowerShell](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) usa várias classes, incluindo a **\_ impressora Win32**, para recuperar informações sobre um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="080af-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="080af-1361">O exemplo de código do PowerShell a seguir mostra como determinar a impressora padrão do computador local.</span><span class="sxs-lookup"><span data-stu-id="080af-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="080af-1362">O exemplo de código VBScript a seguir descreve como recuperar estatísticas de impressora de instâncias da **\_ impressora Win32**.</span><span class="sxs-lookup"><span data-stu-id="080af-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="080af-1363">O exemplo de código Perl a seguir descreve como recuperar estatísticas de impressora de instâncias da **\_ impressora Win32**.</span><span class="sxs-lookup"><span data-stu-id="080af-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="080af-1364">O exemplo de código VBScript a seguir mostra como obter o nome da impressora padrão para um computador.</span><span class="sxs-lookup"><span data-stu-id="080af-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="080af-1365">Requisitos</span><span class="sxs-lookup"><span data-stu-id="080af-1365">Requirements</span></span>



| <span data-ttu-id="080af-1366">Requisito</span><span class="sxs-lookup"><span data-stu-id="080af-1366">Requirement</span></span> | <span data-ttu-id="080af-1367">Valor</span><span class="sxs-lookup"><span data-stu-id="080af-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="080af-1368">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="080af-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="080af-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="080af-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="080af-1370">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="080af-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="080af-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="080af-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="080af-1372">Namespace</span><span class="sxs-lookup"><span data-stu-id="080af-1372">Namespace</span></span><br/>                | <span data-ttu-id="080af-1373">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="080af-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="080af-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="080af-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="080af-1375"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="080af-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="080af-1376">DLL</span><span class="sxs-lookup"><span data-stu-id="080af-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="080af-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="080af-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="080af-1378">Confira também</span><span class="sxs-lookup"><span data-stu-id="080af-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="080af-1379">**\_Impressora CIM**</span><span class="sxs-lookup"><span data-stu-id="080af-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="080af-1380">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="080af-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="080af-1381">Tarefas do WMI: impressoras e impressão</span><span class="sxs-lookup"><span data-stu-id="080af-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
