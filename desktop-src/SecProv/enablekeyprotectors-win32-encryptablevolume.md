---
description: Habilita ou retoma todos os protetores de chave desabilitados ou suspensos.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Método EnableKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d90e37f800a9c224abefb21253f7e74c2bc08401
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474922"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método EnableKeyProtectors da classe Win32 \_ EncryptableVolume

O método **EnableKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) habilita ou retoma todos os protetores de chave desabilitados ou suspensos. Você pode usar esse método para habilitar novamente ou retomar a proteção BitLocker em um volume criptografado. Esse método garante que a chave de criptografia do volume não seja exposta na limpeza no disco rígido.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, o estado de banda passará para "desbloqueado" de "Always undeled".

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se os protetores de chave já estiverem habilitados e nenhum outro erro ocorrer, esse método retornará zero.




| Código/valor de retorno | Descrição | 
|-------------------|-------------|
| <dl><dt><strong>S_OK</strong></dt><dt>0 (0x0)</dt></dl> | O método foi bem-sucedido.<br /> | 
| <dl><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt><dt>2150694919 (0x80310007)</dt></dl> | Não existem protetores de chave no volume. Use um dos seguintes métodos para especificar protetores de chave para o volume:<br /><ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul> | 
| <dl><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt><dt>2150694920 (0x80310008)</dt></dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br /> | 




 

## <a name="remarks"></a>Comentários

Se o volume estiver totalmente criptografado, a execução bem-sucedida desse método garantirá que o volume esteja protegido. Se o volume for parcialmente criptografado, a execução bem-sucedida desse método implicará que o volume será protegido quando ele se tornar totalmente criptografado. Para obter mais informações, consulte o método [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .

Se existirem protetores de chave baseados em TPM para o volume, a execução bem-sucedida desse método também atualizará esses protetores para que o TPM seja validado em relação aos serviços de inicialização atuais na plataforma. Em outras palavras, você está afirmando que o estado atual do computador é o estado correto no qual o TPM fará a verificação em caso de reinicializações futuras do computador.

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
</dt> <dt>

[**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
