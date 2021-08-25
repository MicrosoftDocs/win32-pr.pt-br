---
description: Recupera a senha numérica para um determinado protetor de chave.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Método GetKeyProtectorNumericalPassword da classe Win32_EncryptableVolume dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a97740338b55238a441c2f08dedf4324144625e3bc58a684f36f0ae98886e0b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100636"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorNumericalPassword da classe EncryptableVolume do Win32 \_

O **método GetKeyProtectorNumericalPassword** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) recupera a senha numérica para um determinado protetor de chave do tipo apropriado.

O identificador do protetor de chave deve se referir a um protetor de chave do tipo "Senha Numérica".

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*NumericalPassword* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Uma cadeia de caracteres que representa a senha que pode ser usada para desbloquear o volume correspondente.

A senha numérica tem 48 dígitos. Esses dígitos são divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo indicando um valor de verificação para o grupo. Supondo que um grupo de seis dígitos seja rotulado como x1, x2, x3, x4, x5 e x6, o dígito de checksum x6 é calculado como –x1+x2-x3+x4-x5 mod 11.

Os grupos de dígitos são separados por um hífen. Portanto, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" é o formato da senha retornada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                  | Descrição                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                               |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O *parâmetro VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "Senha Numérica".<br/> |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                        |



 

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

 

 
