---
description: Protege a chave de criptografia do volume usando um SID (identificador de segurança Active Directory).
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Método ProtectKeyWithAdSid da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784130"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a>Método ProtectKeyWithAdSid da classe Win32 \_ EncryptableVolume

O método **ProtectKeyWithAdSid** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) protege a chave de criptografia do volume usando um SID (identificador de segurança) Active Directory.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyName* \[ em, opcional\]
</dt> <dd>

Uma cadeia de caracteres que especifica um identificador atribuído pelo usuário para esse protetor de chave. Se esse parâmetro não for especificado, um valor em branco será usado.

</dd> <dt>

*SidString* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém o Active Directory SID usado para proteger a chave de criptografia.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Sinalizadores que alteram o comportamento da função. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <dt>**FVE \_ \_Sinalizador DPAPI \_ ng \_ None**</dt> <dt>0x0000</dt> </dl>                                                                   | Nenhum efeito.<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <dt>**FVE \_ \_Desbloqueio \_ de sinalizador DPAPI ng \_ \_ como \_ \_ conta de serviço**</dt> <dt>0x0001</dt> </dl> | Especifica que o protetor baseado em SID foi protegido a uma conta de serviço. Se esse sinalizador for especificado, o chamador deverá garantir que ele esteja sendo executado como a conta de serviço apropriada antes de chamar [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (descartando a representação temporariamente, por exemplo).<br/> |



 

</dd> <dt>

*VolumeKeyProtectorID* \[ fora\]
</dt> <dd>

Um identificador exclusivo associado ao protetor criado. Você pode usar essa cadeia de caracteres para gerenciar o protetor de chave.

Se a unidade oferecer suporte à criptografia de hardware e o BitLocker não tiver usado a propriedade Band, a cadeia de caracteres de ID será definida como "BitLocker" e o protetor de chave será gravado nos metadados por banda.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md)

Por padrão, você não pode adicionar uma conta de Active Directory ou um protetor de grupo remotamente. Você deve habilitar a delegação restrita no controlador de domínio e no computador de origem. No controlador de domínio, execute as seguintes etapas:

1.  Abra o gerenciador de servidor.
2.  Selecionar computadores em funções de Active Directory
3.  Selecione o computador cliente de destino e clique com o botão direito do mouse
4.  Selecione a guia Delegação
5.  Selecione o botão de opção "confiar neste computador para delegação a serviços especificados"
6.  Selecione o botão de opção "usar somente Kerberos"
7.  Clique em Adicionar
8.  Selecione "usuários ou computadores"
9.  Selecione host/como o nome da entidade de serviço

Execute as etapas 3 a 9 no computador de origem.

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

 

 
