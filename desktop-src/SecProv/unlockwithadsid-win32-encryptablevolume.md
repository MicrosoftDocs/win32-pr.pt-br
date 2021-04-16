---
description: Usa a cadeia de caracteres de SID (identificador de segurança) Active Directory fornecida para obter a chave derivada e desbloquear o volume criptografado.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Método UnlockWithAdSid da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754118"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a>Método UnlockWithAdSid da classe Win32 \_ EncryptableVolume

O método **UnlockWithAdSid** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) usa a cadeia de caracteres de Sid (identificador de segurança) Active Directory fornecida para obter a chave derivada e desbloquear o volume criptografado.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, essa função definirá o status da banda como "desbloqueado" "

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SidString* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém o Active Directory SID.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
