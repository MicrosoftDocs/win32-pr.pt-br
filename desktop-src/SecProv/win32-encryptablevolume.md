---
description: Para a criptografia de unidade ou para criar um software de segurança de criptografia, você pode usar o software de criptografia do Windows, Criptografia de Unidade de Disco BitLocker, uma API de criptografia que pode ser usada usando a \_ classe de provedor WMI EncryptableVolume do Win32.
ms.assetid: 464fa664-4330-43fa-a5e0-144d1e73cf58
title: Classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume
- Win32_EncryptableVolume.DeviceID
- Win32_EncryptableVolume.PersistentVolumeID
- Win32_EncryptableVolume.DriveLetter
- Win32_EncryptableVolume.ProtectionStatus
api_type:
- Schema
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b202a536f3c20126c05f072c029fe316f90ce4fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920810"
---
# <a name="win32_encryptablevolume-class"></a>\_Classe Win32 EncryptableVolume

A classe de provedor WMI **\_ EncryptableVolume do Win32** representa uma área de armazenamento em um disco rígido que pode ser protegido usando criptografia de unidade de disco BitLocker. Somente volumes NTFS podem ser criptografados. Pode ser um volume que contém um sistema operacional ou pode ser um volume de dados no disco local. Não pode ser uma unidade de rede.

Para obter os benefícios do BitLocker, você deve especificar um método de proteção para a chave de criptografia do volume e, em seguida, criptografar totalmente o volume.

Para proteger a chave de criptografia do volume, adicione protetores de chave usando estes métodos:

-   [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

Cada tipo de protetor de chave fornece uma experiência de autenticação diferente para desbloquear o acesso aos dados criptografados. Chaves externas e senhas numéricas podem fornecer autenticação durante cenários de recuperação. Para protetores de chave baseados em TPM, você pode primeiro precisar inicializar o TPM corretamente. Para obter mais informações, consulte a classe de provedor WMI do [**\_ TPM do Win32**](win32-tpm.md) .

Use o método [**Encrypt**](encrypt-win32-encryptablevolume.md) ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) para iniciar a criptografia. Os protetores de chave devem ser adicionados antes de iniciar a criptografia ou, caso contrário, você deve usar o método [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) para expor uma chave não protegida. Se o computador desligar enquanto a criptografia estiver em andamento, a criptografia será retomada automaticamente quando o computador for reiniciado.

Você pode usar os métodos [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) e [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) para verificar o status de um volume acessível.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_EncryptableVolume
{
  string DeviceID;
  string PersistentVolumeID;
  string DriveLetter;
  uint32 ProtectionStatus;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ EncryptableVolume** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ EncryptableVolume** tem esses métodos.



| Método                                                                                                                   | Descrição                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BackupRecoveryInformationToActiveDirectory**](backuprecoveryinformationtoactivedirectory-win32-encryptablevolume.md) | Salva todas as chaves externas e informações relacionadas que são necessárias para a recuperação para o Active Directory.<br/>                                                                                                                                                                       |
| [**ChangeExternalKey**](changeexternalkey-win32-encryptablevolume.md)                                                   | Altera a chave externa associada a um volume criptografado.<br/>                                                                                                                                                                                                              |
| [**ChangePassphrase**](changepassphrase-win32-encryptablevolume.md)                                                     | Usa a nova senha para obter uma nova chave derivada.<br/>                                                                                                                                                                                                                       |
| [**ChangePIN**](changepin-win32-encryptablevolume.md)                                                                   | Altera um PIN associado a um volume criptografado.<br/>                                                                                                                                                                                                                         |
| [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md)                                         | Remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usadas para desbloquear automaticamente os volumes de dados.<br/>                                                                                                             |
| [**Descriptografar**](decrypt-win32-encryptablevolume.md)                                                                       | Começa a descriptografia de um volume totalmente criptografado ou retoma a descriptografia de um volume parcialmente criptografado.<br/>                                                                                                                                                                       |
| [**DeleteKeyProtector**](deletekeyprotector-win32-encryptablevolume.md)                                                 | Exclui um determinado protetor de chave para o volume.<br/>                                                                                                                                                                                                                              |
| [**DeleteKeyProtectors**](deletekeyprotectors-win32-encryptablevolume.md)                                               | Exclui todos os protetores de chave do volume.<br/>                                                                                                                                                                                                                                 |
| [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md)                                                   | Remove a chave externa salva no volume do sistema operacional em execução no momento para que o volume não seja desbloqueado automaticamente quando for montado.<br/>                                                                                                                       |
| [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md)                                             | Desabilita todos os protetores de chave associados a este volume.<br/>                                                                                                                                                                                                                   |
| [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)                                                     | Permite que um volume de dados seja desbloqueado automaticamente quando o volume é montado.<br/>                                                                                                                                                                                              |
| [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md)                                               | Habilita todos os protetores de chave desabilitados.<br/>                                                                                                                                                                                                                                       |
| [**Encrypt**](encrypt-win32-encryptablevolume.md)                                                                       | Inicia a criptografia de um volume totalmente descriptografado ou retoma a criptografia de um volume parcialmente criptografado.<br/>                                                                                                                                                                       |
| [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md)                                     | Inicia a criptografia de um volume totalmente descriptografado após um teste de hardware.<br/>                                                                                                                                                                                                       |
| [**FindValidCertificates**](findvalidcertificates-win32-encryptablevolume.md)                                           | Enumera todos os certificados no sistema que correspondem aos critérios indicados e retorna uma lista de impressões digitais.<br/>                                                                                                                                                             |
| [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md)                                               | Indica o status da criptografia ou descriptografia no volume.<br/>                                                                                                                                                                                                        |
| [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md)                                               | Indica o algoritmo de criptografia e o tamanho da chave usados no volume.<br/>                                                                                                                                                                                                        |
| [**GetExternalKeyFileName**](getexternalkeyfilename-win32-encryptablevolume.md)                                         | Retorna o nome do arquivo que contém a chave externa.<br/>                                                                                                                                                                                                               |
| [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md)                                         | Retorna a chave externa de um arquivo.<br/>                                                                                                                                                                                                                                      |
| [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md)                                           | Retorna informações de status em um teste de hardware.<br/>                                                                                                                                                                                                                             |
| [**Getidentificafield**](getidentificationfield-win32-encryptablevolume.md)                                         | Retorna a cadeia de caracteres do identificador que está disponível nos metadados do volume.<br/>                                                                                                                                                                                                  |
| [**GetKeyPackage**](getkeypackage-win32-encryptablevolume.md)                                                           | Retorna informações que tornam o help Salvage dados criptografados quando a unidade está seriamente danificada.<br/>                                                                                                                                                                              |
| [**GetKeyProtectorCertificate**](getkeyprotectorcertificate-win32-encryptablevolume.md)                                 | Recupera a chave pública e a impressão digital do certificado para um protetor de chave pública.<br/>                                                                                                                                                                                            |
| [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md)                                 | Recupera a chave externa para um determinado protetor de chave do tipo apropriado.<br/>                                                                                                                                                                                              |
| [**GetKeyProtectorFriendlyName**](getkeyprotectorfriendlyname-win32-encryptablevolume.md)                               | Recupera o nome de exibição usado para identificar um protetor de chave específico.<br/>                                                                                                                                                                                                         |
| [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md)                     | Recupera a senha numérica de um determinado protetor de chave do tipo apropriado.<br/>                                                                                                                                                                                        |
| [**GetKeyProtectorPlatformValidationProfile**](getkeyprotectorplatformvalidationprofile-win32-encryptablevolume.md)     | Recupera o perfil de validação de plataforma para um protetor de chave específico do tipo apropriado.<br/>                                                                                                                                                                               |
| [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md)                                                     | Lista os protetores usados para proteger a chave de criptografia do volume.<br/>                                                                                                                                                                                                           |
| [**GetKeyProtectorType**](getkeyprotectortype-win32-encryptablevolume.md)                                               | Indica o tipo de um protetor de chave fornecido.<br/>                                                                                                                                                                                                                               |
| [**GetLockStatus**](getlockstatus-win32-encryptablevolume.md)                                                           | Indica se o conteúdo do volume pode ser acessado do sistema operacional em execução no momento.<br/>                                                                                                                                                                   |
| [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md)                                               | Indica se o volume e sua chave de criptografia (se houver) estão protegidos.<br/>                                                                                                                                                                                                  |
| [**Obter versão**](getversion-win32-encryptablevolume.md)                                                                 | Indica a versão de metadados FVE do volume.<br/>                                                                                                                                                                                                                          |
| [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md)                                               | Indica se o volume é desbloqueado automaticamente quando montado.<br/>                                                                                                                                                                                                       |
| [**IsAutoUnlockKeyStored**](isautounlockkeystored-win32-encryptablevolume.md)                                           | Indica se existe no volume do sistema operacional em execução no momento todas as chaves externas e as informações relacionadas que podem ser usadas para desbloquear automaticamente os volumes de dados.<br/>                                                                                           |
| [**IsKeyProtectorAvailable**](iskeyprotectoravailable-win32-encryptablevolume.md)                                       | Indica se os protetores estão disponíveis para o volume.<br/>                                                                                                                                                                                                                 |
| [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md)                                     | Indica se a senha numérica atende aos requisitos especiais de formato.<br/>                                                                                                                                                                                            |
| [**Bloquear**](lock-win32-encryptablevolume.md)                                                                             | Desmonta o volume e remove a chave de criptografia do volume da memória do sistema.<br/>                                                                                                                                                                                           |
| [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)                                                       | Pausa a criptografia ou descriptografia de um volume.<br/>                                                                                                                                                                                                                           |
| [**PrepareVolume**](preparevolume-win32-encryptablevolume.md)                                                           | Cria um volume do BitLocker com o tipo de sistema de arquivos especificado do volume de descoberta.<br/>                                                                                                                                                                                    |
| [**ProtectKeyWithCertificateFile**](protectkeywithcertificatefile-win32-encryptablevolume.md)                           | Valida o OID (identificador de objeto) de uso avançado de chave (EKU) do arquivo de certificado fornecido.<br/>                                                                                                                                                                           |
| [**ProtectKeyWithCertificateThumbprint**](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)               | Valida o OID (identificador de objeto) de uso avançado de chave (EKU) da impressão digital do certificado fornecido.<br/>                                                                                                                                                                     |
| [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md)                                   | Protege a chave de criptografia do volume com uma chave externa de 256 bits.<br/>                                                                                                                                                                                                           |
| [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md)                       | Protege a chave de criptografia do volume com uma senha de 48 dígitos formatada especialmente.<br/>                                                                                                                                                                                          |
| [**ProtectKeyWithPassphrase**](protectkeywithpassphrase-win32-encryptablevolume.md)                                     | Usa a frase secreta para obter a chave derivada.<br/>                                                                                                                                                                                                                             |
| [**ProtectKeyWithTPM**](protectkeywithtpm-win32-encryptablevolume.md)                                                   | Protege a chave de criptografia do volume usando o hardware de segurança do Trusted Platform Module (TPM) no computador, se disponível.<br/>                                                                                                                                            |
| [**ProtectKeyWithTPMAndPIN**](protectkeywithtpmandpin-win32-encryptablevolume.md)                                       | Protege a chave de criptografia do volume usando o hardware de segurança do Trusted Platform Module (TPM) no computador, se disponível, aprimorado por um PIN (número de identificação pessoal) especificado pelo usuário que deve ser fornecido ao computador na inicialização.<br/>                        |
| [**ProtectKeyWithTPMAndPINAndStartupKey**](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)             | Protege a chave de criptografia do volume usando o hardware de segurança do Trusted Platform Module (TPM) no computador, se disponível, aprimorado por um PIN (número de identificação pessoal) especificado pelo usuário e por uma chave externa que deve ser fornecida ao computador na inicialização.<br/> |
| [**ProtectKeyWithTPMAndStartupKey**](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)                         | Protege a chave de criptografia do volume usando o hardware de segurança do Trusted Platform Module (TPM) no computador, se disponível, aprimorado por uma chave externa que deve ser fornecida ao computador na inicialização.<br/>                                                              |
| [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md)                                                     | Retoma a criptografia ou descriptografia de um volume.<br/>                                                                                                                                                                                                                          |
| [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)                                           | Grava a chave externa associada ao protetor de chave de volume especificado em um local de arquivo especificado.<br/>                                                                                                                                                                   |
| [**Setidentificafield**](setidentificationfield-win32-encryptablevolume.md)                                         | Define a cadeia de caracteres do identificador especificado nos metadados do volume.<br/>                                                                                                                                                                                                             |
| [**UnlockWithCertificateFile**](unlockwithcertificatefile-win32-encryptablevolume.md)                                   | Usa o arquivo de certificado fornecido para obter a chave derivada e desbloquear o volume criptografado.<br/>                                                                                                                                                                              |
| [**UnlockWithCertificateThumbprint**](unlockwithcertificatethumbprint-win32-encryptablevolume.md)                       | Usa a impressão digital do certificado fornecida para obter a chave derivada e desbloquear o volume criptografado.<br/>                                                                                                                                                                        |
| [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md)                                           | Usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.<br/>                                                                                                                                                                                                      |
| [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md)                               | Usa uma senha numérica fornecida para acessar o conteúdo de um volume de dados.<br/>                                                                                                                                                                                                |
| [**UnlockWithPassphrase**](unlockwithpassphrase-win32-encryptablevolume.md)                                             | Usa a frase secreta para obter a chave derivada. Depois que a chave derivada é calculada, a chave derivada é usada para desbloquear a chave mestra do volume criptografado.<br/>                                                                                                                   |
| [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md)                                                           | Atualiza um volume do formato do Windows Vista para o formato do Windows 7.<br/>                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ EncryptableVolume** tem essas propriedades.

<dl> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Um identificador exclusivo para o volume neste sistema. Use isso para associar um volume a outras classes de provedor de WMI, por exemplo, o **\_ volume Win32**.

</dd> <dt>

**DriveLetter**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A letra da unidade do volume. Esse identificador pode ser usado para associar um volume com outras classes de provedor WMI, por exemplo, o [**\_ volume Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85)).

Para volumes sem letras de unidade, esse valor é **NULL**.

</dd> <dt>

**PersistentVolumeID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um identificador persistente para o volume neste sistema. Esse identificador é exclusivo para **Win32 \_ EncryptableVolume**.

Esse identificador é uma cadeia de caracteres vazia se o volume for um volume NTFS padrão totalmente descriptografado; caso contrário, ele tem um valor exclusivo.

</dd> <dt>

**ProtectionStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O status do volume, se o BitLocker está ou não protegendo o volume. Esse valor é armazenado quando a classe é instanciada. É possível que o status da proteção mude o estado entre a instanciação e quando você verificar o valor. Para verificar o valor da propriedade **ProtectionStatus** em tempo real, use o método [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .



| Valor                                                                        | Significado                                                                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | PROTEÇÃO DESATIVADA<br/> O volume não é criptografado, parcialmente criptografado ou a chave de criptografia do volume para o volume está disponível no limpar no disco rígido. <br/> |
| <dl> <dt>1</dt> </dl> | PROTEÇÃO ATIVADA<br/> O volume é totalmente criptografado e a chave de criptografia para o volume não está disponível em claro no disco rígido. <br/>                          |
| <dl> <dt>2</dt> </dl> | PROTEÇÃO DESCONHECIDA<br/> Não é possível determinar o status de proteção do volume. Uma causa potencial é que o volume está em um estado bloqueado.<br/>                          |



 

</dd> </dl>

## <a name="security-considerations"></a>Considerações de segurança

A classe de provedor WMI **\_ EncryptableVolume do Win32** depende da segurança do namespace do WMI e do subsistema criptografia de unidade de disco BitLocker para controle de acesso.

Para usar os **métodos \_ EncryptableVolume do Win32** , as seguintes condições devem ser atendidas:

-   Você deve ter privilégios de administrador.
-   A criptografia de conexão deve ser capaz de se conectar ao provedor.

    Para obter mais informações sobre como criar uma conexão criptografada, consulte [exigindo uma conexão criptografada para um namespace](../wmisdk/requiring-an-encrypted-connection-to-a-namespace.md).

Para habilitar conexões remotas, o tráfego WMI remoto deve ser permitido. Para obter mais informações sobre como habilitar o tráfego WMI, consulte [conectando-se ao WMI remotamente a partir do vista](../wmisdk/connecting-to-wmi-remotely-starting-with-vista.md).

A configuração de segurança de namespace padrão inclui uma entrada para permitir a edição por padrão. Para obter mais informações sobre a auditoria de namespace do WMI, consulte [acesso aos namespaces do WMI](../wmisdk/access-to-wmi-namespaces.md).

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]<br/>                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



 

 
