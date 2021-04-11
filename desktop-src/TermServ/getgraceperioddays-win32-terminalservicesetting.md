---
title: Método GetGracePeriodDays da classe Win32_TerminalServiceSetting
description: Recupera o número de dias restantes no período de carência de licenciamento Serviços de Área de Trabalho Remota para um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Um valor zero indica que o período de carência está acima.
ms.assetid: d84d7815-ee09-43d9-a370-993d23f14898
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetGracePeriodDays
- Método GetGracePeriodDays Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método GetGracePeriodDays
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
ms.openlocfilehash: 0faaf525bb74a8ac4b0164c181e5a20cfb215d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294779"
---
# <a name="getgraceperioddays-method-of-the-win32_terminalservicesetting-class"></a>Método GetGracePeriodDays da classe Win32 \_ TerminalServiceSetting

Recupera o número de dias restantes no período de carência de licenciamento Serviços de Área de Trabalho Remota para um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD). Um valor zero indica que o período de carência está acima.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetGracePeriodDays(
  [out] uint32 DaysLeft
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DaysLeft* \[ fora\]
</dt> <dd>

O número de dias restantes no período de carência.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6. O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



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

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

