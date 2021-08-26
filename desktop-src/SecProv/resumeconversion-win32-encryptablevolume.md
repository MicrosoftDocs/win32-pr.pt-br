---
description: Retoma a criptografia ou descriptografia de um volume.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Método ResumeConversion da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e1b3908f77b72f7f9a5ca0583193784ba054a50ab59aa63dad1c13b9f03317e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992666"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a>Método ResumeConversion da classe Win32 \_ EncryptableVolume

O método **ResumeConversion** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retoma a criptografia ou descriptografia de um volume.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função poderá retomar apenas uma operação de apagamento. Para obter mais informações, consulte [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se esse método for usado em um volume totalmente criptografado ou totalmente descriptografado, ou se a criptografia/descriptografia já estiver em andamento no volume, 0 será retornado supondo que nenhum outro erro ocorra.



| Código/valor de retorno                                                                                                                                                                  | Descrição                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>      |



 

## <a name="remarks"></a>Comentários

Se esse método for usado em um volume com criptografia/descriptografia em pausa, a execução bem-sucedida desse método fará com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a criptografia ou descriptografia está em andamento.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Enterprise, \[ somente aplicativos de área de trabalho do vista Ultimate Windows\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
