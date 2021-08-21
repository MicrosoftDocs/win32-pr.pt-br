---
title: Método FindLicenseServers da classe Win32_TerminalServiceSetting
description: Enumera todos os servidores de Área de Trabalho Remota licença e o método de descoberta.
ms.assetid: 0de2ee6f-6c56-4293-84da-131b433c6a9d
ms.tgt_platform: multiple
keywords:
- Método FindLicenseServers Serviços de Área de Trabalho Remota
- Método FindLicenseServers Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota método , FindLicenseServers
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.FindLicenseServers
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98af0d63c736e5bc82dd13d2abc94786634d7b92ba2c9a4628ae8ffd32a18b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130785"
---
# <a name="findlicenseservers-method-of-the-win32_terminalservicesetting-class"></a>Método FindLicenseServers da classe Win32 \_ TerminalServiceSetting

Enumera todos os servidores de Área de Trabalho Remota licença e o método de descoberta.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FindLicenseServers(
  [out] Win32_TSDiscoveredLicenseServer LicenseServersList[],
  [out] uint32                          Count
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LicenseServersList* \[ out\]
</dt> <dd>

A lista de [**objetos \_ Win32 TSDiscoveredLicenseServer.**](win32-tsdiscoveredlicenseserver.md) Cada objeto na lista de saída tem o nome do servidor Área de Trabalho Remota licença e o método de descoberta.

</dd> <dt>

*Contagem* \[ out\]
</dt> <dd>

O número total de servidores Área de Trabalho Remota licenças descobertas na lista de saída.

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

 

