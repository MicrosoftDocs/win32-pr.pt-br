---
description: Retorna a versão de metadados FVE do volume.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Método GetVersion da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796356"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a>Método GetVersion da classe Win32 \_ EncryptableVolume

O método **GetVersion** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retorna a versão de metadados FVE do volume.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Versão* \[ do fora\]
</dt> <dd>

Tipo: **UInt32**

Um inteiro sem sinal que indica a versão de metadados do volume.



| Valor                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt></dt> <dt>0</dt> desconhecido </dl> | O sistema operacional é desconhecido.<br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <dt>**Vista**</dt> <dt>1</dt> </dl>         | Formato do Windows Vista, o que significa que o volume foi protegido com o BitLocker em um computador que executa o Windows Vista.<br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <dt>**Win7**</dt> <dt>2</dt> </dl>             | Formato do Windows 7, o que significa que o volume foi protegido com o BitLocker em um computador que executa o Windows 7 ou o formato de metadados foi atualizado usando o método [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.

Se o volume já estiver desbloqueado e nenhum outro erro ocorrer, esse método retornará zero.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                       | O método foi bem-sucedido.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt> </dl> | O valor do parâmetro de *versão* não é válido.<br/> |
| <dl> <dt>**Erro \_ do \_Dados INválidos**</dt> <dt>13 (0xD)</dt> </dl>       | O driver retornou um formato de dados sem suporte.<br/>     |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

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

 

 
