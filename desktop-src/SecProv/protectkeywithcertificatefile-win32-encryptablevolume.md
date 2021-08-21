---
description: Método ProtectKeyWithCertificateFile da classe Win32_EncryptableVolume - Valida o OID (Identificador de Objeto de Uso Avançado de Chave) (EKU) do certificado fornecido.
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Método ProtectKeyWithCertificateFile da classe Win32_EncryptableVolume dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e96667af5e9c16097e951f3162082a6fb06b13d0504da3e8582b9f1b7ebfd4cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004454"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithCertificateFile da classe EncryptableVolume do Win32 \_

O **método ProtectKeyWithCertificateFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) valida o [*identificador*](../secgloss/o-gly.md) de objeto EKU (Uso Avançado de Chave) do certificado fornecido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyName* \[ in, opcional\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave. Se esse parâmetro não for especificado, o *parâmetro FriendlyName* será criado usando o Nome da Assunto no certificado.

</dd> <dt>

*FileName* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que especifica o local e o nome do arquivo .cer usado para habilitar o BitLocker. Um certificado de criptografia deve ser exportado no formato .cer ( binário codificado por [*DER (Distinguished Encoding Rules)*](../secgloss/d-gly.md) [*X.509*](../secgloss/x-gly.md) ou X.509 codificado em Base 64). O certificado de criptografia pode ser gerado a partir da PKI da Microsoft, PKI de terceiros ou auto-assinado.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado que pode ser usado para gerenciar esse protetor de chave.

Se a unidade for compatível com criptografia de hardware e o BitLocker não tiver assumido a propriedade da banda, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado em metadados por banda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ \_ OID \_ NÃO BITLOCKER 2150695022**</dt> <dt>(0x8031006E)</dt> </dl>                     | O atributo EKU do certificado especificado não permite que ele seja usado para Criptografia de Unidade de Disco BitLocker. O BitLocker não exige que um certificado tenha um atributo EKU, mas se um estiver configurado, ele deverá ser definido como um OID que corresponde ao OID configurado para o BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERTIFICATE NOT \_ \_ \_ \_ ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | Política de Grupo permite que certificados de usuário, como cartões inteligentes, sejam usados com o BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ POLICY USER CERT DEVE SER \_ \_ \_ \_ \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Política de Grupo requer que você fornece um cartão inteligente para usar o BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ A POLÍTICA DE E \_ \_ PROÍBE A \_ 2150695046**</dt> <dt>(0x80310086)</dt> </dl>           | Política de Grupo não permite o uso de certificados auto-assinados.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**ERRO \_ ARQUIVO \_ NÃO \_ ENCONTRADO**</dt> <dt>0000000002 (0x2)</dt> </dl>                                | O sistema não pode encontrar o arquivo especificado.<br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Comentários

Se o OID não corresponder ao associado ao controlador de serviço no Registro, esse método falhará. Isso impede que o usuário de configurar os protetores do DRA (agente de recuperação de dados) manualmente no volume. Os DRAs só devem ser definidos pelo serviço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 Enterprise, Windows 7 aplicativos de área de \[ trabalho ultimate\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                 |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 
