---
description: Remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usados para desbloquear automaticamente os volumes de dados.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Método ClearAllAutoUnlockKeys da classe Win32_EncryptableVolume dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 46ee3791425afafe63b0d566c3f4204fecc9195f4341b90caee4c95306afdeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668166"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a>Método ClearAllAutoUnlockKeys da classe EncryptableVolume do Win32 \_

O **método ClearAllAutoUnlockKeys** da classe [**\_ EncryptableVolume win32**](win32-encryptablevolume.md) remove todas as chaves externas e informações relacionadas salvas no volume do sistema operacional em execução no momento que são usados para desbloquear automaticamente os volumes de dados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Valor/código de retorno                                                                                                                                                                   | Descrição                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                   | O método foi bem-sucedido.<br/>                                                        |
| <dl> <dt>**FVE \_ E \_ NOT \_ ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt> </dl>  | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/> |
| <dl> <dt>**FVE \_ E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt> </dl> | O método só pode ser executado para o volume do sistema operacional em execução no momento.<br/>     |



 

## <a name="remarks"></a>Comentários

**ClearAllAutoUnlockKeys** atinge a mesma funcionalidade que executar [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) para cada volume de dados que já foi associado ao sistema operacional em execução no momento, até mesmo volumes de dados que não estão conectados ao computador no momento. Ele também remove todas as informações de desbloqueio desassociadas associadas a volumes de dados que não existem mais.

Antes de chamar [**Descriptografar**](decrypt-win32-encryptablevolume.md) no volume do sistema operacional em execução no momento, use **ClearAllAutoUnlockKeys** para garantir que as informações colocadas no registro do sistema operacional para desbloquear automaticamente volumes de dados não estão acessíveis em disco limpo.

Depois **que ClearAllAutoUnlockKeys** for executado com êxito, os métodos [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) poderão ser usados para desbloquear todos os volumes de dados neste computador. Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) para habilitar o desbloqueio automático de um volume de dados.

Se nenhum outro erro for retornado, **ClearAllAutoUnlockKeys** removerá do Registro quaisquer IDs de protetor de volume e chaves externas usadas para desbloquear automaticamente qualquer volume de dados que já tenha sido associado ao volume do sistema operacional em execução no momento.

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

 

 
