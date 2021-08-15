---
description: Tenta provisionar o TPM para um estado completamente pronto e assumirá a propriedade do TPM, se ele ainda não tiver sido possuído.
ms.assetid: D0C09A48-00D0-4BF2-8F0A-451A61EA7810
title: Win32_Tpm::P método rovision
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Provision
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5153672d91c88597676f65b53a93de6ffac9f4989dd9e231c87a3b7947b1d657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890804"
---
# <a name="win32_tpmprovision-method"></a>TPM do Win32 \_ : método de:P rovision

Tenta provisionar o TPM para um estado completamente pronto e assumirá a propriedade do TPM, se ele ainda não tiver sido possuído. Esse método é caro para ser executado porque ele executa muitas verificações. É recomendável que os aplicativos usem esse método somente quando necessário.

Esse método só pode ser acessado por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 Provision(
  [in]  BOOL   ForceClear_Allowed,
  [in]  BOOL   PhysicalPresencePrompts_Allowed,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ForceClear \_ Permitido* \[ em\]
</dt> <dd>

Quando definido como **true** , o método pode solicitar operações de presença física para limpar o TPM. Se definido como **false**, o método não solicitará uma operação de presença física para limpar o TPM.

</dd> <dt>

*PhysicalPresencePrompts \_ Permitido* \[ em\]
</dt> <dd>

Quando definido como **true** , o método pode solicitar operações de presença física que exigem o envolvimento do usuário durante o processo de inicialização para confirmar a alteração do estado do TPM.

</dd> <dt>

*Informações* \[ do fora\]
</dt> <dd>

Retorna uma bitmask de tanta informação quanto está disponível para o que é necessário para provisionar totalmente o TPM. Valores de máscara como informações \_ de reinicialização indicam que a chamada de método deve iniciar uma reinicialização para mover o processo de provisionamento para encaminhamentos.

O parâmetro *Information* pode consistir nos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**Informações \_ do DESLIGAR**</dt> <dt>0x00000002</dt> </dl>                                                 | A reinicialização da plataforma é necessária (desligada).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**Informações \_ do Reinicializar**</dt> <dt>0x00000004</dt> </dl>                                                       | A reinicialização da plataforma é necessária (reinicialização).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**Informações \_ do 0x00000008 de força do TPM- \_ \_ limpar**</dt> <dt></dt> </dl>                          | O TPM já é de propriedade. O TPM precisa ser limpo ou o valor de autorização do proprietário do TPM precisa ser importado.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**Informações \_ do \_Presença física**</dt> <dt>0x00000010</dt> </dl>                     | A presença física é necessária para provisionar o TPM.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**Informações \_ do \_Ativação do TPM**</dt> <dt>0x00000020</dt> </dl>                                    | O TPM está desabilitado ou desativado.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**Informações \_ do 0x00000040 \_ de \_ apropriação do TPM**</dt> <dt></dt> </dl>                 | A propriedade do TPM foi tirada.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**Informações \_ do \_ \_ Criar**</dt> <dt>0X00000080</dt> de endosso de TPM </dl>                                | Existe uma chave de endosso (EK) no TPM. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**Informações \_ do 0x00000100 \_ OWNERAUTH TPM**</dt> <dt></dt> </dl>                                 | A autorização do proprietário do TPM não está armazenada corretamente no registro.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**Informações \_ do 0x000000200 \_ de \_ autenticação SRK do TPM**</dt> <dt></dt> </dl>                                  | o valor de autorização da chave raiz de Armazenamento (SRK) não é todos os zeros.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**Informações \_ do \_Desabilitar proprietário do TPM \_ \_ limpar**</dt> <dt>0x00000400</dt> </dl> | Se o sistema operacional estiver configurado para desabilitar a limpeza do TPM com o valor de autorização do proprietário do TPM e o TPM ainda não tiver sido configurado para impedir a limpeza do TPM com o valor de autorização do proprietário do TPM.<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**Informações \_ do 0x00000800 \_ SRKPUB TPM**</dt> <dt></dt> </dl>                                          | as informações de registro do sistema operacional sobre a chave raiz Armazenamento do tpm não correspondem à chave raiz Armazenamento do tpm.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**Informações \_ do 0x00001000 \_ \_ SRKPUB leitura do TPM**</dt> <dt></dt> </dl>                          | o sinalizador permanente do TPM para permitir a leitura do valor público da chave raiz de Armazenamento não está definido.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**Informações \_ do \_ \_ Contador de inicialização do TPM**</dt> <dt>0x00002000</dt> </dl>                       | O contador monotônico incrementado durante a inicialização não foi criado.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**Informações \_ do 0x00004000 \_ de \_ backup do AD TPM**</dt> <dt></dt> </dl>                                | Não foi feito backup da autorização do proprietário do TPM para Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**Informações \_ do Fase de backup do AD do TPM \_ \_ \_ \_ I**</dt> <dt>0x00008000</dt> </dl>      | A primeira parte do armazenamento de informações de autorização do proprietário do TPM no Active Directory está em andamento.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**Informações \_ do \_ \_ \_ Fase \_ II do backup do AD do TPM**</dt> <dt>0x00010000</dt> </dl>   | A segunda parte do armazenamento de informações de autorização do proprietário do TPM no Active Directory está em andamento.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**Informações \_ do 0x00020000 de \_ configuração herdada**</dt> <dt></dt> </dl>            | Windows Política de Grupo está configurado para não armazenar nenhuma autorização de proprietário do TPM para que o TPM não possa estar totalmente pronto.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**Informações \_ do \_Certificado de EK**</dt> <dt>0x00040000</dt> </dl>                              | O certificado EK não foi lido na RAM NV do TPM e está armazenado no registro. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**Informações \_ do 0x00080000 \_ do \_ log de eventos do TCG**</dt> <dt></dt> </dl>                                | O log de eventos do TCG está vazio ou não pode ser lido. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**Informações \_ do 0x00100000 não \_ reduzido**</dt> <dt></dt> </dl>                                       | O TPM não é proprietário.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**Informações \_ do \_Erro genérico**</dt> <dt>0x00200000</dt> </dl>                                 | Ocorreu um erro, mas não específico de uma tarefa específica.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**Informações \_ do 0x00400000 \_ do \_ contador de bloqueio de dispositivo**</dt> <dt></dt> </dl>              | O contador de bloqueios de dispositivo não foi criado.<br/>                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
