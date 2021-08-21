---
description: Altera o valor de autorização do proprietário do TPM.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Método ChangeOwnerAuth da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 02ca13049df20c57eeb5cc594bde1b247df0eb3829c757b64b8bd31f87e3796b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004674"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a>Método ChangeOwnerAuth da classe Win32 \_ TPM

O método **ChangeOwnerAuth** da classe [**Win32 \_ TPM**](win32-tpm.md) altera o valor de autorização do proprietário do TPM.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldOwnerAuth* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que nomeia o valor atual de autorização do proprietário do TPM do dispositivo. Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma senha para esse valor de autorização. O parâmetro *OldOwnerAuth* não é fornecido ou uma cadeia de caracteres vazia é fornecida, esse método obtém o valor do registro, se presente.

</dd> <dt>

*NewOwnerAuth* \[ em, opcional\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres que nomeia o novo valor de autorização de proprietário do TPM. Use o método [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) para converter uma senha para esse valor de autorização. O parâmetro *NewOwnerAuth* não pode ser vazio ou **nulo.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                              | O método foi bem-sucedido.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt> </dl>                   | O valor de autorização do proprietário do TPM atual está incorreto.<br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <dt>**TPM \_ E \_ defender \_ bloqueio \_ em execução**</dt> <dt>2150107139 (0x80280803)</dt> </dl>      | O TPM está se defendendo contra ataques de dicionário e está em um período de tempo limite. Para obter mais informações, consulte o método [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .<br/>                                                                                                                                                                                                             |
| <dl> <dt>**FVE \_ E \_ ad \_ Schema \_ não \_ instalado**</dt> <dt>2150694922 (0x8031000A)</dt> </dl> | Não é possível salvar informações de recuperação na rede. O computador foi configurado para armazenar informações de recuperação para Active Directory Domain Services. Para obter instruções sobre como configurar Active Directory, consulte [criptografia de unidade de disco BitLocker guia de configuração: fazendo backup de informações de recuperação do TPM e do BitLocker para Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).<br/> |
| <dl> <dt>**Falha na conexão**</dt> <dt>2147943755 (0x8007054B)</dt> </dl>                  | Não é possível salvar informações de recuperação na rede. O computador foi configurado para armazenar informações de recuperação para Active Directory Domain Services. Uma conexão de rede é necessária para continuar.<br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

O método **ChangeOwnerAuth** faz backup da nova autorização de proprietário do TPM para Active Directory Domain Services se as configurações de política de grupo apropriadas foram configuradas.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
