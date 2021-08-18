---
description: Exclui todos os protetores de chave para o volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Método DeleteKeyProtectors da classe Win32_EncryptableVolume dados
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
ms.openlocfilehash: 49884566a45bde4977d56baa3e83ae4c42fdd676447a3da1f3df528ec823c414
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004604"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a>Método DeleteKeyProtectors da classe EncryptableVolume do Win32 \_

O **método DeleteKeyProtectors** da [**classe Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exclui todos os protetores de chave para o volume.

Se um volume não criptografado tiver protetores de chave, quando **DeleteKeyProtectors** for executado com êxito, o volume reverterá para um sistema de arquivos NTFS padrão.

Se o volume ainda não estiver totalmente descriptografado, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) antes de executar **DeleteKeyProtectors** para garantir que as partes criptografadas do volume permaneçam acessíveis.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                          | Descrição                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                          | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FVE \_ E \_ LOCKED \_ VOLUME**</dt> <dt>2150694912 (0x80310000)</dt> </dl>         | O volume está bloqueado.<br/>                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FVE \_ E \_ KEY \_ REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt> </dl>          | O último protetor de chave para um volume parcial ou totalmente criptografado não poderá ser removido se os protetores de chave estão habilitados. Use [**DisableKeyProtectors antes**](disablekeyprotectors-win32-encryptablevolume.md) de remover esse último protetor de chave para garantir que partes criptografadas do volume permaneçam acessíveis. <br/> |
| <dl> <dt>**FVE \_ E \_ VOLUME BOUND JÁ \_ \_ 2150694943**</dt> <dt>(0x8031001F)</dt> </dl> | Os protetores de chave não podem ser excluídos porque um deles está sendo usado para desbloquear automaticamente o volume. <br/> Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para desabilitar o desbloqueio automático antes de executar esse método.<br/>                                                       |



 

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

 

 
