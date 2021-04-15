---
description: Exporta informações que podem ajudar a recuperar dados criptografados quando a unidade está seriamente danificada e não existem arquivos de backup de dados.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Método GetKeyPackage da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761387"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a>Método GetKeyPackage da classe Win32 \_ EncryptableVolume

O método **GetKeyPackage** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exporta informações que podem ajudar a recuperar dados criptografados quando a unidade está seriamente danificada e não existem arquivos de backup de dados.

As informações exportadas consistem na chave de criptografia do volume protegida por um protetor de chave do tipo "senha numérica" ou "chave externa". Para usar esse pacote, você também deve salvar a senha numérica ou a chave externa correspondente.

> [!IMPORTANT]
> Se você optar por exportar um pacote de chaves, certifique-se de manter essas informações em um local bem protegido. Não carregue essas informações com seu computador. Se esse pacote de chaves for perdido ou roubado, você precisará descriptografar o volume e criptografá-lo novamente usando uma nova chave.

 

No caso de uma falha de unidade, a ferramenta de reparo do BitLocker existe para ajudar a recuperar os dados disponíveis. Para obter mais informações sobre como essa ferramenta pode usar o pacote de chaves, consulte [como usar a ferramenta de reparo do BitLocker para ajudar a recuperar dados de um volume criptografado no Windows Vista](https://support.microsoft.com/kb/928201).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*VolumeKeyProtectorID* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Um identificador de cadeia de caracteres exclusivo usado para gerenciar um protetor de chave de volume criptografado. Para exportar um pacote de chaves, você deve usar um protetor de chave do tipo "senha numérica" ou "chave externa".

</dd> <dt>

*\[ Pacote \]* de \[out\]
</dt> <dd>

Tipo: **uint8**

Um fluxo de bytes que contém a chave de criptografia para um volume, protegido pelo protetor de chave especificado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                            | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**FVE \_ E \_ \_ VOLUME bloqueado**</dt> <dt>2150694912 (0x80310000)</dt> </dl>           | O volume está bloqueado.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**FVE \_ E \_ não \_ ativado**</dt> <dt>2150694920 (0x80310008)</dt> </dl>           | O BitLocker não está habilitado no volume. Adicione um protetor de chave para habilitar o BitLocker. <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**FVE \_ O \_ protetor E \_ não \_ foi encontrado**</dt> <dt>2150694963 (0x80310033)</dt> </dl>    | O protetor de chave fornecido não existe no volume.<br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <dt>**FVE \_ E \_ \_ \_ tipo de protetor inválido**</dt> <dt>2150694970 (0x8031003A)</dt> </dl> | O parâmetro *VolumeKeyProtectorID* não se refere a um protetor de chave do tipo "senha numérica" ou "chave externa". Use o método [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) para criar um protetor de chave do tipo apropriado.<br/> |



 

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

 

 
