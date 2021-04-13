---
title: Método addaccount da classe Win32_TSPermissionsSetting (Faxcomex. h)
description: O método addaccount se prepara para adicionar uma conta ao terminal com o conjunto de permissões especificado. Você pode adicionar usuários, grupos ou computadores.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Método addaccount Serviços de Área de Trabalho Remota
- Método addaccount Serviços de Área de Trabalho Remota, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Serviços de Área de Trabalho Remota, método addaccount
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
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455473"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Método addaccount da classe Win32 \_ TSPermissionsSetting

O método **addaccount** se prepara para adicionar uma conta ao terminal com o conjunto de permissões especificado. Você pode adicionar usuários, grupos ou computadores.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AccountName* \[ no\]
</dt> <dd>

O nome da conta a ser adicionada ao terminal.

</dd> <dt>

*PermissionPreSet* \[ no\]
</dt> <dd>

O conjunto de permissões a ser associado à conta especificada. Esse parâmetro pode ser qualquer um ou todos os valores a seguir. Para obter mais informações, consulte [serviços de área de trabalho remota permissões](terminal-services-permissions.md).

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ \_Acesso de convidado** (0)


</dt> <dd>

A conta tem permissão de logon.

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ \_Acesso do usuário** (1)


</dt> <dd>

A conta tem as seguintes permissões: logon, informações de consulta, enviar mensagem e conectar.

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ Todos os \_ acessos** (2)


</dt> <dd>

A conta tem todas as permissões de Serviços de Área de Trabalho Remota.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| parâmetro<br/>                   | <dl> <dt>Faxcomex. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSPermissionsSetting Win32**](win32-tspermissionssetting.md)
</dt> </dl>

 

