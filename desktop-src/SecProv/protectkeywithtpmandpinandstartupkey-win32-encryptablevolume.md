---
description: Protege a chave de criptografia do volume usando o Trusted Platform Module (TPM) no computador, se disponível, aprimorado por um PIN (número de identificação pessoal) especificado pelo usuário e por uma chave externa que deve ser apresentada ao computador na inicialização.
ms.assetid: 8991c22c-1e36-415e-a82b-c5ddf9c3b24a
title: Método ProtectKeyWithTPMAndPINAndStartupKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPINAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9f315629c810027e18dac3a337c126f4a4a4bcce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662663"
---
# <a name="protectkeywithtpmandpinandstartupkey-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithTPMAndPINAndStartupKey da classe Win32 \_ EncryptableVolume

O método **ProtectKeyWithTPMAndPINAndStartupKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume usando o Trusted Platform Module (TPM) no computador, se disponível, aprimorado por um PIN (número de identificação pessoal) especificado pelo usuário e por uma chave externa que deve ser apresentada ao computador na inicialização.

Três fatores de autenticação são necessários para desbloquear o conteúdo criptografado do volume:

1.  Validação pelo TPM
2.  Entrada de um PIN de 4 a 20 dígitos ou, se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, de 4 a 20 letras, símbolos, espaços ou números
3.  Entrada de um dispositivo de memória USB que contém a chave externa

Use o método [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) para salvar essa chave externa em um arquivo em um dispositivo de memória USB para uso como uma chave de inicialização. Esse método se aplica somente ao volume do sistema operacional. Um protetor de chave do tipo "TPM e PIN e chave de inicialização" é criado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProtectKeyWithTPMAndPINAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile,
  [in]           string PIN,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyName* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que rotula esse protetor de chave. Se esse parâmetro não for especificado, um valor em branco será usado.

</dd> <dt>

*PlatformValidationProfile* \[ em, opcional\]
</dt> <dd>

Tipo: **uint8**

Uma matriz de inteiros que especifica como o TPM do computador protege a chave de criptografia do volume. Um perfil de validação de plataforma consiste em um conjunto de índices de PCR (registro de configuração de plataforma) que variam de 0 a 23, inclusive. Os valores de repetição no parâmetro são ignorados. Cada índice de PCR é associado a serviços que são executados quando o sistema operacional é iniciado. Cada vez que o computador for iniciado, o TPM verificará se os serviços especificados no perfil de validação de plataforma não foram alterados. Se qualquer um desses serviços for alterado enquanto a proteção do BitLocker permanecer ativada, o TPM não liberará a chave de criptografia para desbloquear o volume e o computador entrará no modo de recuperação.

Se esse parâmetro não for especificado, os índices padrão de 0, 2, 4, 5, 8, 9, 10 e 11 serão usados. O perfil de validação de plataforma padrão protege a chave de criptografia contra alterações na raiz principal da CRTM (relação de confiança de medida), BIOS e extensões de plataforma (PCR 0), código de ROM de opção (PCR 2), código de registro de inicialização mestre (PCR 4), tabela de partição MBR (registro mestre de inicialização) (PCR 5), o setor de inicialização NTFS (PCR 8), o bloco de inicialização NTFS (PCR 9), o Gerenciador de inicialização (PCR 10) e o controle de acesso do BitLocker (PCR 11). Os computadores baseados em Unified Extensible Firmware Interface (UEFI) não usam a PCR 5 por padrão.

O perfil de validação de plataforma padrão é recomendado. Para proteção adicional contra alterações de configuração de inicialização antecipada, use um perfil de PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.

A alteração do perfil padrão afeta a segurança e a capacidade de gerenciamento do seu computador. A sensibilidade do BitLocker com as modificações de plataforma (maliciosas ou autorizadas) é aumentada ou reduzida, dependendo da inclusão ou exclusão, respectivamente, do PCRs. Para que a proteção do BitLocker seja habilitada, o perfil de validação de plataforma deve incluir o PCR 11.



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



 

</dd> <dt>

*Fixar* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Contém um número de identificação pessoal de 4 a 20 dígitos (PIN) ou, se a política de grupo "permitir PINs avançados para inicialização" estiver habilitada, 4 e 20 letras, símbolos, espaços ou números. Essa cadeia de caracteres deve ser fornecida ao computador na inicialização.

</dd> <dt>

*ExternalKey* \[ em, opcional\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume quando o computador é iniciado. Deixe esse parâmetro em branco para gerar aleatoriamente a chave externa. Use o método [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) para obter a chave gerada aleatoriamente.

</dd> <dt>

*VolumeKeyProtectorID* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

O identificador de cadeia de caracteres exclusivo atualizado usado para gerenciar um protetor de chave de volume criptografado.

Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                        | O parâmetro *PlatformValidationProfile* é fornecido, mas seus valores não estão dentro do intervalo conhecido ou não correspondem à configuração de política de grupo que está atualmente em vigor.<br/> O parâmetro *ExternalKey* é fornecido, mas não é uma matriz de tamanho de 32.<br/> |
| <dl> <dt>**FVE \_ E \_ inicializável \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt> </dl>              | Um CD/DVD inicializável foi encontrado neste computador. Remova o CD/DVD e reinicie o computador.<br/>                                                                                                                                                                               |
| <dl> <dt>**FVE \_ E \_ o \_ VOLUME externo**</dt> <dt>2150694947 (0x80310023)</dt> </dl>              | O TPM não pode proteger a chave de criptografia do volume porque o volume não contém o sistema operacional em execução no momento.<br/>                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ \_ \_ caracteres de PIN inválidos**</dt> <dt>2150695066 (0x8031009A)</dt> </dl>          | O parâmetro *NewPIN* contém caracteres que não são válidos. Quando a Política de Grupo "permitir PINs avançados para inicialização" está desabilitada, somente os números têm suporte.<br/>                                                                                                        |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>               | O volume está bloqueado.<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**FVE \_ \_Política E \_ \_ \_ comprimento de PIN inválido**</dt> <dt>2150695016 (0x80310068)</dt> </dl> | O parâmetro *NewPIN* fornecido tem mais de 20 caracteres, menos de 4 caracteres ou menos que o comprimento mínimo especificado por política de grupo.<br/>                                                                                                          |
| <dl> <dt>**FVE \_ O \_ protetor E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt> </dl>            | Já existe um protetor de chave deste tipo.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**TBS \_ O \_ serviço E \_ não \_ está executando**</dt> o <dt>2150121480 (0x80284008)</dt> </dl>        | Nenhum TPM compatível foi encontrado neste computador.<br/>                                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Comentários

No máximo um protetor de chave do tipo "TPM e PIN e chave de inicialização" pode existir para um volume a qualquer momento. Se você quiser alterar o nome de exibição ou o perfil de validação de plataforma usado por um protetor de chave "TPM e PIN e chave de inicialização" existente, primeiro deverá remover o protetor de chave existente e, em seguida, chamar **ProtectKeyWithTPMAndPINAndStartupKey** para criar um novo.

Protetores de chave adicionais devem ser especificados para desbloquear o volume em cenários de recuperação em que o acesso à chave de criptografia do volume não pode ser obtido; por exemplo, quando o TPM não puder ser validado com êxito no perfil de validação de plataforma ou quando o PIN for perdido. Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) para criar um ou mais protetores de chave para recuperar um volume bloqueado de outra forma.

Embora seja possível ter tanto um protetor de chave do tipo "TPM" quanto outro do tipo "TPM e PIN e chave de inicialização", a presença do tipo de protetor de chave "TPM" nega os efeitos de outros protetores de chave baseados em TPM.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise com SP1, somente Windows Vista Ultimate com SP1 para \[ aplicativos de área de trabalho\]<br/>     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
