---
description: Recupera o perfil de validação de plataforma para um determinado protetor de chave do tipo apropriado.
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
ms.openlocfilehash: 9563fc306bd8d50ce4f0c13164640ecee8e99d441b1b923df35cce8615097c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667786"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorPlatformValidationProfile da classe \_ EncryptableVolume win32

O **método GetKeyProtectorPlatformValidationProfile** recupera o perfil de validação da plataforma para um determinado protetor de chave do tipo apropriado.

O identificador do protetor de chave deve se referir a um protetor de chave do tipo "TPM", "TPM e PIN", "TPM e PIN e chave de inicialização" ou "TPM e chave de inicialização".

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*PlatformValidationProfile* \[ out\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de inteiros que especifica como o hardware de segurança Trusted Platform Module (TPM) do computador segura a chave de criptografia do volume de disco.



| Valor                                                                         | Significado                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Raiz principal da crtm (confiança de medida), BIOS e extensões de plataforma<br/> |
| <dl> <dt>1</dt> </dl>  | Configuração de plataforma e placa-mãe e dados<br/>                         |
| <dl> <dt>2</dt> </dl>  | Código ROM da opção<br/>                                                         |
| <dl> <dt>3</dt> </dl>  | Configuração e dados de ROM da opção<br/>                                       |
| <dl> <dt>4</dt> </dl>  | Código MBR (Registro mestre de inicialização)<br/>                                           |
| <dl> <dt>5</dt> </dl>  | Tabela de partição MBR (Registro Mestre de Inicialização)<br/>                                |
| <dl> <dt>6</dt> </dl>  | Eventos de transição de estado e a adoção<br/>                                        |
| <dl> <dt>7</dt> </dl>  | Computador Manufacturer-Specific<br/>                                          |
| <dl> <dt>8</dt> </dl>  | Setor de inicialização NTFS<br/>                                                        |
| <dl> <dt>9</dt> </dl>  | Bloco de inicialização NTFS<br/>                                                         |
| <dl> <dt>10</dt> </dl> | Gerenciador de Inicialização<br/>                                                            |
| <dl> <dt>11</dt> </dl> | Controle de acesso do BitLocker<br/>                                                |
| <dl> <dt>12</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>13</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>14</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>15</dt> </dl> | Definido para uso pelo sistema operacional estático<br/>                          |
| <dl> <dt>16</dt> </dl> | Usado para depuração<br/>                                                      |
| <dl> <dt>17</dt> </dl> | CRTM dinâmico<br/>                                                            |
| <dl> <dt>18</dt> </dl> | Plataforma definida<br/>                                                        |
| <dl> <dt>19</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>20</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>21</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>22</dt> </dl> | Usado por um sistema operacional confiável<br/>                                      |
| <dl> <dt>23</dt> </dl> | Suporte a aplicativos<br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                  | Descrição                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                                                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O *parâmetro VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "TPM", "TPM e PIN", "TPM e PIN e chave de inicialização" ou "TPM e chave de inicialização".<br/> |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker.<br/>                                                                                  |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows aplicativos da área de trabalho do Vista Ultimate \[\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                    |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
