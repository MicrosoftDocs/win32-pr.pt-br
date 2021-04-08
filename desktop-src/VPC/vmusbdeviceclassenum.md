---
title: Enumeração VMUSBDeviceClassEnum (VPCCOMInterfaces. h)
description: Especifica a classe de dispositivo USB.
ms.assetid: 3f5044ea-f7a4-4524-bfb8-55db22732f81
keywords:
- VMUSBDeviceClassEnum de enumeração Virtual PC
topic_type:
- apiref
api_name:
- VMUSBDeviceClassEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70335ae083ac2a80717ae64cc8c76f0aff9e791b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085963"
---
# <a name="vmusbdeviceclassenum-enumeration"></a><span data-ttu-id="71a8e-104">Enumeração VMUSBDeviceClassEnum</span><span class="sxs-lookup"><span data-stu-id="71a8e-104">VMUSBDeviceClassEnum enumeration</span></span>

<span data-ttu-id="71a8e-105">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71a8e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="71a8e-106">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="71a8e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="71a8e-107">Especifica a classe de dispositivo USB.</span><span class="sxs-lookup"><span data-stu-id="71a8e-107">Specifies the USB device class.</span></span>

## <a name="syntax"></a><span data-ttu-id="71a8e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71a8e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUSBDeviceClass_InterfaceDescriptor  = 0x00,
  vmUSBDeviceClass_Audio                = 0x01,
  vmUSBDeviceClass_Communication        = 0x02,
  vmUSBDeviceClass_HID                  = 0x03,
  vmUSBDeviceClass_Physical             = 0x05,
  vmUSBDeviceClass_Image                = 0x06,
  vmUSBDeviceClass_Printer              = 0x07,
  vmUSBDeviceClass_MassStorage          = 0x08,
  vmUSBDeviceClass_Hub                  = 0x09,
  vmUSBDeviceClass_CDCData              = 0x0A,
  vmUSBDeviceClass_SmartCard            = 0x0B,
  vmUSBDeviceClass_ContentSecurity      = 0x0D,
  vmUSBDeviceClass_Video                = 0x0E,
  vmUSBDeviceClass_PersonalHealthcare   = 0x0F,
  vmUSBDeviceClass_DiagnosticDevice     = 0xDC,
  vmUSBDeviceClass_WirelessController   = 0xE0,
  vmUSBDeviceClass_Miscellaneous        = 0xEF,
  vmUSBDeviceClass_ApplicationSpecific  = 0xFE,
  vmUSBDeviceClass_VendorSpecific       = 0xFF
} VMUSBDeviceClassEnum;
```



## <a name="constants"></a><span data-ttu-id="71a8e-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="71a8e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="71a8e-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass \_ InterfaceDescriptor**</span><span class="sxs-lookup"><span data-stu-id="71a8e-110"><span id="vmUSBDeviceClass_InterfaceDescriptor"></span><span id="vmusbdeviceclass_interfacedescriptor"></span><span id="VMUSBDEVICECLASS_INTERFACEDESCRIPTOR"></span>**vmUSBDeviceClass\_InterfaceDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-111">Um dispositivo não identificado.</span><span class="sxs-lookup"><span data-stu-id="71a8e-111">An unidentified device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**\_áudio vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-112"><span id="vmUSBDeviceClass_Audio"></span><span id="vmusbdeviceclass_audio"></span><span id="VMUSBDEVICECLASS_AUDIO"></span>**vmUSBDeviceClass\_Audio**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-113">Dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="71a8e-113">Audio device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**\_comunicação vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-114"><span id="vmUSBDeviceClass_Communication"></span><span id="vmusbdeviceclass_communication"></span><span id="VMUSBDEVICECLASS_COMMUNICATION"></span>**vmUSBDeviceClass\_Communication**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-115">Dispositivo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="71a8e-115">Communication device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass \_ HID**</span><span class="sxs-lookup"><span data-stu-id="71a8e-116"><span id="vmUSBDeviceClass_HID"></span><span id="vmusbdeviceclass_hid"></span><span id="VMUSBDEVICECLASS_HID"></span>**vmUSBDeviceClass\_HID**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-117">Dispositivo HID.</span><span class="sxs-lookup"><span data-stu-id="71a8e-117">HID device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass \_ físico**</span><span class="sxs-lookup"><span data-stu-id="71a8e-118"><span id="vmUSBDeviceClass_Physical"></span><span id="vmusbdeviceclass_physical"></span><span id="VMUSBDEVICECLASS_PHYSICAL"></span>**vmUSBDeviceClass\_Physical**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-119">Dispositivo de sensor físico.</span><span class="sxs-lookup"><span data-stu-id="71a8e-119">Physical sensory device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**\_imagem vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-120"><span id="vmUSBDeviceClass_Image"></span><span id="vmusbdeviceclass_image"></span><span id="VMUSBDEVICECLASS_IMAGE"></span>**vmUSBDeviceClass\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-121">Dispositivo de digitalização ou geração de imagens.</span><span class="sxs-lookup"><span data-stu-id="71a8e-121">Scanning or imaging device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**\_impressora vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-122"><span id="vmUSBDeviceClass_Printer"></span><span id="vmusbdeviceclass_printer"></span><span id="VMUSBDEVICECLASS_PRINTER"></span>**vmUSBDeviceClass\_Printer**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-123">Dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="71a8e-123">Printer device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass \_ MassStorage**</span><span class="sxs-lookup"><span data-stu-id="71a8e-124"><span id="vmUSBDeviceClass_MassStorage"></span><span id="vmusbdeviceclass_massstorage"></span><span id="VMUSBDEVICECLASS_MASSSTORAGE"></span>**vmUSBDeviceClass\_MassStorage**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-125">Dispositivo de armazenamento em massa.</span><span class="sxs-lookup"><span data-stu-id="71a8e-125">Mass storage device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**\_Hub vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-126"><span id="vmUSBDeviceClass_Hub"></span><span id="vmusbdeviceclass_hub"></span><span id="VMUSBDEVICECLASS_HUB"></span>**vmUSBDeviceClass\_Hub**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-127">Dispositivo de Hub.</span><span class="sxs-lookup"><span data-stu-id="71a8e-127">Hub device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass \_ CDCData**</span><span class="sxs-lookup"><span data-stu-id="71a8e-128"><span id="vmUSBDeviceClass_CDCData"></span><span id="vmusbdeviceclass_cdcdata"></span><span id="VMUSBDEVICECLASS_CDCDATA"></span>**vmUSBDeviceClass\_CDCData**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-129">Dispositivo de dados CDC.</span><span class="sxs-lookup"><span data-stu-id="71a8e-129">CDC data device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**\_cartão inteligente vmUSBDeviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-130"><span id="vmUSBDeviceClass_SmartCard"></span><span id="vmusbdeviceclass_smartcard"></span><span id="VMUSBDEVICECLASS_SMARTCARD"></span>**vmUSBDeviceClass\_SmartCard**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-131">Dispositivo de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="71a8e-131">Smart card device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass \_ ContentSecurity**</span><span class="sxs-lookup"><span data-stu-id="71a8e-132"><span id="vmUSBDeviceClass_ContentSecurity"></span><span id="vmusbdeviceclass_contentsecurity"></span><span id="VMUSBDEVICECLASS_CONTENTSECURITY"></span>**vmUSBDeviceClass\_ContentSecurity**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-133">Dispositivo de segurança de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="71a8e-133">Content security device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vídeo do vmUSBDeviceClass \_**</span><span class="sxs-lookup"><span data-stu-id="71a8e-134"><span id="vmUSBDeviceClass_Video"></span><span id="vmusbdeviceclass_video"></span><span id="VMUSBDEVICECLASS_VIDEO"></span>**vmUSBDeviceClass\_Video**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-135">Dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="71a8e-135">Video device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass \_ PersonalHealthcare**</span><span class="sxs-lookup"><span data-stu-id="71a8e-136"><span id="vmUSBDeviceClass_PersonalHealthcare"></span><span id="vmusbdeviceclass_personalhealthcare"></span><span id="VMUSBDEVICECLASS_PERSONALHEALTHCARE"></span>**vmUSBDeviceClass\_PersonalHealthcare**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-137">Dispositivo de assistência médica.</span><span class="sxs-lookup"><span data-stu-id="71a8e-137">Health care device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass \_ DiagnosticDevice**</span><span class="sxs-lookup"><span data-stu-id="71a8e-138"><span id="vmUSBDeviceClass_DiagnosticDevice"></span><span id="vmusbdeviceclass_diagnosticdevice"></span><span id="VMUSBDEVICECLASS_DIAGNOSTICDEVICE"></span>**vmUSBDeviceClass\_DiagnosticDevice**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-139">Dispositivo de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="71a8e-139">Diagnostic device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass \_ WirelessController**</span><span class="sxs-lookup"><span data-stu-id="71a8e-140"><span id="vmUSBDeviceClass_WirelessController"></span><span id="vmusbdeviceclass_wirelesscontroller"></span><span id="VMUSBDEVICECLASS_WIRELESSCONTROLLER"></span>**vmUSBDeviceClass\_WirelessController**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-141">Dispositivo sem fio.</span><span class="sxs-lookup"><span data-stu-id="71a8e-141">Wireless device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass \_ diversos**</span><span class="sxs-lookup"><span data-stu-id="71a8e-142"><span id="vmUSBDeviceClass_Miscellaneous"></span><span id="vmusbdeviceclass_miscellaneous"></span><span id="VMUSBDEVICECLASS_MISCELLANEOUS"></span>**vmUSBDeviceClass\_Miscellaneous**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-143">Dispositivo variado.</span><span class="sxs-lookup"><span data-stu-id="71a8e-143">Miscellaneous device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass \_ ApplicationSpecific**</span><span class="sxs-lookup"><span data-stu-id="71a8e-144"><span id="vmUSBDeviceClass_ApplicationSpecific"></span><span id="vmusbdeviceclass_applicationspecific"></span><span id="VMUSBDEVICECLASS_APPLICATIONSPECIFIC"></span>**vmUSBDeviceClass\_ApplicationSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-145">Dispositivo específico do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71a8e-145">Application-specific device.</span></span>

</dd> <dt>

<span data-ttu-id="71a8e-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass \_ VendorSpecific**</span><span class="sxs-lookup"><span data-stu-id="71a8e-146"><span id="vmUSBDeviceClass_VendorSpecific"></span><span id="vmusbdeviceclass_vendorspecific"></span><span id="VMUSBDEVICECLASS_VENDORSPECIFIC"></span>**vmUSBDeviceClass\_VendorSpecific**</span></span>
</dt> <dd>

<span data-ttu-id="71a8e-147">Dispositivo específico do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="71a8e-147">Vendor-specific device.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71a8e-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71a8e-148">Requirements</span></span>



| <span data-ttu-id="71a8e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="71a8e-149">Requirement</span></span> | <span data-ttu-id="71a8e-150">Valor</span><span class="sxs-lookup"><span data-stu-id="71a8e-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="71a8e-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a8e-151">Minimum supported client</span></span><br/> | <span data-ttu-id="71a8e-152">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="71a8e-152">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71a8e-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71a8e-153">Minimum supported server</span></span><br/> | <span data-ttu-id="71a8e-154">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="71a8e-154">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="71a8e-155">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="71a8e-155">End of client support</span></span><br/>    | <span data-ttu-id="71a8e-156">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71a8e-156">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="71a8e-157">Produto</span><span class="sxs-lookup"><span data-stu-id="71a8e-157">Product</span></span><br/>                  | <span data-ttu-id="71a8e-158">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="71a8e-158">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="71a8e-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71a8e-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="71a8e-160"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="71a8e-160"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71a8e-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="71a8e-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71a8e-162">**IVMUSBDevice::D eviceClass**</span><span class="sxs-lookup"><span data-stu-id="71a8e-162">**IVMUSBDevice::DeviceClass**</span></span>](ivmusbdevice-deviceclass.md)
</dt> </dl>

 

