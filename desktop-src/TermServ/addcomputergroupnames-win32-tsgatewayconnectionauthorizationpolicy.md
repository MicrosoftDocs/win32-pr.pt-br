---
title: Método AddComputerGroupNames da classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Adiciona os nomes de grupo de computadores especificados à propriedade ComputerGroupNames.
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AddComputerGroupNames
- Método AddComputerGroupNames Serviços de Área de Trabalho Remota, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Serviços de Área de Trabalho Remota, método AddComputerGroupNames
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085776"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Método AddComputerGroupNames da classe Win32 \_ TSGatewayConnectionAuthorizationPolicy

Adiciona os nomes de grupo de computadores especificados à propriedade **ComputerGroupNames** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerGroupNames* \[ no\]
</dt> <dd>

Lista separada por ponto e vírgula de nomes de grupos de computadores para adicionar à propriedade **ComputerGroupNames** . Os nomes de grupos de computadores devem ter o formato *Domain \\ ComputerGroupName*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários nomes de grupos de computadores estiverem no parâmetro *ComputerGroupNames* e um dos nomes não puder ser processado, nenhum dos nomes será processado.

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 

