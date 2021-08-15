---
description: Indica se o conteúdo do volume pode ser acessado de Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Método GetLockStatus da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: caa213dbebc7db07851bc8df41b5d9379d3dfe97ee207f9b2578b0567fd9b65b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118892012"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a>Método GetLockStatus da classe Win32 \_ EncryptableVolume

O método **GetLockStatus** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se o conteúdo do volume pode ser acessado de Windows.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LockStatus* \[ fora\]
</dt> <dd>

Tipo: **UInt32**

Especifica se o conteúdo do volume pode ser acessado de Windows.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <dt>**Desbloqueado**</dt> <dt>0</dt> </dl> | Para um HDD padrão:<br/> O conteúdo completo do volume pode ser acessado. Um volume desbloqueado está totalmente descriptografado ou tem a chave de criptografia disponível em apagar no disco. o volume que contém o sistema operacional em execução atual (por exemplo, o volume Windows em execução) é sempre acessível e não pode ser bloqueado.<br/> Para um EHDD:<br/> A banda é desbloqueada perpétuamente.<br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <dt>**Bloqueado**</dt> em <dt>1</dt> </dl>         | Para um HDD padrão:<br/> Toda ou uma parte do conteúdo do volume não está acessível. Um volume bloqueado deve ser parcialmente ou totalmente criptografado e não deve ter a chave de criptografia disponível no disco não criptografado.<br/> Para um EHDD:<br/> A banda está desbloqueada ou bloqueada.<br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Use [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) e [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) para obter acesso ao conteúdo do volume. Use o método [**Lock**](lock-win32-encryptablevolume.md) para ceder o acesso ao conteúdo do volume.

O volume que contém o sistema operacional em execução no momento é sempre acessível e não pode ser bloqueado.

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

 

 
