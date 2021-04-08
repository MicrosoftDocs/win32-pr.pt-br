---
description: A \_ classe WMI SerialPortConfiguration do Win32 representa as configurações de transmissão de dados em uma porta serial baseada no Windows. Isso inclui configurações para estabelecer uma conexão e verificação de erro.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Classe Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920182"
---
# <a name="win32_serialportconfiguration-class"></a><span data-ttu-id="b054e-104">\_Classe Win32 SerialPortConfiguration</span><span class="sxs-lookup"><span data-stu-id="b054e-104">Win32\_SerialPortConfiguration class</span></span>

<span data-ttu-id="b054e-105">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortConfiguration do Win32** representa as configurações de transmissão de dados em uma porta serial baseada no Windows.</span><span class="sxs-lookup"><span data-stu-id="b054e-105">The **Win32\_SerialPortConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the settings for data transmission on a Windows-based serial port.</span></span> <span data-ttu-id="b054e-106">Isso inclui configurações para estabelecer uma conexão e verificação de erro.</span><span class="sxs-lookup"><span data-stu-id="b054e-106">This includes configurations for establishing a connection and error checking.</span></span>

<span data-ttu-id="b054e-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b054e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b054e-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b054e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b054e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b054e-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a><span data-ttu-id="b054e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b054e-110">Members</span></span>

<span data-ttu-id="b054e-111">A classe **Win32 \_ SerialPortConfiguration** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b054e-111">The **Win32\_SerialPortConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="b054e-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b054e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b054e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b054e-113">Properties</span></span>

<span data-ttu-id="b054e-114">A classe **Win32 \_ SerialPortConfiguration** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b054e-114">The **Win32\_SerialPortConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b054e-115">**AbortReadWriteOnError**</span><span class="sxs-lookup"><span data-stu-id="b054e-115">**AbortReadWriteOnError**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-118">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")</span><span class="sxs-lookup"><span data-stu-id="b054e-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fAbortOnError")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-119">Se **for true**, as operações de leitura e gravação serão encerradas se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="b054e-119">If **TRUE**, read and write operations are terminated if an error occurs.</span></span> <span data-ttu-id="b054e-120">Se **for true**, o driver encerrará todas as operações de leitura e gravação com um status de erro se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="b054e-120">If **TRUE**, the driver terminates all read and write operations with an error status if an error occurs.</span></span> <span data-ttu-id="b054e-121">O driver não aceitará nenhuma outra operação de comunicação até que o aplicativo confirme o erro.</span><span class="sxs-lookup"><span data-stu-id="b054e-121">The driver will not accept any further communications operations until the application acknowledges the error.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-122">**Taxa**</span><span class="sxs-lookup"><span data-stu-id="b054e-122">**BaudRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-123">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-125">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("estruturas de comunicação do win32api \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| baudrate")</span><span class="sxs-lookup"><span data-stu-id="b054e-125">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|BaudRate")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-126">Taxa de bauds (bits por segundo) na qual o dispositivo de comunicação Opera.</span><span class="sxs-lookup"><span data-stu-id="b054e-126">Baud (bits per second) rate at which the communications device operates.</span></span>

<span data-ttu-id="b054e-127">Exemplo: 9600</span><span class="sxs-lookup"><span data-stu-id="b054e-127">Example: 9600</span></span>

</dd> <dt>

<span data-ttu-id="b054e-128">**BinaryModeEnabled**</span><span class="sxs-lookup"><span data-stu-id="b054e-128">**BinaryModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-129">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-131">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")</span><span class="sxs-lookup"><span data-stu-id="b054e-131">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fBinary")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-132">Se **for true**, as transferências de dados no modo binário serão habilitadas para a porta serial.</span><span class="sxs-lookup"><span data-stu-id="b054e-132">If **TRUE**, binary-mode data transfers are enabled for the serial port.</span></span> <span data-ttu-id="b054e-133">Os sistemas de computador que executam o Windows só permitem transferências binárias por meio de portas seriais, portanto, esse valor é sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="b054e-133">Computer systems running Windows only allow binary transfers through serial ports, so this value is always **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-134">**BitsPerByte**</span><span class="sxs-lookup"><span data-stu-id="b054e-134">**BitsPerByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-137">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("estruturas de comunicação do win32api \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| bytes")</span><span class="sxs-lookup"><span data-stu-id="b054e-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ByteSize")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-138">Número de bits transmitidos e recebidos para cada byte de dados para a porta serial do Windows.</span><span class="sxs-lookup"><span data-stu-id="b054e-138">Number of bits transmitted and received for each byte of data for the Windows serial port.</span></span> <span data-ttu-id="b054e-139">O número pode variar com bits de correção de erro e controle, como bits de paridade.</span><span class="sxs-lookup"><span data-stu-id="b054e-139">The number may vary with control and error correction bits, such as parity bits.</span></span>

<span data-ttu-id="b054e-140">Exemplo: 8</span><span class="sxs-lookup"><span data-stu-id="b054e-140">Example: 8</span></span>

</dd> <dt>

<span data-ttu-id="b054e-141">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b054e-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-144">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="b054e-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b054e-145">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b054e-145">Short textual description of the current object.</span></span>

<span data-ttu-id="b054e-146">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b054e-146">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b054e-147">**ContinueXMitOnXOff**</span><span class="sxs-lookup"><span data-stu-id="b054e-147">**ContinueXMitOnXOff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-148">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-150">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")</span><span class="sxs-lookup"><span data-stu-id="b054e-150">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fTXContinueOnXoff")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-151">Se **for true**, as transmissões de dados continuarão quando o buffer de entrada entrar em **XOffXMitThreshold** bytes de estar cheio e o driver tiver transmitido o valor de **XOffChararcter** para parar de receber bytes.</span><span class="sxs-lookup"><span data-stu-id="b054e-151">If **TRUE**, data transmissions continue when the input buffer has come within **XOffXMitThreshold** bytes of being full and the driver has transmitted the **XOffChararcter** value to stop receiving bytes.</span></span> <span data-ttu-id="b054e-152">Se **for false**, a transmissão não continuará até que o buffer de entrada esteja dentro do **XOnXMitThreshold** bytes de estar vazio e o driver tenha transmitido o valor de **XOnCharacter** para retomar a recepção.</span><span class="sxs-lookup"><span data-stu-id="b054e-152">If **FALSE**, transmission does not continue until the input buffer is within **XOnXMitThreshold** bytes of being empty and the driver has transmitted the **XOnCharacter** value to resume reception.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-153">**CTSOutflowControl**</span><span class="sxs-lookup"><span data-stu-id="b054e-153">**CTSOutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-154">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-154">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-156">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")</span><span class="sxs-lookup"><span data-stu-id="b054e-156">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxCtsFlow")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-157">Se for **true**, o sinal Clear to send (CTS) será verificado antes de transmitir os dados.</span><span class="sxs-lookup"><span data-stu-id="b054e-157">If **TRUE**, the clear to send (CTS) signal is checked before transmitting data.</span></span> <span data-ttu-id="b054e-158">O CTS sinaliza que ambos os dispositivos na conexão serial estão prontos para transferir dados.</span><span class="sxs-lookup"><span data-stu-id="b054e-158">CTS signals that both devices on the serial connection are ready to transfer data.</span></span> <span data-ttu-id="b054e-159">A transmissão de dados é suspensa até que o sinal CTS seja fornecido.</span><span class="sxs-lookup"><span data-stu-id="b054e-159">Data transmission is suspended until the CTS signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-160">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b054e-160">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b054e-163">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="b054e-163">Textual description of the current object.</span></span>

<span data-ttu-id="b054e-164">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b054e-164">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b054e-165">**DiscardNULLBytes**</span><span class="sxs-lookup"><span data-stu-id="b054e-165">**DiscardNULLBytes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-166">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-168">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")</span><span class="sxs-lookup"><span data-stu-id="b054e-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fNull")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-169">Se **for true**, bytes **nulos** (caracteres) serão descartados quando forem recebidos.</span><span class="sxs-lookup"><span data-stu-id="b054e-169">If **TRUE**, **NULL** bytes (characters) are discarded when they are received.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-170">**DSROutflowControl**</span><span class="sxs-lookup"><span data-stu-id="b054e-170">**DSROutflowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-171">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-171">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-173">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")</span><span class="sxs-lookup"><span data-stu-id="b054e-173">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutxDsrFlow")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-174">Se for **true**, o controle de saída de dados será habilitado quando houver uma condição de Data Set Ready (DSR).</span><span class="sxs-lookup"><span data-stu-id="b054e-174">If **TRUE**, data outflow control is enabled when there is a data set ready (DSR) condition.</span></span> <span data-ttu-id="b054e-175">O DSR sinaliza que a conexão foi estabelecida pelos dispositivos na conexão serial.</span><span class="sxs-lookup"><span data-stu-id="b054e-175">DSR signals that the connection has been established by the devices on the serial connection.</span></span> <span data-ttu-id="b054e-176">A transmissão de dados DSR é suspensa até que o sinal de DSR seja fornecido.</span><span class="sxs-lookup"><span data-stu-id="b054e-176">DSR data transmission is suspended until the DSR signal is given.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-177">**DSRSensitivity**</span><span class="sxs-lookup"><span data-stu-id="b054e-177">**DSRSensitivity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-178">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-178">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-180">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")</span><span class="sxs-lookup"><span data-stu-id="b054e-180">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDsrSensitivity")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-181">Se for **true**, o driver de comunicação será sensível ao estado do sinal DSR.</span><span class="sxs-lookup"><span data-stu-id="b054e-181">If **TRUE**, the communications driver is sensitive to the state of the DSR signal.</span></span> <span data-ttu-id="b054e-182">O driver ignora todos os bytes recebidos, a menos que a linha de entrada do modem DSR esteja alta.</span><span class="sxs-lookup"><span data-stu-id="b054e-182">The driver ignores any bytes received, unless the DSR modem input line is high.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-183">**DTRFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="b054e-183">**DTRFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-186">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")</span><span class="sxs-lookup"><span data-stu-id="b054e-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fDtrControl")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-187">Uso do controle de fluxo de Data Terminal Ready (DTR) depois que uma conexão é estabelecida.</span><span class="sxs-lookup"><span data-stu-id="b054e-187">Use of the data terminal ready (DTR) flow control after a connection has been established.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="b054e-188">**Habilitar** ("habilitar")</span><span class="sxs-lookup"><span data-stu-id="b054e-188">**Enable** ("Enable")</span></span>


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="b054e-189">**Desabilitar** ("Desabilitar")</span><span class="sxs-lookup"><span data-stu-id="b054e-189">**Disable** ("Disable")</span></span>


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="b054e-190">**Handshake** ("handshake")</span><span class="sxs-lookup"><span data-stu-id="b054e-190">**Handshake** ("Handshake")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b054e-191">**EOFCharacter**</span><span class="sxs-lookup"><span data-stu-id="b054e-191">**EOFCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-192">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-194">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")</span><span class="sxs-lookup"><span data-stu-id="b054e-194">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EofChar")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-195">Valor do caractere usado para sinalizar o fim dos dados.</span><span class="sxs-lookup"><span data-stu-id="b054e-195">Value of the character used to signal the end of data.</span></span>

<span data-ttu-id="b054e-196">Exemplo: ^ Z</span><span class="sxs-lookup"><span data-stu-id="b054e-196">Example: ^Z</span></span>

</dd> <dt>

<span data-ttu-id="b054e-197">**ErrorReplaceCharacter**</span><span class="sxs-lookup"><span data-stu-id="b054e-197">**ErrorReplaceCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-198">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-200">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")</span><span class="sxs-lookup"><span data-stu-id="b054e-200">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|ErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-201">Valor do caractere usado para substituir bytes recebidos por um erro de paridade.</span><span class="sxs-lookup"><span data-stu-id="b054e-201">Value of the character used to replace bytes received with a parity error.</span></span>

<span data-ttu-id="b054e-202">Exemplo: ^ C</span><span class="sxs-lookup"><span data-stu-id="b054e-202">Example: ^C</span></span>

</dd> <dt>

<span data-ttu-id="b054e-203">**ErrorReplacementEnabled**</span><span class="sxs-lookup"><span data-stu-id="b054e-203">**ErrorReplacementEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-204">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-204">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-205">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-206">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")</span><span class="sxs-lookup"><span data-stu-id="b054e-206">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fErrorChar")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-207">Se **for true**, bytes recebidos com erros de paridade serão substituídos pelo valor **ErrorReplaceCharacter** .</span><span class="sxs-lookup"><span data-stu-id="b054e-207">If **TRUE**, bytes received with parity errors are replaced with the **ErrorReplaceCharacter** value.</span></span> <span data-ttu-id="b054e-208">Os caracteres com erros de paridade serão substituídos apenas se essa propriedade for **true** e a paridade estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="b054e-208">Characters with parity errors are only replaced if this property is **TRUE** and the parity is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-209">**EventCharacter**</span><span class="sxs-lookup"><span data-stu-id="b054e-209">**EventCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-210">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-210">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-212">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")</span><span class="sxs-lookup"><span data-stu-id="b054e-212">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|EvtChar")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-213">Valor do caractere de controle usado para sinalizar um evento, como o fim do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b054e-213">Value of the control character that is used to signal an event, such as end of file.</span></span>

<span data-ttu-id="b054e-214">Exemplo: ^ e</span><span class="sxs-lookup"><span data-stu-id="b054e-214">Example: ^e</span></span>

</dd> <dt>

<span data-ttu-id="b054e-215">**IsBusy**</span><span class="sxs-lookup"><span data-stu-id="b054e-215">**IsBusy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-216">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-218">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| File Functions \| CreateFile")</span><span class="sxs-lookup"><span data-stu-id="b054e-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|File Functions\|CreateFile")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-219">Se for **true**, a porta serial estará ocupada.</span><span class="sxs-lookup"><span data-stu-id="b054e-219">If **TRUE**, the serial port is busy.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-220">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b054e-220">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-223">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| hardware \\ \\ DeviceMap \\ \\ SerialComm")</span><span class="sxs-lookup"><span data-stu-id="b054e-223">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Hardware\\\\DeviceMap\\\\SerialComm")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-224">Nome da porta serial do Windows.</span><span class="sxs-lookup"><span data-stu-id="b054e-224">Name of the Windows serial port.</span></span>

<span data-ttu-id="b054e-225">Exemplo: "COM1"</span><span class="sxs-lookup"><span data-stu-id="b054e-225">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="b054e-226">**Parity**</span><span class="sxs-lookup"><span data-stu-id="b054e-226">**Parity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-227">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-229">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)de \| paridade")</span><span class="sxs-lookup"><span data-stu-id="b054e-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|Parity")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-230">Método de verificação de paridade a ser usado.</span><span class="sxs-lookup"><span data-stu-id="b054e-230">Method of parity checking to be used.</span></span> <span data-ttu-id="b054e-231">A paridade é usada como uma técnica de verificação de erros em que um bit de paridade extra é incluído em cada unidade de dados.</span><span class="sxs-lookup"><span data-stu-id="b054e-231">Parity is used as an error checking technique where an extra parity bit is included with every unit of data.</span></span> <span data-ttu-id="b054e-232">O receptor pode, então, verificar a validade dos dados contando os bits que estão definidos.</span><span class="sxs-lookup"><span data-stu-id="b054e-232">The receiver can then verify the validity of the data by counting the bits that are set.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="b054e-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** ("nenhum")</span><span class="sxs-lookup"><span data-stu-id="b054e-233"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-234">Verificação de paridade não usada.</span><span class="sxs-lookup"><span data-stu-id="b054e-234">Parity checking not used.</span></span>

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span data-ttu-id="b054e-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Ímpar** ("ímpar")</span><span class="sxs-lookup"><span data-stu-id="b054e-235"><span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Odd** ("Odd")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-236">Define o bit de paridade de modo que a contagem de bits definida seja um número ímpar.</span><span class="sxs-lookup"><span data-stu-id="b054e-236">Sets the parity bit so that the count of bits set is an odd number.</span></span>

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span data-ttu-id="b054e-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Par** ("uniforme")</span><span class="sxs-lookup"><span data-stu-id="b054e-237"><span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-238">Define o bit de paridade de modo que a contagem de bits definida seja um número par.</span><span class="sxs-lookup"><span data-stu-id="b054e-238">Sets the parity bit so that the count of bits set is an even number.</span></span>

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span data-ttu-id="b054e-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Marcar** ("Mark")</span><span class="sxs-lookup"><span data-stu-id="b054e-239"><span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-240">Deixa o bit de paridade definido como 1.</span><span class="sxs-lookup"><span data-stu-id="b054e-240">Leaves the parity bit set to 1.</span></span>

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span data-ttu-id="b054e-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Espaço** ("espaço")</span><span class="sxs-lookup"><span data-stu-id="b054e-241"><span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Space** ("Space")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-242">Deixa o bit de paridade definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b054e-242">Leaves the parity bit set to 0 (zero).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b054e-243">**ParityCheckEnabled**</span><span class="sxs-lookup"><span data-stu-id="b054e-243">**ParityCheckEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-244">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b054e-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-246">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")</span><span class="sxs-lookup"><span data-stu-id="b054e-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fParity")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-247">Se for **true**, a verificação de paridade estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="b054e-247">If **TRUE**, parity checking is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-248">**RTSFlowControlType**</span><span class="sxs-lookup"><span data-stu-id="b054e-248">**RTSFlowControlType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b054e-251">Solicitação para enviar o controle de fluxo (RTS).</span><span class="sxs-lookup"><span data-stu-id="b054e-251">Request to send (RTS) flow control.</span></span> <span data-ttu-id="b054e-252">O RTS é usado para sinalizar que os dados estão disponíveis para transmissão.</span><span class="sxs-lookup"><span data-stu-id="b054e-252">RTS is used to signal that data is available for transmission.</span></span>

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span data-ttu-id="b054e-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** ("habilitar")</span><span class="sxs-lookup"><span data-stu-id="b054e-253"><span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-254">O RTS é deixado para a sessão de transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="b054e-254">RTS is left on for the data transfer session.</span></span>

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="b054e-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Desabilitar** ("Desabilitar")</span><span class="sxs-lookup"><span data-stu-id="b054e-255"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** ("Disable")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-256">O RTS é ignorado após o primeiro sinal de RTS ser recebido.</span><span class="sxs-lookup"><span data-stu-id="b054e-256">RTS is ignored after the first RTS signal is received.</span></span>

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span data-ttu-id="b054e-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("handshake")</span><span class="sxs-lookup"><span data-stu-id="b054e-257"><span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-258">O RTS será desativado se o buffer de transmissão tiver mais de três trimestres cheios e o RTS for ativado quando o buffer for menor do que a metade completa.</span><span class="sxs-lookup"><span data-stu-id="b054e-258">RTS is turned off if the transmission buffer is more than three-quarters full, and RTS is turned on when the buffer is less than one-half full.</span></span>

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span data-ttu-id="b054e-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Ativar/desativar** ("alternar")</span><span class="sxs-lookup"><span data-stu-id="b054e-259"><span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Toggle** ("Toggle")</span></span>


</dt> <dd>

<span data-ttu-id="b054e-260">O RTS será ativado se houver algum buffer de dados para transmissão.</span><span class="sxs-lookup"><span data-stu-id="b054e-260">RTS is turned on if there is any data buffered for transmission.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b054e-261">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="b054e-261">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-264">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="b054e-264">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b054e-265">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b054e-265">Identifier by which the current object is known.</span></span>

<span data-ttu-id="b054e-266">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b054e-266">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="b054e-267">**StopBits**</span><span class="sxs-lookup"><span data-stu-id="b054e-267">**StopBits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b054e-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-270">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits")</span><span class="sxs-lookup"><span data-stu-id="b054e-270">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|StopBits")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-271">Número de bits de parada a serem usados.</span><span class="sxs-lookup"><span data-stu-id="b054e-271">Number of stop bits to be used.</span></span> <span data-ttu-id="b054e-272">Parar bits separa cada unidade de dados em uma conexão serial assíncrona.</span><span class="sxs-lookup"><span data-stu-id="b054e-272">Stop bits separate each unit of data on an asynchronous serial connection.</span></span> <span data-ttu-id="b054e-273">Eles também são enviados continuamente quando não há dados disponíveis para transmissão.</span><span class="sxs-lookup"><span data-stu-id="b054e-273">They are also sent continuously when no data is available for transmission.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="b054e-274">**1** ("1")</span><span class="sxs-lookup"><span data-stu-id="b054e-274">**1** ("1")</span></span>


</dt> <dd></dd> <dt>

<span id="1.5"></span>

<span data-ttu-id="b054e-275">**1,5** ("1,5")</span><span class="sxs-lookup"><span data-stu-id="b054e-275">**1.5** ("1.5")</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="b054e-276">**2** ("2")</span><span class="sxs-lookup"><span data-stu-id="b054e-276">**2** ("2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b054e-277">**XOffCharacter**</span><span class="sxs-lookup"><span data-stu-id="b054e-277">**XOffCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-278">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-278">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-279">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-280">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")</span><span class="sxs-lookup"><span data-stu-id="b054e-280">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffChar")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-281">Valor do caractere XOFF para transmissão e recepção.</span><span class="sxs-lookup"><span data-stu-id="b054e-281">Value of the XOFF character for both transmission and reception.</span></span> <span data-ttu-id="b054e-282">XOFF é um controle de software para interromper a transmissão de dados (enquanto RTS e CTS são controles de hardware).</span><span class="sxs-lookup"><span data-stu-id="b054e-282">XOFF is a software control to stop the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="b054e-283">XON retoma a transmissão.</span><span class="sxs-lookup"><span data-stu-id="b054e-283">XON resumes the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-284">**XOffXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="b054e-284">**XOffXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-285">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-285">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-286">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-286">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-287">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")</span><span class="sxs-lookup"><span data-stu-id="b054e-287">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XoffLim")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-288">Número máximo de bytes permitidos no buffer de entrada antes que o caractere XOFF seja enviado.</span><span class="sxs-lookup"><span data-stu-id="b054e-288">Maximum number of bytes allowed in the input buffer before the XOFF character is sent.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-289">**XOnCharacter**</span><span class="sxs-lookup"><span data-stu-id="b054e-289">**XOnCharacter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-290">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-292">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")</span><span class="sxs-lookup"><span data-stu-id="b054e-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonChar")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-293">Valor do caractere XON para transmissão e recepção.</span><span class="sxs-lookup"><span data-stu-id="b054e-293">Value of the XON character for both transmission and reception.</span></span> <span data-ttu-id="b054e-294">XON é um controle de software para retomar a transmissão de dados (enquanto RTS e CTS são controles de hardware).</span><span class="sxs-lookup"><span data-stu-id="b054e-294">XON is a software control to resume the transmission of data (whereas RTS and CTS are hardware controls).</span></span> <span data-ttu-id="b054e-295">XOFF interrompe a transmissão.</span><span class="sxs-lookup"><span data-stu-id="b054e-295">XOFF stops the transmission.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-296">**XOnXMitThreshold**</span><span class="sxs-lookup"><span data-stu-id="b054e-296">**XOnXMitThreshold**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-297">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-297">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-299">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")</span><span class="sxs-lookup"><span data-stu-id="b054e-299">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|XonLim")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-300">Número mínimo de bytes permitidos no buffer de entrada antes que o caractere XON seja enviado.</span><span class="sxs-lookup"><span data-stu-id="b054e-300">Minimum number of bytes allowed in the input buffer before the XON character is sent.</span></span> <span data-ttu-id="b054e-301">Essa propriedade funciona em conjunto com **XOffXMitThreshold** para regular a taxa na qual os dados são transferidos.</span><span class="sxs-lookup"><span data-stu-id="b054e-301">This property works in conjunction with **XOffXMitThreshold** to regulate the rate at which data is transferred.</span></span>

</dd> <dt>

<span data-ttu-id="b054e-302">**XOnXOffInFlowControl**</span><span class="sxs-lookup"><span data-stu-id="b054e-302">**XOnXOffInFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-303">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-303">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-305">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")</span><span class="sxs-lookup"><span data-stu-id="b054e-305">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fInX")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-306">Se **for true**, o controle de fluxo XON/XOFF será usado durante a recepção.</span><span class="sxs-lookup"><span data-stu-id="b054e-306">If **TRUE**, XON/XOFF flow control is used during reception.</span></span> <span data-ttu-id="b054e-307">Se **for true**, o valor de **XOffCharacter** será enviado quando o buffer de entrada ficar dentro de **XOffXMitThreshold** bytes de estar cheio, e o valor de **XOnCharacter** será enviado quando o buffer de entrada entrar em **XOnXMitThreshold** bytes de estar vazio.</span><span class="sxs-lookup"><span data-stu-id="b054e-307">If **TRUE**, the **XOffCharacter** value is sent when the input buffer comes within **XOffXMitThreshold** bytes of being full, and the **XOnCharacter** value is sent when the input buffer comes within **XOnXMitThreshold** bytes of being empty.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b054e-308"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b054e-308"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b054e-309">FALSE</span><span class="sxs-lookup"><span data-stu-id="b054e-309">FALSE</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b054e-310"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b054e-310"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b054e-311">TRUE</span><span class="sxs-lookup"><span data-stu-id="b054e-311">TRUE</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b054e-312">**XOnXOffOutFlowControl**</span><span class="sxs-lookup"><span data-stu-id="b054e-312">**XOnXOffOutFlowControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b054e-313">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b054e-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b054e-314">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b054e-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b054e-315">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")</span><span class="sxs-lookup"><span data-stu-id="b054e-315">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Communication Structures\|[**DCB**](/windows/win32/api/winbase/ns-winbase-dcb)\|fOutX")</span></span>
</dt> </dl>

<span data-ttu-id="b054e-316">O **XOnXOffOutFlowControl** especifica se o controle de fluxo XON ou XOFF é usado durante a transmissão.</span><span class="sxs-lookup"><span data-stu-id="b054e-316">The **XOnXOffOutFlowControl** specifies whether XON or XOFF flow control is used during transmission.</span></span> <span data-ttu-id="b054e-317">Se **for true**, a transmissão será interrompida quando o valor de **XOffCharacter** for recebido e iniciar novamente quando o valor de **XOnCharacter** for recebido.</span><span class="sxs-lookup"><span data-stu-id="b054e-317">If **TRUE**, transmission stops when the **XOffCharacter** value is received and starts again when the **XOnCharacter** value is received.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b054e-318">Comentários</span><span class="sxs-lookup"><span data-stu-id="b054e-318">Remarks</span></span>

<span data-ttu-id="b054e-319">A classe **Win32 \_ SerialPortConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="b054e-319">The **Win32\_SerialPortConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b054e-320">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b054e-320">Requirements</span></span>



| <span data-ttu-id="b054e-321">Requisito</span><span class="sxs-lookup"><span data-stu-id="b054e-321">Requirement</span></span> | <span data-ttu-id="b054e-322">Valor</span><span class="sxs-lookup"><span data-stu-id="b054e-322">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b054e-323">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b054e-323">Minimum supported client</span></span><br/> | <span data-ttu-id="b054e-324">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b054e-324">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b054e-325">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b054e-325">Minimum supported server</span></span><br/> | <span data-ttu-id="b054e-326">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b054e-326">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b054e-327">Namespace</span><span class="sxs-lookup"><span data-stu-id="b054e-327">Namespace</span></span><br/>                | <span data-ttu-id="b054e-328">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b054e-328">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b054e-329">MOF</span><span class="sxs-lookup"><span data-stu-id="b054e-329">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b054e-330"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b054e-330"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b054e-331">DLL</span><span class="sxs-lookup"><span data-stu-id="b054e-331">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b054e-332"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b054e-332"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b054e-333">Confira também</span><span class="sxs-lookup"><span data-stu-id="b054e-333">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b054e-334">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b054e-334">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="b054e-335">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="b054e-335">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
