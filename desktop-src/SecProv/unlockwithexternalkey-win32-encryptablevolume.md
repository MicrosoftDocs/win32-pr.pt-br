---
description: Usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Método UnlockWithExternalKey da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a61e85608e8ed0f3e5b014d015ce7d59c4f01c8d97ab9092864fe9bb338833ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004214"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithExternalKey da classe EncryptableVolume do Win32 \_

O **método UnlockWithExternalKey** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) usa uma chave externa fornecida para acessar o conteúdo de um volume de dados.

A chave de criptografia do volume deve ter sido protegida com um ou mais protetores de chave do tipo "Chave Externa" usando o [**método ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para poder desbloquear o volume com esse método.

> [!Note]  
> Se o disco dá suporte à criptografia de hardware, essa função define o status da banda como "desbloqueado""

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ExternalKey* \[ Em\]
</dt> <dd>

Tipo: **uint8 \[ \]**

Uma matriz de bytes que especifica a chave externa de 256 bits usada para desbloquear o volume. Essa chave pode ser obtida chamando o [**método GetExternalKeyFromFile.**](getexternalkeyfromfile-win32-encryptablevolume.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se o volume já estiver desbloqueado, esse método retornará 0.



| Valor/código de retorno                                                                                                                                                                  | Descrição                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                                                       |
| <dl> <dt>**ERRO \_ NOT \_ FOUND**</dt> <dt>Nenhum valor determinado (0x)</dt> </dl>          | O volume não tem um protetor de chave do tipo "Chave Externa".<br/>                                                             |
| <dl> <dt>**ERRO \_ SENHA \_ INVÁLIDA**</dt> <dt>Nenhum valor fornecido (0x)</dt> </dl>   | Existe um ou mais protetores de chave do tipo "Chave Externa", mas o parâmetro *ExternalKey* especificado não pode desbloquear o volume.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>          | O *parâmetro ExternalKey* não é uma matriz de tamanho 4.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                |



 

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Windows SDK. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

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

 

 
