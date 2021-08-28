---
description: Indica se o volume e sua chave de criptografia estão protegidos.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Método GetProtectionStatus da Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 66fcbcfc4c5f228fde786a6b9d8913cc69c0d341
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471502"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetProtectionStatus da classe EncryptableVolume do Win32 \_

O **método GetProtectionStatus** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) indica se o volume e sua chave de criptografia (se alguma) estão protegidos.

A proteção será desligada se um volume não estiver criptografado ou parcialmente criptografado ou se a chave de criptografia do volume estiver disponível de forma não criptografada no disco rígido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtectionStatus* \[ out\]
</dt> <dd>

Tipo: **uint32**

Especifica se o volume e a chave de criptografia (se alguma) estão protegidos.




| Valor | Significado | 
|-------|---------|
| <span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl><dt><strong>Desprotegido</strong></dt><dt>0</dt></dl> | PROTEÇÃO DESLIGADA<br /> Para um HDD padrão:<br /> O volume está descriptografado, parcialmente criptografado ou a chave de criptografia do volume está disponível de forma não criptografada no disco rígido. A chave de criptografia estará disponível de forma clara no disco rígido se os protetores de chave foram desabilitados usando o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou se nenhum protetor de chave tiver sido especificado usando os seguintes métodos:<ul><li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li><li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li><li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li><li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li><li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li><li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li><li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li><li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li><li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li></ul><br /> Para um EHDD:<br /> A banda do volume é desbloqueada permanentemente, não tem nenhum gerenciador de chaves ou é gerenciada por um gerenciador de chaves de terceiros.<br /> Isso também pode significar que a banda é gerenciada pelo BitLocker, mas o <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>método DisableKeyProtectors</strong></a> foi chamado e a unidade está suspensa.<br /> | 
| <span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl><dt><strong>Protegido</strong></dt><dt>1</dt></dl> | PROTEÇÃO EM<br /> Para um HDD padrão:<br /> O volume é totalmente criptografado e a chave de criptografia para o volume não está disponível de forma clara no disco rígido.<br /> Para um EHDD:<br /> O BitLocker é o gerenciador de chaves para a banda. A unidade pode ser bloqueada ou desbloqueada, mas não pode ser desbloqueada permanentemente.<br /> | 
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl><dt><strong>Desconhecido</strong></dt><dt>2</dt></dl> | O status de proteção de volume não pode ser determinado. Isso pode ser causado pelo volume estar em um estado bloqueado.<br /><strong>Windows Vista Ultimate, Windows Vista Enterprise e Windows Server 2008:</strong> Não há suporte para esse valor. Esse valor tem suporte a partir do Windows 7 e Windows Server 2008 R2.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Você só poderá criptografar um volume se chamar [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) primeiro ou usar um dos seguintes métodos:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Portanto, se o disco for criptografado e *ProtectionStatus* retornar zero (PROTECTION OFF), as chaves serão desabilitadas.

Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) para listar os protetores de chave que foram especificados para proteger a chave de criptografia do volume. Se existirem protetores de chave, mas a proteção for zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) para ativar a proteção por volume.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Windows SDK. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows aplicativos de área de trabalho do Vista Ultimate \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
