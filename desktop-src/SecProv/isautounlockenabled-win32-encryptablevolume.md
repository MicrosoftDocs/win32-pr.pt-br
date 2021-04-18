---
description: Indica se o volume é desbloqueado automaticamente quando é montado.
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
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810494"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a>Método IsAutoUnlockEnabled da classe Win32 \_ EncryptableVolume

O método **IsAutoUnlockEnabled** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se o volume será desbloqueado automaticamente quando for montado (por exemplo, quando dispositivos de memória removível estiverem conectados ao computador).

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsAutoUnlockEnabled* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Um valor booliano que será true se a chave externa usada para desbloquear automaticamente o volume existir e tiver sido armazenada no volume do sistema operacional em execução no momento; caso contrário, será false.

</dd> <dt>

*VolumeKeyProtectorID* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo que contém a ID do protetor de chave de volume criptografado associado se *IsAutoUnlockEnabled* for true.

Se *IsAutoUnlockEnabled* for false, *VolumeKeyProtectorID* será uma cadeia de caracteres vazia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                     | Descrição                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                     | O método foi bem-sucedido.<br/>                                                       |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>    | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker.<br/> |
| <dl> <dt>**FVE \_ E \_ não \_ \_ VOLUME de dados**</dt> <dt>2150694937 (0x80310019)</dt> </dl> | O método não pode ser executado para o volume do sistema operacional em execução no momento.<br/>      |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]<br/>                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
