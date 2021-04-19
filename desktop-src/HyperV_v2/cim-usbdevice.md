---
description: As características de gerenciamento de um dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: Classe CIM_USBDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775739"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a><span data-ttu-id="6ff50-103">Classe CIM_USBDevice (gerenciamento do Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="6ff50-103">CIM_USBDevice class (Hyper-V management)</span></span>

<span data-ttu-id="6ff50-104">As características de gerenciamento de um dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-104">The management characteristics of a USB device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ff50-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a><span data-ttu-id="6ff50-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6ff50-106">Members</span></span>

<span data-ttu-id="6ff50-107">A classe **CIM \_ UsbDevice** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6ff50-107">The **CIM\_USBDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="6ff50-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ff50-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="6ff50-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ff50-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6ff50-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ff50-110">Methods</span></span>

<span data-ttu-id="6ff50-111">A classe **CIM \_ UsbDevice** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6ff50-111">The **CIM\_USBDevice** class has these methods.</span></span>



| <span data-ttu-id="6ff50-112">Método</span><span class="sxs-lookup"><span data-stu-id="6ff50-112">Method</span></span>                                               | <span data-ttu-id="6ff50-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ff50-113">Description</span></span>                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [<span data-ttu-id="6ff50-114">**Getdescriptor**</span><span class="sxs-lookup"><span data-stu-id="6ff50-114">**GetDescriptor**</span></span>](cim-usbdevice-getdescriptor.md) | <span data-ttu-id="6ff50-115">Recupera um descritor de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-115">Retrieves a USB device descriptor.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6ff50-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ff50-116">Properties</span></span>

<span data-ttu-id="6ff50-117">A classe **CIM \_ UsbDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6ff50-117">The **CIM\_USBDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ff50-118">**ClassCode**</span><span class="sxs-lookup"><span data-stu-id="6ff50-118">**ClassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-119">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-119">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-121">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bDeviceClass")</span><span class="sxs-lookup"><span data-stu-id="6ff50-121">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceClass")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-122">O código de classe USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-122">The USB class code.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-123">**CommandTimeOut**</span><span class="sxs-lookup"><span data-stu-id="6ff50-123">**CommandTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-124">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6ff50-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-126">Um intervalo de tempo limite que é configurável por aplicativos de gerenciamento que dão suporte ao redirecionamento de USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-126">A timeout interval that is configurable by management applications that support USB redirection.</span></span> <span data-ttu-id="6ff50-127">Quando o serviço de redirecionamento redireciona um comando de dispositivo USB para um dispositivo remoto e o dispositivo remoto não responde antes do intervalo de tempo limite, o serviço de redirecionamento emulará um evento de ejeção de mídia.</span><span class="sxs-lookup"><span data-stu-id="6ff50-127">When the redirection service redirects a USB device command to a remote device, and the remote device does not respond before timeout interval, the redirection service will emulate a media eject event.</span></span> <span data-ttu-id="6ff50-128">Além disso, o serviço pode tentar novamente o comando ou tentar restabelecer a conexão com o dispositivo remoto.</span><span class="sxs-lookup"><span data-stu-id="6ff50-128">In addition, the service may re-try the command or try to re-establish the connection to the remote device.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-129">**CurrentAlternateSettings**</span><span class="sxs-lookup"><span data-stu-id="6ff50-129">**CurrentAlternateSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-130">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-132">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ UsbDevice**.**CurrentConfigValue**")</span><span class="sxs-lookup"><span data-stu-id="6ff50-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentConfigValue**")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-133">Uma matriz que contém as configurações alternativas para cada interface na configuração atual do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff50-133">An array that contains the alternate settings for each interface in the current configuration of the device.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-134">**CurrentConfigValue**</span><span class="sxs-lookup"><span data-stu-id="6ff50-134">**CurrentConfigValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-135">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-135">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-137">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ UsbDevice**.**CurrentAlternateSettings**")</span><span class="sxs-lookup"><span data-stu-id="6ff50-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_USBDevice**.**CurrentAlternateSettings**")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-138">A configuração selecionada no momento para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff50-138">The configuration currently selected for the device.</span></span> <span data-ttu-id="6ff50-139">Se esse valor for zero, o dispositivo não será configurado.</span><span class="sxs-lookup"><span data-stu-id="6ff50-139">If this value is zero, the Device is not configured.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-140">**DeviceReleaseNumber**</span><span class="sxs-lookup"><span data-stu-id="6ff50-140">**DeviceReleaseNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-141">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ff50-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-143">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bcdDevice")</span><span class="sxs-lookup"><span data-stu-id="6ff50-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdDevice")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-144">O número de liberação do dispositivo no formato BCD.</span><span class="sxs-lookup"><span data-stu-id="6ff50-144">The device release number in BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-145">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="6ff50-145">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ff50-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| iManufacturer")</span><span class="sxs-lookup"><span data-stu-id="6ff50-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iManufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-149">A cadeia de caracteres do fabricante do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff50-149">The manufacturer string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-150">**MaxPacketSize**</span><span class="sxs-lookup"><span data-stu-id="6ff50-150">**MaxPacketSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-151">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-151">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-153">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bMaxPacketSize")</span><span class="sxs-lookup"><span data-stu-id="6ff50-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bMaxPacketSize")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-154">O tamanho máximo do pacote para o ponto de extremidade de USB zero.</span><span class="sxs-lookup"><span data-stu-id="6ff50-154">The maximum packet size for the USB zero endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-155">**NumberOfConfigs**</span><span class="sxs-lookup"><span data-stu-id="6ff50-155">**NumberOfConfigs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-156">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-156">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-158">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bNumConfigurations")</span><span class="sxs-lookup"><span data-stu-id="6ff50-158">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bNumConfigurations")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-159">O número de configurações de dispositivo que são definidas para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff50-159">The number of device configurations that are defined for the Device.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-160">**Product**</span><span class="sxs-lookup"><span data-stu-id="6ff50-160">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ff50-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-163">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| iProduct")</span><span class="sxs-lookup"><span data-stu-id="6ff50-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iProduct")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-164">A cadeia de caracteres do produto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff50-164">The product string of the device.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-165">**ProductID**</span><span class="sxs-lookup"><span data-stu-id="6ff50-165">**ProductID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-166">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ff50-166">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-168">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| idProduct")</span><span class="sxs-lookup"><span data-stu-id="6ff50-168">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idProduct")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-169">A ID do produto atribuída ao dispositivo pelo fabricante.</span><span class="sxs-lookup"><span data-stu-id="6ff50-169">The product ID assigned to the device by manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-170">**ProtocolCode**</span><span class="sxs-lookup"><span data-stu-id="6ff50-170">**ProtocolCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-171">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-171">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-173">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bDeviceProtocol")</span><span class="sxs-lookup"><span data-stu-id="6ff50-173">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-174">O código do protocolo USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-174">The USB protocol code.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-175">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="6ff50-175">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ff50-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-178">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| iSerialNumber")</span><span class="sxs-lookup"><span data-stu-id="6ff50-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|iSerialNumber")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-179">O número de série do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff50-179">The serial number of the device.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-180">**SubclassCode**</span><span class="sxs-lookup"><span data-stu-id="6ff50-180">**SubclassCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-181">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="6ff50-181">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-183">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bDeviceSubClass")</span><span class="sxs-lookup"><span data-stu-id="6ff50-183">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bDeviceSubClass")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-184">O código de subclasse USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-184">The USB subclass code.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-185">**USBVersion**</span><span class="sxs-lookup"><span data-stu-id="6ff50-185">**USBVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-186">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ff50-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-188">A versão USB mais recente com suporte do dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="6ff50-188">The latest USB Version supported by the USB Device.</span></span> <span data-ttu-id="6ff50-189">A propriedade é expressa como um formato decimal codificado em binário (BCD) que contém um ponto decimal entre o 2º e o terceiro dígitos.</span><span class="sxs-lookup"><span data-stu-id="6ff50-189">The property is expressed as a binary-coded decimal (BCD) that contains a decimal point between the 2nd and 3rd digits.</span></span> <span data-ttu-id="6ff50-190">Por exemplo, um valor de 0x201 indica que a versão 2, 1 tem suporte.</span><span class="sxs-lookup"><span data-stu-id="6ff50-190">For example, a value of 0x201 indicates that version 2.01 is supported.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-191">**USBVersionInBCD**</span><span class="sxs-lookup"><span data-stu-id="6ff50-191">**USBVersionInBCD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-192">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ff50-192">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-194">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bcdUSB")</span><span class="sxs-lookup"><span data-stu-id="6ff50-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|bcdUSB")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-195">O número de especificação USB com o qual o dispositivo está em conformidade.</span><span class="sxs-lookup"><span data-stu-id="6ff50-195">The USB specification number that the device complies with.</span></span> <span data-ttu-id="6ff50-196">Essa propriedade é formatada com o formato BCD.</span><span class="sxs-lookup"><span data-stu-id="6ff50-196">This property is formatted with BCD format.</span></span>

</dd> <dt>

<span data-ttu-id="6ff50-197">**VendorID**</span><span class="sxs-lookup"><span data-stu-id="6ff50-197">**VendorID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ff50-198">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6ff50-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ff50-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ff50-200">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| idVendor")</span><span class="sxs-lookup"><span data-stu-id="6ff50-200">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Universal Serial Bus Specification.USB-IF\|Standard Device Descriptor\|idVendor")</span></span>
</dt> </dl>

<span data-ttu-id="6ff50-201">A ID do fornecedor atribuída ao dispositivo por USB.org.</span><span class="sxs-lookup"><span data-stu-id="6ff50-201">The vendor ID assigned to the device by USB.org.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ff50-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ff50-202">Requirements</span></span>



| <span data-ttu-id="6ff50-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ff50-203">Requirement</span></span> | <span data-ttu-id="6ff50-204">Valor</span><span class="sxs-lookup"><span data-stu-id="6ff50-204">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff50-205">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ff50-205">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff50-206">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6ff50-206">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6ff50-207">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ff50-207">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff50-208">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6ff50-208">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6ff50-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ff50-209">Namespace</span></span><br/>                | <span data-ttu-id="6ff50-210">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6ff50-210">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ff50-211">MOF</span><span class="sxs-lookup"><span data-stu-id="6ff50-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ff50-212"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ff50-212"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ff50-213">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff50-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff50-214"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ff50-214"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ff50-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ff50-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff50-216">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6ff50-216">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

