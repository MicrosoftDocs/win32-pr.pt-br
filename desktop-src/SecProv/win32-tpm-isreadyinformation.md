---
description: Indica se o TPM está pronto e fornece informações adicionais sobre o estado do TPM.
ms.assetid: 1E348D77-979C-42FC-824D-7C57F7BAABE5
title: Win32_Tpm::Método IsReadyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReadyInformation
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 319152da3604044500c107520cf1afd1d04e16fc2c7f54f0ecebf7b49d81f0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890831"
---
# <a name="win32_tpmisreadyinformation-method"></a>Método Win32 \_ Tpm::IsReadyInformation

Indica se o TPM está pronto e fornece informações adicionais sobre o estado do TPM. O parâmetro information retorna um bitmask de informações do que é necessário para provisionar totalmente o TPM.

Esse método só é acessível por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 IsReadyInformation(
  [out] BOOL   IsReady,
  [out] uint32 Information
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsReady* \[ out\]
</dt> <dd>

Definido como **TRUE** se o TPM e o sistema são totalmente provisionados para uso do TPM.

</dd> <dt>

*Informações* \[ out\]
</dt> <dd>

Retorna um bitmask com o máximo de informações disponíveis do que é necessário para provisionar totalmente o TPM.

O *parâmetro* Information pode consistir nos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INFORMATION_SHUTDOWN"></span><span id="information_shutdown"></span><dl> <dt>**INFORMAÇÕES \_ DESLIGAMENTO**</dt> <dt>0x00000002</dt> </dl>                                                 | A reinicialização da plataforma é necessária (desligamento).<br/>                                                                                                                                                                                    |
| <span id="INFORMATION_REBOOT"></span><span id="information_reboot"></span><dl> <dt>**INFORMAÇÕES \_ REINICIALIZAR**</dt> <dt>0x00000004</dt> </dl>                                                       | A reinicialização da plataforma é necessária (reinicialização).<br/>                                                                                                                                                                                      |
| <span id="INFORMATION_TPM_FORCE_CLEAR"></span><span id="information_tpm_force_clear"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ FORCE \_ CLEAR**</dt> <dt>0x00000008</dt> </dl>                          | O TPM já é de propriedade. O TPM precisa ser limpo ou o valor de autorização do proprietário do TPM precisa ser importado.<br/>                                                                                                     |
| <span id="INFORMATION_PHYSICAL_PRESENCE"></span><span id="information_physical_presence"></span><dl> <dt>**INFORMAÇÕES \_ PRESENÇA \_ FÍSICA**</dt> <dt>0X00000010</dt> </dl>                     | A presença física é necessária para provisionar o TPM.<br/>                                                                                                                                                                         |
| <span id="INFORMATION_TPM_ACTIVATE"></span><span id="information_tpm_activate"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ ACTIVATE**</dt> <dt>0x00000020</dt> </dl>                                    | O TPM está desabilitado ou desativado.<br/>                                                                                                                                                                                         |
| <span id="INFORMATION_TPM_TAKE_OWNERSHIP"></span><span id="information_tpm_take_ownership"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ TAKE \_ OWNERSHIP**</dt> <dt>0X00000040</dt> </dl>                 | A propriedade do TPM foi tomada.<br/>                                                                                                                                                                                                |
| <span id="INFORMATION_TPM_CREATE_EK"></span><span id="information_tpm_create_ek"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ CREATE \_ EK**</dt> <dt>0x00000080</dt> </dl>                                | Existe uma chave de endosso (EK) no TPM. <br/>                                                                                                                                                                                 |
| <span id="INFORMATION_TPM_OWNERAUTH"></span><span id="information_tpm_ownerauth"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ OWNERAUTH**</dt> <dt>0x00000100</dt> </dl>                                 | A autorização do proprietário do TPM não está armazenada corretamente no Registro.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_SRK_AUTH"></span><span id="information_tpm_srk_auth"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ SRK \_ AUTH**</dt> <dt>0x00000200</dt> </dl>                                  | O Armazenamento de autorização da chave raiz (SRK) não é todos zeros.<br/>                                                                                                                                                            |
| <span id="INFORMATION_TPM_DISABLE_OWNER_CLEAR"></span><span id="information_tpm_disable_owner_clear"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ DISABLE OWNER CLEAR \_ \_ 0X00000400**</dt> <dt></dt> </dl> | Se o sistema operacional estiver configurado para desabilitar a limpeza do TPM com o valor de autorização do proprietário do TPM e o TPM ainda não tiver sido configurado para impedir a limpeza do TPM com o valor de autorização do proprietário do TPM .<br/> |
| <span id="INFORMATION_TPM_SRKPUB"></span><span id="information_tpm_srkpub"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ SRKPUB**</dt> <dt>0x00000800</dt> </dl>                                          | As informações do registro do sistema operacional sobre a chave Armazenamento raiz do TPM não corresponderão à chave Armazenamento raiz TPM.<br/>                                                                                                       |
| <span id="INFORMATION_TPM_READ_SRKPUB"></span><span id="information_tpm_read_srkpub"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ READ \_ SRKPUB**</dt> <dt>0x00001000</dt> </dl>                          | O sinalizador permanente do TPM para permitir a leitura Armazenamento valor público da Chave Raiz não está definido.<br/>                                                                                                                                    |
| <span id="INFORMATION_TPM_BOOT_COUNTER"></span><span id="information_tpm_boot_counter"></span><dl> <dt>**INFORMAÇÕES \_ CONTADORES DE \_ \_ INICIALIZAÇÃO**</dt> do TPM <dt>0x00002000</dt> </dl>                       | O contador monotônico incrementado durante a inicialização não foi criado.<br/>                                                                                                                                                         |
| <span id="INFORMATION_TPM_AD_BACKUP"></span><span id="information_tpm_ad_backup"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ AD \_ BACKUP**</dt> <dt>0x00004000</dt> </dl>                                | Não foi feito backup da autorização do proprietário do TPM no Active Directory.<br/>                                                                                                                                                   |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_I"></span><span id="information_tpm_ad_backup_phase_i"></span><dl> <dt>**INFORMAÇÕES \_ FASE DE BACKUP DO AD DO TPM \_ \_ \_ \_ 0X00008000**</dt> <dt></dt> </dl>      | A primeira parte do armazenamento de informações de autorização do proprietário do TPM no Active Directory está em andamento.<br/>                                                                                                                    |
| <span id="INFORMATION_TPM_AD_BACKUP_PHASE_II"></span><span id="information_tpm_ad_backup_phase_ii"></span><dl> <dt>**INFORMAÇÕES \_ TPM \_ AD \_ BACKUP FASE \_ \_ II**</dt> <dt>0x00010000</dt> </dl>   | A segunda parte do armazenamento de informações de autorização do proprietário do TPM no Active Directory está em andamento.<br/>                                                                                                                   |
| <span id="INFORMATION_LEGACY_CONFIGURATION"></span><span id="information_legacy_configuration"></span><dl> <dt>**INFORMAÇÕES \_ CONFIGURAÇÃO \_ HERDDA**</dt> <dt>0X00020000</dt> </dl>            | Windows Política de Grupo está configurado para não armazenar nenhuma autorização de proprietário do TPM para que o TPM não possa estar totalmente pronto.<br/>                                                                                                               |
| <span id="INFORMATION_EK_CERTIFICATE"></span><span id="information_ek_certificate"></span><dl> <dt>**INFORMAÇÕES \_ Certificado \_ EK**</dt> <dt>0x00040000</dt> </dl>                              | O Certificado EK não foi lido da ram NV do TPM e armazenado no Registro. <br/>                                                                                                                                            |
| <span id="INFORMATION_TCG_EVENT_LOG"></span><span id="information_tcg_event_log"></span><dl> <dt>**INFORMAÇÕES \_ Log de EVENTOS \_ \_ TCG**</dt> <dt>0x00080000</dt> </dl>                                | O log de eventos do TCG está vazio ou não pode ser lido. <br/>                                                                                                                                                                              |
| <span id="INFORMATION_NOT_REDUCED"></span><span id="information_not_reduced"></span><dl> <dt>**INFORMAÇÕES \_ NOT \_ REDUCED**</dt> <dt>0X00100000</dt> </dl>                                       | O TPM não é de propriedade.<br/>                                                                                                                                                                                                       |
| <span id="INFORMATION_GENERIC_ERROR"></span><span id="information_generic_error"></span><dl> <dt>**INFORMAÇÕES \_ ERRO \_ GENÉRICO**</dt> <dt>0X00200000</dt> </dl>                                 | Ocorreu um erro, mas não específico para uma tarefa específica.<br/>                                                                                                                                                                   |
| <span id="INFORMATION_DEVICE_LOCK_COUNTER"></span><span id="information_device_lock_counter"></span><dl> <dt>**INFORMAÇÕES \_ CONTADORES \_ DE BLOQUEIO \_ DO**</dt> <dt>DISPOSITIVO 0X00400000</dt> </dl>              | O contador de bloqueio do dispositivo não foi criado.<br/>                                                                                                                                                                               |
| <span id="INFORMATION_DEVICEID"></span><span id="information_deviceid"></span><dl> <dt>**INFORMAÇÕES \_ DEVICEID**</dt> <dt> 0x00800000</dt> </dl>                                                | O identificador do dispositivo não foi criado.<br/>                                                                                                                                                                                 |
| <span id="INFORMATION_ATTESTATION_VULNERABILITY"></span><span id="information_attestation_vulnerability"></span><dl> <dt>**INFORMAÇÕES \_ ATTESTATION \_ VULNERABILITY**</dt> <dt> 0X01000000</dt> </dl>                                                | O TPM tem uma vulnerabilidade relacionada ao Atestado de Saúde.<br/>                                                                                                                                                                                 |


 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Todos os erros do TPM, bem como erros específicos dos [Serviços Base do TPM,](../tbs/tbs-return-codes.md) podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Valor/código de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
