---
title: Configurar o método da Win32_TSGatewayServerSettings classe
description: Define as configurações de IIS e RPC exigidas pelo serviço Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: 12d7264e-46aa-457f-b89d-547231573db8
ms.tgt_platform: multiple
keywords:
- Configurar o método Serviços de Área de Trabalho Remota
- Configurar a Serviços de Área de Trabalho Remota , Win32_TSGatewayServerSettings classe
- Win32_TSGatewayServerSettings classe Serviços de Área de Trabalho Remota , configurar método
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.Configure
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e246b81569f63c3a6eac9cafe043c837deca593072b622efa3f854a4a74862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515686"
---
# <a name="configure-method-of-the-win32_tsgatewayserversettings-class"></a>Configurar o método da classe \_ Win32 TSGatewayServerSettings

Define as configurações de IIS e RPC exigidas pelo serviço Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Configure();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                        |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

