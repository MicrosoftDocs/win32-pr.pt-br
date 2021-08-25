---
description: Recupera o número de vezes que o BitLocker foi suspenso.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Método GetSuspendCount da classe Win32_EncryptableVolume (Activdbg.h)
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
ms.openlocfilehash: 468bd6cdc8f3df7efba26997fd76b0724d3e4cc5da552275dad5201adc469f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906346"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a>Método GetSuspendCount da classe EncryptableVolume do Win32 \_

O **método GetSuspendCount** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) recupera o número de reinicializações antes que a proteção seja retomada automaticamente.

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

## <a name="return-value"></a>Valor retornado

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código de retorno                                                                                          | Descrição                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | O método foi bem-sucedido.<br/>                                      |
| <dl> <dt>**ERRO \_ SEM \_ SUPORTE**</dt> </dl> | Retornado se o volume não estiver suspenso ou não for um volume do sistema operacional.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método só se aplica ao volume do sistema operacional e somente se ele estiver realmente suspenso no momento. Se o volume não estiver suspenso ou não for um volume do sistema operacional, **ERROR \_ NOT \_ SUPPORTED** será retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 Enterprise, Windows 8 Pro \[ somente aplicativos da área de trabalho\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftVolumeEncryption<br/>                                             |
| Cabeçalho<br/>                   | <dl> <dt>Activdbg.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume.mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)
</dt> </dl>

 

 




