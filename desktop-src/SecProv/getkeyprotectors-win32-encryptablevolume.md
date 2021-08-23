---
description: Lista os protetores usados para proteger a chave de criptografia do volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Método GetKeyProtectors da Win32_EncryptableVolume classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 01342b932e3a285870026ef57bfa0040d1659ca7af1165e6fb67f3af780896d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667676"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyProtectors da classe EncryptableVolume do Win32 \_

O **método GetKeyProtectors** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) lista os protetores usados para proteger a chave de criptografia do volume. Se um tipo de protetor for fornecido, somente os protetores de chave de volume do tipo especificado serão retornados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*KeyProtectorType* \[ in, opcional\]
</dt> <dd>

Tipo: **uint32**

Um inteiro sem sinal que especifica o tipo de protetor de chave a ser retornada.

Se esse parâmetro não for especificado, todos os protetores de chave disponíveis do volume serão retornados.



| Valor                                                                         | Significado                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>  | Todos os tipos.<br/> Todos os protetores de chave são retornados.<br/> |
| <dl> <dt>1</dt> </dl>  | Trusted Platform Module (TPM).<br/>                         |
| <dl> <dt>2</dt> </dl>  | Chave externa.<br/>                                          |
| <dl> <dt>3</dt> </dl>  | Senha numérica.<br/>                                      |
| <dl> <dt>4</dt> </dl>  | TPM e PIN.<br/>                                           |
| <dl> <dt>5</dt> </dl>  | TPM e Chave de Inicialização.<br/>                                   |
| <dl> <dt>6</dt> </dl>  | TPM e PIN e chave de inicialização.<br/>                           |
| <dl> <dt>7</dt> </dl>  | Chave pública.<br/>                                            |
| <dl> <dt>8</dt> </dl>  | Senha.<br/>                                            |
| <dl> <dt>9</dt> </dl>  | Certificado TPM<br/>                                        |
| <dl> <dt>10</dt> </dl> | SID (Identificador de Segurança)<br/>                              |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres \[ \]**

Uma matriz de cadeias de caracteres que identificam os protetores de chave usados para proteger a chave de criptografia do volume.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                  | Descrição                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O *parâmetro VolumeKeyProtectorID* é especificado, mas não se refere a *um KeyProtectorType válido.*<br/> |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                   |



 

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

 

 
