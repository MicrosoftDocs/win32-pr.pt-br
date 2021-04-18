---
description: Recupera o número de vezes que o BitLocker foi suspenso.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Método GetSuspendCount da classe Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810495"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Método GetSuspendCount da classe Win32 \_ EncryptableVolume

O método **GetSuspendCount** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera o número de reinicializações antes que a proteção seja retomada automaticamente.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SuspendCount* 
</dt> <dd>

Um valor inteiro de 0 a 15.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código de retorno                                                                                          | Descrição                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | O método foi bem-sucedido.<br/>                                      |
| <dl> <dt>**ERRO \_ sem \_ suporte**</dt> </dl> | Retornado se o volume não estiver suspenso ou não for um volume do sistema operacional.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método só se aplica ao volume do sistema operacional e somente se ele estiver realmente suspenso no momento. Se o volume não estiver suspenso ou não for um volume do sistema operacional, o **erro \_ não terá \_ suporte** será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 Enterprise, \[ somente aplicativos de área de trabalho do Windows 8 pro\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| parâmetro<br/>                   | <dl> <dt>Activdbg. h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 




