---
title: Método SetAllowTSConnections da classe Win32_TerminalServiceSetting
description: O método SetAllowTSConnections permite ou nega novas conexões de área de trabalho remota. Esse método modificará a propriedade AllowTSConnections para a classe de acordo.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Método SetAllowTSConnections Serviços de Área de Trabalho Remota
- Método SetAllowTSConnections Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f8e9be06a19599f578089fa979d7fd93a7bf457fcadf033ed0ab56fea4947f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127022"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Método SetAllowTSConnections da classe Win32 \_ TerminalServiceSetting

O **método SetAllowTSConnections** permite ou nega novas conexões de área de trabalho remota. Esse método modificará a **propriedade AllowTSConnections** para a classe de acordo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AllowTSConnections* \[ Em\]
</dt> <dd>

Especifica se novas conexões de área de trabalho remota são permitidas. Esse deve ser um dos valores a seguir.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Novas conexões não são permitidas. Se o *parâmetro ModifyFirewallException* for 1, a exceção Área de Trabalho Remota firewall será desabilitada.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Novas conexões são permitidas. Se o *parâmetro ModifyFirewallException* for 1, a exceção Área de Trabalho Remota firewall será habilitada.

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[ Em\]
</dt> <dd>

Especifica se a configuração de exceção de firewall para Área de Trabalho Remota será modificada para o estado especificado pelo *parâmetro AllowTSConnections.* Esse deve ser um dos valores a seguir.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Não modifique a configuração de exceção do firewall.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Modifique a configuração de exceção do firewall.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna Êxito em caso de êxito; caso contrário, retornará um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

