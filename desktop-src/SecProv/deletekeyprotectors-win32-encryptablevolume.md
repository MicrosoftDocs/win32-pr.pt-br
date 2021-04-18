---
description: Exclui todos os protetores de chave do volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Método DeleteKeyProtectors da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760006"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DeleteKeyProtectors da classe Win32 \_ EncryptableVolume

O método **DeleteKeyProtectors** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exclui todos os protetores de chave do volume.

Se um volume não criptografado tiver protetores de chave, quando **DeleteKeyProtectors** for executado com êxito, o volume será revertido para um sistema de arquivos NTFS padrão.

Se o volume ainda não tiver sido totalmente descriptografado, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de executar **DeleteKeyProtectors** para garantir que partes criptografadas do volume permaneçam acessíveis.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | O volume está bloqueado.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ \_Chave E \_ necessária**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | O último protetor de chave para um volume parcialmente ou totalmente criptografado não poderá ser removido se os protetores de chave estiverem habilitados. Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de remover esse último protetor de chave para garantir que partes criptografadas do volume permaneçam acessíveis. <br/> |
| <dl> <dt>**FVE \_ E o \_ volume \_ associado \_ já**</dt> <dt>2150694943 (0x8031001F)</dt> </dl> | Os protetores de chave não podem ser excluídos porque um deles está sendo usado para desbloquear automaticamente o volume. <br/> Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para desabilitar o desbloqueio automático antes de executar este método.<br/>                                                       |



 

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

 

 
