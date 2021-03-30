---
description: Indica se o volume e sua chave de criptografia estão protegidos.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Método GetProtectionStatus da classe Win32_EncryptableVolume
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
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646985"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetProtectionStatus da classe Win32 \_ EncryptableVolume

O método **GetProtectionStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se o volume e sua chave de criptografia (se houver) estão protegidos.

A proteção será desativada se um volume for não criptografado ou parcialmente criptografado, ou se a chave de criptografia do volume estiver disponível em claro no disco rígido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtectionStatus* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Especifica se o volume e a chave de criptografia (se houver) estão protegidos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> Não <dt><strong>protegido</strong></dt> <dt>0</dt> </dl></td>
<td>PROTEÇÃO DESATIVADA<br/> Para um HDD padrão:<br/> O volume é não criptografado, parcialmente criptografado ou a chave de criptografia do volume está disponível em claro no disco rígido. A chave de criptografia estará disponível em claro no disco rígido se os protetores de chave tiverem sido desabilitados usando o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou se nenhum protetor de chave tiver sido especificado usando os seguintes métodos:
<ul>
<li><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></li>
<li><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></li>
<li><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></li>
<li><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></li>
<li><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></li>
<li><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></li>
<li><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></li>
<li><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></li>
<li><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></li>
</ul>
<br/> Para um EHDD:<br/> A banda para o volume é permanente desbloqueada, não tem um Gerenciador de chaves ou é gerenciada por um Gerenciador de chaves de terceiros.<br/> Isso também pode significar que a banda é gerenciada pelo BitLocker, mas o método <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> foi chamado e a unidade está suspensa.<br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <dt><strong>Protegido</strong></dt> <dt>1</dt> </dl></td>
<td>PROTEÇÃO ATIVADA<br/> Para um HDD padrão:<br/> O volume é totalmente criptografado e a chave de criptografia para o volume não está disponível em claro no disco rígido.<br/> Para um EHDD:<br/> O BitLocker é o Gerenciador de chaves da banda. A unidade pode ser bloqueada ou desbloqueada, mas não pode ser desbloqueada perpétuamente.<br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt><strong>Desconhecido</strong></dt> <dt>2</dt> </dl></td>
<td>Não é possível determinar o status de proteção do volume. Isso pode ser causado pelo volume estar em um estado bloqueado.<br/> <strong>Windows Vista Ultimate, Windows Vista Enterprise e Windows Server 2008:</strong> Não há suporte para esse valor. Esse valor tem suporte a partir do Windows 7 e do Windows Server 2008 R2.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
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

Portanto, se o disco for criptografado e *ProtectionStatus* retornar zero (proteção desativada), as chaves serão desabilitadas.

Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) para listar os protetores de chave que foram especificados para proteger a chave de criptografia do volume. Se os protetores de chave existirem, mas a proteção for zero (proteção desativada), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) para ativar a proteção de volume.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]<br/>                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
