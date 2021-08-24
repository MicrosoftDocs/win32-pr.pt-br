---
title: Método PingLicenseServer da classe Win32_TerminalServiceSetting dados
description: PingLicenseServer não está mais disponível.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Método PingLicenseServer Serviços de Área de Trabalho Remota
- Método PingLicenseServer Serviços de Área de Trabalho Remota , Win32_TerminalServiceSetting classe
- Win32_TerminalServiceSetting classe Serviços de Área de Trabalho Remota , método PingLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5a52268073a076c5dada44b7f34c6a6b3e0c820c0b9819f65d23081f4f6c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866096"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método PingLicenseServer da classe Win32 \_ TerminalServiceSetting

\[**PingLicenseServer** não está mais disponível para uso a partir Windows Server 2008 R2.\]

**Windows Server 2008:** Pinga o servidor de licença para determinar se ele é um servidor de licença válido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServerName* \[ Em\]
</dt> <dd>

Nome do servidor de licença.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

<dl> <dt>

**S \_ OK**
</dt> <dd>

O servidor é um servidor de licença válido.

</dd> <dt>

**S \_ FALSE**
</dt> <dd>

O servidor de licença não é válido.

</dd> </dl>

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

 

