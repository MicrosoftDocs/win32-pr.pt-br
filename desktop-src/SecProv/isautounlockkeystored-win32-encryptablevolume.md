---
description: Indica se alguma chave externa ou informações relacionadas que podem ser usadas para desbloquear automaticamente volumes de dados existem no volume do sistema operacional em execução no momento.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Método IsAutoUnlockKeyStored da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: c28f8357edd88322f6f4498fd1e5b7156eeeff0b67d53b4d759c6935f4e9f9eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906306"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockKeyStored da classe EncryptableVolume do Win32 \_

O **método IsAutoUnlockKeyStored** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) indica se alguma chave externa ou informações relacionadas que podem ser usadas para desbloquear automaticamente volumes de dados existem no volume do sistema operacional em execução no momento.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsAutoUnlockKeyStored* \[ out\]
</dt> <dd>

Tipo: **booliana**

Será **true** se qualquer informação que possa ser usada para desbloquear automaticamente volumes de dados for armazenada no registro do volume do sistema operacional em execução no momento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                   | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl>  | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | O método só pode ser executado para o volume do sistema operacional em execução no momento.<br/>     |



 

## <a name="remarks"></a>Comentários

Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) para remover todas as informações de desbloqueio do volume do sistema operacional em execução no momento.

As informações usadas para desbloquear um volume são armazenadas [**quando EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) é executado para um volume de dados enquanto o volume do sistema operacional em execução no momento está em execução.

**IsAutoUnlockKeyStored** difere de [**IsAutoUnlockEnabled,**](isautounlockenabled-win32-encryptablevolume.md) pois, mesmo que o desbloqueio automático esteja desabilitado para todos os volumes de dados atualmente conectados ao computador, ainda poderá haver informações de desbloqueio associadas a volumes de dados desconectados ou volumes de dados que não existem mais.

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

 

 
