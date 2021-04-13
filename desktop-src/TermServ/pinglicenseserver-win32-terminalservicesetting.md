---
title: Método PingLicenseServer da classe Win32_TerminalServiceSetting
description: O PingLicenseServer não está mais disponível.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método PingLicenseServer
- Método PingLicenseServer Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método PingLicenseServer
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
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369574"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método PingLicenseServer da classe Win32 \_ TerminalServiceSetting

\[O **PingLicenseServer** não está mais disponível para uso a partir do Windows Server 2008 R2.\]

**Windows Server 2008:** Executa ping no servidor de licença para determinar se ele é um servidor de licença válido.

## <a name="syntax"></a>Sintaxe


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do Server* \[ no\]
</dt> <dd>

Nome do servidor de licença.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

<dl> <dt>

**S \_ OK**
</dt> <dd>

O servidor é um servidor de licença válido.

</dd> <dt>

**\_falso**
</dt> <dd>

O servidor de licença não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Fim do suporte do cliente<br/>    | Nenhum compatível<br/>                                                               |
| Fim do suporte do servidor<br/>    | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> </dl>

 

