---
description: Desmonta o volume e remove a chave de criptografia do volume da memória do sistema.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Método Lock da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f5053fe027bbae51ce93feb11de5f95bde1d7b17c85a05df1386e5470b1b20fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867656"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a>Método Lock da classe Win32 \_ EncryptableVolume

O método **Lock** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) desmonta o volume e remove a chave de criptografia do volume da memória do sistema. O conteúdo do volume permanece inacessível até que seja desbloqueado pelo método [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou pelo método [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) . Este método não pode ser executado com êxito para o volume do sistema operacional em execução no momento.

> [!Note]  
> Se o disco oferecer suporte à criptografia de hardware, a banda será definida como "bloqueada".

 

## <a name="syntax"></a>Sintaxe


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ForceDismount* \[ em, opcional\]
</dt> <dd>

Tipo: **booliano**

Se **true** , o disco será forçosamente desmontado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                           | Descrição                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | O método foi bem-sucedido.<br/>                                                                                                                                     |
| <dl> <dt>**E \_ ACESSO \_ negado**</dt> <dt>2147942405 (0x80070005)</dt> </dl>               | Os aplicativos estão acessando este volume. Se todo o acesso for não exclusivo, especificar o parâmetro *ForceDismount* como true permitirá que o método seja executado com êxito.<br/> |
| <dl> <dt>**FVE \_ E \_ não \_ criptografado**</dt> <dt>2150694913 (0x80310001)</dt> </dl>          | O volume está totalmente descriptografado e não pode ser bloqueado.<br/>                                                                                                            |
| <dl> <dt>**FVE \_ E \_ proteção \_ desabilitada**</dt> <dt>2150694945 (0x80310021)</dt> </dl>    | A chave de criptografia do volume está disponível em branco no disco, impedindo que o volume seja bloqueado.<br/>                                                    |
| <dl> <dt>**FVE \_ E \_ chave de recuperação \_ \_ necessária**</dt> <dt>2150694946 (0x80310022)</dt> </dl> | O volume não tem protetores de chave do tipo "senha numérica" ou "chave externa" que são necessários para desbloquear o volume.<br/>                            |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows vista Enterprise, \[ somente aplicativos de área de trabalho do vista Ultimate Windows\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                    |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
