---
description: Recupera o perfil de validação de plataforma para um protetor de chave específico do tipo apropriado.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Método GetKeyProtectorPlatformValidationProfile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760192"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorPlatformValidationProfile da classe Win32 \_ EncryptableVolume

O método **GetKeyProtectorPlatformValidationProfile** recupera o perfil de validação de plataforma para um determinado protetor de chave do tipo apropriado.

O identificador de protetor de chave deve se referir a um protetor de chave do tipo "TPM", "TPM e PIN", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*PlatformValidationProfile* \[ fora\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de inteiros que especifica como o hardware de segurança do Trusted Platform Module (TPM) do computador protege a chave de criptografia do volume do disco.



| Valor                                                                         | Significado                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Principal raiz de CRTM (relação de confiança de medida), BIOS e extensões de plataforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configuração e dados da plataforma e da placa-mãe<br/>                         |
| <dl> <dt>2</dt> </dl>  | Código da ROM de opção<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configuração de ROM de opção e dados<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Código de registro mestre de inicialização (MBR)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabela de partição MBR (registro mestre de inicialização)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Transição de estado e eventos de ativação<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Manufacturer-Specific do computador<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Setor de inicialização NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Bloco de inicialização NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Gerenciador de inicialização<br/>                                                            |
| <dl> <dt>11</dt> </dl> | Controle de acesso do BitLocker<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>13</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>14</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>15</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>16</dt> </dl> | Usado para depuração<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinâmico<br/>                                                            |
| <dl> <dt>anos</dt> </dl> | Definido pela plataforma<br/>                                                        |
| <dl> <dt>aprimora</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>Abril</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>23</dt> </dl> | Suporte a aplicativos<br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                  | Descrição                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "TPM", "TPM e PIN", "TPM e PIN e chave de inicialização", ou "TPM e chave de inicialização".<br/> |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker.<br/>                                                                                  |



 

## <a name="remarks"></a>Comentários

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

 

 
