---
description: Redefine o valor de autorização da chave raiz de armazenamento (SRK) como compatível com o sistema operacional.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Método ResetSrkAuth da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297431"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a>Método ResetSrkAuth da classe Win32 \_ TPM

O método **ResetSrkAuth** da classe [**Win32 \_ TPM**](win32-tpm.md) redefine o valor de autorização da chave de raiz de armazenamento (SRK) para ser compatível com o sistema operacional.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ResetSrkAuth(
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



| Código/valor de retorno                                                                                                                                                                         | Descrição                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                         | O método foi bem-sucedido.<br/>                                                                                                                                                |
| <dl> <dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>             | O valor de autorização do proprietário fornecido não pode atender à solicitação.<br/>                                                                                                        |
| <dl> <dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt> </dl> | O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite. Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/> |



 

## <a name="remarks"></a>Comentários

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

 

 
