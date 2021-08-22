---
title: Método DeleteDirectConnectLicenseServer da classe Win32_TerminalServiceSetting
description: DeleteDirectConnectLicenseServer não está mais disponível.
ms.assetid: 190316ab-b8ed-4102-8346-42603d6451e6
ms.tgt_platform: multiple
keywords:
- Método DeleteDirectConnectLicenseServer Serviços de Área de Trabalho Remota
- Método DeleteDirectConnectLicenseServer Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método DeleteDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.DeleteDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cefd0bf27e1b285a8badb9c7fc4b33cf11f9cdac764067662a77b90021afe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999900"
---
# <a name="deletedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método DeleteDirectConnectLicenseServer da classe Win32 \_ TerminalServiceSetting

\[**DeleteDirectConnectLicenseServer** não está mais disponível para uso Windows Server 2008 R2.\]

**Windows Server 2008:** Remove um servidor de licença do Registro.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LicenseServerName* \[ Em\]
</dt> <dd>

Nome do servidor de licença a ser removido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores.

## <a name="remarks"></a>Comentários

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte ao servidor<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

