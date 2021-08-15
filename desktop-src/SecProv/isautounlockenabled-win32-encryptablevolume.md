---
description: Indica se o volume é desbloqueado automaticamente quando ele é montado.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Método IsAutoUnlockEnabled da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 19437bf40d27bea87103beecfbe8bee71e404c054ace46cb9728f7ac992b5c85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891907"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockEnabled da classe EncryptableVolume do Win32 \_

O **método IsAutoUnlockEnabled** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) indica se o volume é desbloqueado automaticamente quando montado (por exemplo, quando dispositivos de memória removível estão conectados ao computador).

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsAutoUnlockEnabled* \[ out\]
</dt> <dd>

Tipo: **booliana**

Um valor booliana true se a chave externa usada para desbloquear automaticamente o volume existir e tiver sido armazenada no volume do sistema operacional em execução no momento, caso contrário, será false.

</dd> <dt>

*VolumeKeyProtectorID* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um identificador de cadeia de caracteres exclusivo que contém a ID do protetor de chave de volume criptografada associada se *IsAutoUnlockEnabled* for true.

Se *IsAutoUnlockEnabled* for false, *VolumeKeyProtectorID* será uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                     | Descrição                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | O método foi bem-sucedido.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ \_ NOTACTIVATED 2150694920**</dt> <dt>(0x80310008)</dt> </dl>    | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | O método não pode ser executado para o volume do sistema operacional em execução no momento.<br/>      |



 

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

 

 
