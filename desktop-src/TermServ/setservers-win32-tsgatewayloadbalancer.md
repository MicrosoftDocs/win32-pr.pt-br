---
title: Método SetServers da classe Win32_TSGatewayLoadBalancer
description: Define a propriedade Servers com a lista de servidores de balanceamento de carga Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Método SetServers Serviços de Área de Trabalho Remota
- Método SetServers Serviços de Área de Trabalho Remota , Win32_TSGatewayLoadBalancer classe
- Win32_TSGatewayLoadBalancer classe Serviços de Área de Trabalho Remota , método SetServers
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.SetServers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c23ac6cf965687a022c5ae5ba8c1ce690c39c45f9149076f36ab13bc2d222
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349612"
---
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Método SetServers da classe \_ Win32 TSGatewayLoadBalancer

Define a **propriedade Servers** com a lista de servidores de balanceamento de carga Área de Trabalho Remota Gateway de Área de Trabalho Remota (Gateway de RD).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Servidores* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula de servidores de balanceamento de carga do Gateway de RD.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="remarks"></a>Comentários

Se vários servidores estão no parâmetro *Servers* e um dos servidores não pode ser processado, nenhum dos servidores será processado.

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

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

