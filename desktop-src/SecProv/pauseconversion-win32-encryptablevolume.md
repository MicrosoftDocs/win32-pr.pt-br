---
description: Pausa a criptografia ou descriptografia de um volume.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Método PauseConversion da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7612f7f587d13bb1dbe5fc96d29117d126b3a7166e0172abe98a0777d815effa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004444"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a>Método PauseConversion da classe Win32 \_ EncryptableVolume

O método **PauseConversion** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) pausa a criptografia ou descriptografia de um volume.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função poderá pausar uma operação de apagamento, mas não poderá pausar a criptografia baseada em hardware.

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se esse método for usado em um volume totalmente criptografado ou totalmente descriptografado, ou se a criptografia/descriptografia já estiver em pausa no volume, 0 será retornado supondo que nenhum outro erro ocorra.



| Código/valor de retorno                                                                                                                                                                  | Descrição                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/> |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>      |



 

## <a name="remarks"></a>Comentários

Se esse método for usado em um volume com criptografia/descriptografia em andamento, a execução bem-sucedida desse método fará com que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que a criptografia ou descriptografia está em pausa.

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

 

 
