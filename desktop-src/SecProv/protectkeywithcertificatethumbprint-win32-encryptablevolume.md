---
description: Método ProtectKeyWithCertificateThumbprint da classe Win32_EncryptableVolume – valida o OID (identificador de objeto) de uso avançado de chave (EKU) do certificado fornecido.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Método ProtectKeyWithCertificateThumbprint da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110574"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithCertificateThumbprint da classe Win32 \_ EncryptableVolume

O método **ProtectKeyWithCertificateThumbprint** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) valida o OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) de uso avançado de chave (EKU) do certificado fornecido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyName* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica um identificador de cadeia de caracteres atribuído pelo usuário para esse protetor de chave. Se esse parâmetro não for especificado, o parâmetro *FriendlyName* será criado usando o nome da entidade no certificado.

</dd> <dt>

*CertThumbprint* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica a impressão digital do certificado.

</dd> <dt>

*VolumeKeyProtectorID* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que identifica exclusivamente o protetor de chave criado que pode ser usado para gerenciar esse protetor de chave.

Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                                           | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                          |
| <dl> <dt>**Erro \_ do \_Dados INválidos**</dt> <dt>13 (0xD)</dt> </dl>                                           | Os dados não são válidos.<br/>                                                                                                                                                                                                                                                              |
| <dl> <dt>**FVE \_ E \_ não é o \_ \_ OID do BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt> </dl>                     | O atributo EKU do certificado especificado não permite que ele seja usado para Criptografia de Unidade de Disco BitLocker. O BitLocker não exige que um certificado tenha um atributo EKU, mas se um estiver configurado, ele deverá ser definido como um OID que corresponda à OID configurada para o BitLocker.<br/> |
| <dl> <dt>**FVE \_ O \_ certificado de usuário de política E \_ não é \_ \_ \_ permitido**</dt> <dt>2150695026 (0x80310072)</dt> </dl> | Política de Grupo não permite que certificados de usuário, como cartões inteligentes, sejam usados com o BitLocker.<br/>                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ O \_ certificado do usuário da política E \_ \_ \_ deve \_ ser \_ HW**</dt> <dt>2150695028 (0x80310074)</dt> </dl>        | Política de Grupo exige que você forneça um cartão inteligente para usar o BitLocker.<br/>                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ A \_ política E \_ proíbe \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt> </dl>           | Política de Grupo não permite o uso de certificados autoassinados.<br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Se o OID não corresponder ao que está associado ao controlador de serviço no registro, esse método falhará. Isso impede que o usuário configure os protetores do agente de recuperação de dados (DRA) manualmente no volume. Os DRAs são apenas para serem definidos pelo serviço.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
