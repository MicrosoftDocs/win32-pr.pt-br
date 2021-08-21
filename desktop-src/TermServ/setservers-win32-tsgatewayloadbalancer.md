---
title: Método setservers da classe Win32_TSGatewayLoadBalancer
description: Define a propriedade Servers com a lista de servidores de balanceamento de carga do gateway de Área de Trabalho Remota (gateway de área de trabalho remota).
ms.assetid: c82de8e2-301b-465d-b375-038b8a480cde
ms.tgt_platform: multiple
keywords:
- Método setservers Serviços de Área de Trabalho Remota
- Método setservers Serviços de Área de Trabalho Remota, classe Win32_TSGatewayLoadBalancer
- Classe Win32_TSGatewayLoadBalancer Serviços de Área de Trabalho Remota, método setservers
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
# <a name="setservers-method-of-the-win32_tsgatewayloadbalancer-class"></a>Método setservers da classe Win32 \_ TSGatewayLoadBalancer

Define a propriedade **Servers** com a lista de servidores de balanceamento de carga do gateway de área de trabalho remota (gateway de área de trabalho remota).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetServers(
  [in] string Servers
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Servidores* \[ do no\]
</dt> <dd>

Lista separada por ponto e vírgula dos servidores de balanceamento de carga do gateway de área de trabalho remota.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários servidores estiverem no parâmetro *servidores* e um dos servidores não puder ser processado, nenhum dos servidores será processado.

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 

