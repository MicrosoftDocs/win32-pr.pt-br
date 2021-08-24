---
title: Método EnableCentralCAP da Win32_TSGatewayServerSettings classe
description: Controla a propriedade CentralCAPEnabled, que controla as políticas Serviços de Área de Trabalho Remota de autorização de conexão (RD \ 160; CAPs) para o servidor Área de Trabalho Remota Gateway de RD.
ms.assetid: 43e476df-714d-43bd-b40f-33511b7757a4
ms.tgt_platform: multiple
keywords:
- Método EnableCentralCAP Serviços de Área de Trabalho Remota
- Método EnableCentralCAP Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , método EnableCentralCAP
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableCentralCAP
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53bc180d2f4636ed2fd8d7b32d819a9d953416e4022b5cf4c18a900b15776fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119574756"
---
# <a name="enablecentralcap-method-of-the-win32_tsgatewayserversettings-class"></a>Método EnableCentralCAP da classe \_ Win32 TSGatewayServerSettings

Controla a **propriedade CentralCAPEnabled,** que controla as políticas Serviços de Área de Trabalho Remota de autorização de conexão (CAPs) para o servidor Área de Trabalho Remota Gateway de Área de Trabalho (Gateway de Área de Trabalho).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableCentralCAP(
  [in] boolean CentralCAPEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CentralCAPEnabled* \[ Em\]
</dt> <dd>

Se definido como **True,** os CAPs de área de trabalho RD CAP servidores centrais serão usados. Se definido como **False,** somente as políticas do servidor local serão usadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

