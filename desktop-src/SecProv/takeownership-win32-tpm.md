---
description: Instala um proprietário para o TPM.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Método TakeOwnership da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011668"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a>Método TakeOwnership da classe Win32 \_ TPM

O método **TakeOwnership** da classe [**Win32 \_ TPM**](win32-tpm.md) instala um proprietário para o TPM. O proprietário do TPM pode fazer uso total dos recursos do TPM. Depois que um proprietário é definido, nenhum outro usuário ou software pode reivindicar a propriedade do TPM.

Os métodos [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)e [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devem ser verdadeiros para que o método **TakeOwnership** possa ser bem sucedido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OwnerAuth* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que identifica o proprietário do TPM. Essa cadeia de caracteres deve ser uma cadeia de caracteres terminada em NULL codificada em base64 que contenha exatamente 20 bytes de dados binários. Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma frase secreta nesse formato esperado. O parâmetro *OwnerAuth* será lido no registro se nenhum for fornecido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                                                         | Descrição                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | O método foi bem-sucedido.<br/>                                                                                                                                                                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt> </dl>                 | O parâmetro *OwnerAuth* não é válido.<br/>                                                                                                                                                                 |
| <dl> <dt>**TPM \_ \_ \_ Conjunto de proprietário E**</dt> <dt>2150105108 (0x80280014)</dt> </dl>            | Já existe um proprietário no TPM.<br/>                                                                                                                                                                     |
| <dl> <dt>**TPM \_ E \_ sem \_ endosso**</dt> <dt>2150105123 (0x80280023)</dt> </dl>       | Nenhuma chave de endosso pode ser encontrada no TPM.<br/> Para criar um par de chaves de endosso no TPM, consulte o método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .<br/>             |
| <dl> <dt>**TPM \_ E \_ instalação \_ desabilitada**</dt> <dt>2150105099 (0x8028000B)</dt> </dl>     | Não é possível instalar um proprietário neste TPM.<br/> Para obter informações sobre como permitir a instalação de um proprietário de dispositivo, consulte [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).<br/> |
| <dl> <dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite. Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                               |



 

## <a name="remarks"></a>Comentários

Os métodos [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)e [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) devem ser verdadeiros para que **TakeOwnership** possa ter sucesso.

Você deve usar o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para alterar uma frase secreta no valor de entrada usado para o parâmetro *OwnerAuth* .

O método **TakeOwnership** faz backup do valor de autorização do proprietário para Active Directory se as configurações de política de grupo apropriadas foram configuradas.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
