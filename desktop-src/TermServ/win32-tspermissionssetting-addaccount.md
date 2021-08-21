---
title: Método AddAccount da classe Win32_TSPermissionsSetting (Faxcomex.h)
description: O método AddAccount se prepara para adicionar uma conta ao terminal com o conjunto de permissões especificado. Você pode adicionar usuários, grupos ou computadores.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Método AddAccount Serviços de Área de Trabalho Remota
- Método AddAccount Serviços de Área de Trabalho Remota , Win32_TSPermissionsSetting classe
- Win32_TSPermissionsSetting classe Serviços de Área de Trabalho Remota , método AddAccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3bd1862dfde955d782527ca60fc0fb43ca31431ccb307574e875fe84a640655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348551"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Método AddAccount da classe \_ Win32 TSPermissionsSetting

O **método AddAccount** se prepara para adicionar uma conta ao terminal com o conjunto de permissões especificado. Você pode adicionar usuários, grupos ou computadores.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AccountName* \[ Em\]
</dt> <dd>

O nome da conta a ser acrescentada ao terminal.

</dd> <dt>

*PermissionPreSet* \[ Em\]
</dt> <dd>

O conjunto de permissões a ser associado à conta especificada. Esse parâmetro pode ser qualquer ou todos os valores a seguir. Para obter mais informações, [consulte Serviços de Área de Trabalho Remota permissões](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ ACESSO \_ DE CONVIDADO** (0)


</dt> <dd>

A conta tem permissão logon.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ ACESSO \_ DO USUÁRIO** (1)


</dt> <dd>

A conta tem as seguintes permissões: Logon, Informações de Consulta, Enviar Mensagem e Conexão.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ ALL \_ ACCESS** (2)


</dt> <dd>

A conta tem todas Serviços de Área de Trabalho Remota Permissões.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| Cabeçalho<br/>                   | <dl> <dt>Faxcomex.h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

