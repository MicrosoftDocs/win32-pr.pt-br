---
title: Método GetGracePeriodDays da classe Win32_TerminalServiceSetting
description: Recupera o número de dias restantes no período de carência Serviços de Área de Trabalho Remota licenciamento para um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Um valor zero indica que o período de carência terminou.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Método GetGracePeriodDays Serviços de Área de Trabalho Remota
- Método GetGracePeriodDays Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método GetGracePeriodDays
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetGracePeriodDays
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbfe1a99fb0b4f12db19f018d8acb3aaee6ab15a3560cd9140c3a05f36986585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010116"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Método GetGracePeriodDays da classe Win32 \_ TerminalServiceSetting

Recupera o número de dias restantes no período de carência Serviços de Área de Trabalho Remota licenciamento para um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Um valor zero indica que o período de carência terminou.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DaysLeft* \[ out\]
</dt> <dd>

O número de dias restantes no período de carência.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para se conectar ao \\ \\ namespace raiz CIMV2 \\ TerminalServices, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Para Visual Basic e script de chamadas, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



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

 

