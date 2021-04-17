---
title: Método ModifyPermissions da classe Win32_TSAccount
description: Define uma permissão para a conta especificada.
ms.assetid: cef36f7f-d327-4bb6-9bff-282036c1a5d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ModifyPermissions
- Método ModifyPermissions Serviços de Área de Trabalho Remota, classe Win32_TSAccount
- Classe Win32_TSAccount Serviços de Área de Trabalho Remota, método ModifyPermissions
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4bf6147c215475314f65bb8fa426442884bc82e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811904"
---
# <a name="modifypermissions-method-of-the-win32_tsaccount-class"></a>Método ModifyPermissions da classe Win32 \_ TSAccount

Define uma permissão para a conta especificada.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ModifyPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Allow
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PermissionMask* \[ no\]
</dt> <dd>

A [permissão host da sessão da área de trabalho remota](terminal-services-permissions.md) a ser definida.

Os valores possíveis são:

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_ CONSULTA** (0)


</dt> <dd>

Permissão para consultar informações sobre uma sessão.

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_ DEFINIR** (1)


</dt> <dd>

Permissão para modificar os parâmetros de conexão.

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_ REDEFINIR** (6)


</dt> <dd>

Permissão para redefinir ou encerrar uma sessão ou conexão.

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_ \| Direitos padrão \_ virtuais \_ necessários** (3)


</dt> <dd>

Permissão para usar canais virtuais. Os canais virtuais fornecem acesso de um programa de servidor a dispositivos cliente.

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_ SOMBRA** (4)


</dt> <dd>

Permissão para sombrear ou controlar remotamente a sessão de outro usuário.

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_ LOGON** (5)


</dt> <dd>

Permissão para fazer logon em uma sessão no servidor.

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_ LOGOFF** (2)


</dt> <dd>

Permissão para fazer logoff de um usuário de uma sessão.

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_ MSG** (7)


</dt> <dd>

Permissão para enviar uma mensagem para a sessão de outro usuário.

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_ CONECTAR** (8)


</dt> <dd>

Permissão para se conectar a outra sessão.

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_ Desconectar** (9)


</dt> <dd>

Permissão para desconectar uma sessão.

</dd> </dl> </dd> <dt>

*Permitir* \[ no\]
</dt> <dd>

Especifica se a permissão no parâmetro *PermissionMask* é permitida ou negada.

Os valores possíveis são:

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

O conjunto de permissões especificado é permitido.

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

O conjunto de permissões especificado foi negado.

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
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSAccount Win32**](win32-tsaccount.md)
</dt> </dl>

 

