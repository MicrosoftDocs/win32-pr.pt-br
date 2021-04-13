---
title: Método ExplicitLogon da classe Win32_TSLogonSetting
description: O método ExplicitLogon define as credenciais a serem usadas para autenticação.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ExplicitLogon
- Método ExplicitLogon Serviços de Área de Trabalho Remota, classe Win32_TSLogonSetting
- Classe Win32_TSLogonSetting Serviços de Área de Trabalho Remota, método ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369766"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Método ExplicitLogon da classe Win32 \_ TSLogonSetting

O método **ExplicitLogon** define as credenciais a serem usadas para autenticação.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome de usuário* \[ no\]
</dt> <dd>

A credencial de logon do nome de usuário.

</dd> <dt>

*Domínio* \[ do no\]
</dt> <dd>

A credencial de logon de domínio.

</dd> <dt>

*Senha* \[ do no\]
</dt> <dd>

A credencial de logon de senha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna êxito em caso de êxito, caso contrário retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLogonSetting Win32**](win32-tslogonsetting.md)
</dt> </dl>

 

