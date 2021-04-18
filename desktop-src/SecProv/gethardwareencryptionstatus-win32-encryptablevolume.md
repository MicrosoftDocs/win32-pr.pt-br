---
description: Determina se o volume está localizado em uma unidade que dá suporte ou pode dar suporte à criptografia de hardware.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Método GetHardwareEncryptionStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796358"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetHardwareEncryptionStatus da classe Win32 \_ EncryptableVolume

O método **GetHardwareEncryptionStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) determina se o volume está localizado em uma unidade que dá suporte ou pode dar suporte à criptografia de hardware.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HardwareEncryptionStatus* \[ fora\]
</dt> <dd>

Especifica se a unidade pode dar suporte à criptografia de hardware. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                               | Significado                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <dt>**Sem suporte**</dt> <dt>0</dt> </dl> | Não há suporte para criptografia de hardware.<br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <dt>**Sem proteção**</dt> <dt>1</dt> </dl> | Não há suporte para a criptografia de unidade.<br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <dt>**Usa software**</dt> <dt>2</dt> </dl> | O método de criptografia é baseado em software.<br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <dt>**Usa hardware**</dt> <dt>3</dt> </dl> | A unidade dá suporte à criptografia de hardware.<br/>  |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará zero (0) se o volume for compatível com a criptografia de hardware do BitLocker. Caso contrário, a função retornará um erro.



| Código/valor de retorno                                                                                                                                 | Descrição                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O volume é compatível com a criptografia de hardware do BitLocker.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




