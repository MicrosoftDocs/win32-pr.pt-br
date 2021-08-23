---
description: Recupera a chave externa para um determinado protetor de chave.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Método GetKeyProtectorExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f6db531e28880c6b47cb41d87769917a524965984e2a2fc1099f0d0aa65095f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667886"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectorExternalKey da classe EncryptableVolume do Win32 \_

O **método GetKeyProtectorExternalKey** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera a chave externa para um determinado protetor de chave do tipo apropriado.

O identificador do protetor de chave deve se referir a um protetor de chave do tipo "Chave Externa", "TPM e PIN e chave de inicialização" ou "TPM e chave de inicialização".

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado.

</dd> <dt>

*ExternalKey* \[ out\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de bytes que especifica a chave externa de 256 bits que pode ser usada para desbloquear o volume correspondente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                  | Descrição                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                                                                                  |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | O volume está bloqueado.<br/>                                                                                                                                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O *parâmetro VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "Chave Externa", "TPM e PIN e Chave de Inicialização" ou "TPM e Chave de Inicialização".<br/> |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                           |



 

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

 

 
