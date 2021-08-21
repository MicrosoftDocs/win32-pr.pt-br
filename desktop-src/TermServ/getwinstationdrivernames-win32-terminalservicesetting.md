---
title: Método GetWinstationDriverNames da classe Win32_TerminalServiceSetting dados
description: Recupera uma lista de nomes de driver do Winstation.
ms.assetid: 578c2a07-17e7-4bd6-b520-942cd48ee40f
ms.tgt_platform: multiple
keywords:
- Método GetWinstationDriverNames Serviços de Área de Trabalho Remota
- Método GetWinstationDriverNames Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método GetWinstationDriverNames
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetWinstationDriverNames
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d51d31e6a9857dd1ec1faf46df2adadc4379c0ccf99a7a5ed634a4fa27bf4d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059474"
---
# <a name="getwinstationdrivernames-method-of-the-win32_terminalservicesetting-class"></a>Método GetWinstationDriverNames da classe Win32 \_ TerminalServiceSetting

Recupera uma lista de nomes de driver do Winstation.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetWinstationDriverNames(
  [out] string WinstaDriverNames[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*WinstaDriverNames* \[ out\]
</dt> <dd>

A lista de nomes de driver do Winstation.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para se conectar ao \\ \\ namespace raiz CIMV2 \\ TerminalServices, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Para Visual Basic e chamadas de script, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


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

 

