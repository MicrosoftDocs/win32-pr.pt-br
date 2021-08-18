---
title: Método ExplicitLogon da classe Win32_TSLogonSetting dados
description: O método ExplicitLogon define as credenciais a usar para autenticação.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Método ExplicitLogon Serviços de Área de Trabalho Remota
- Método ExplicitLogon Serviços de Área de Trabalho Remota , Win32_TSLogonSetting classe
- Win32_TSLogonSetting classe Serviços de Área de Trabalho Remota , método ExplicitLogon
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
ms.openlocfilehash: 7303f06967d26276c7b43e06109cd9b37d664b960946afdffbb4f6a5a7c18821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137779"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Método ExplicitLogon da classe \_ Win32 TSLogonSetting

O **método ExplicitLogon** define as credenciais a usar para autenticação.

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

*UserName* \[ Em\]
</dt> <dd>

A credencial de logon de nome de usuário.

</dd> <dt>

*Domínio* \[ Em\]
</dt> <dd>

A credencial de logon do domínio.

</dd> <dt>

*Senha* \[ Em\]
</dt> <dd>

A credencial de logon de senha.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

