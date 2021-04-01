---
description: Define a cadeia de caracteres do identificador especificado nos metadados do volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Método setidentificafield da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836975"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a>Método setidentificafield da classe Win32 \_ EncryptableVolume

O método **Setidentificafield** da classe [**\_ EncryptableVolume do Win32**](win32-encryptablevolume.md) define a cadeia de caracteres do identificador especificado nos metadados do volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Identificação do identificador* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que especifica o campo de identificação que é atribuído ao volume. Se a cadeia de caracteres opcional não estiver presente, os valores definidos do registro serão usados. Se a cadeia de caracteres estiver presente e não estiver vazia, o valor especificado será usado. O parâmetro *identificafield* não diferencia maiúsculas de minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                  | Descrição                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                                                                           |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl> | Esta unidade está bloqueada por Criptografia de Unidade de Disco BitLocker. Você deve desbloquear este volume no painel de controle. <br/> |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl> | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




