---
title: Criar método da classe Win32_TSGatewayResourceGroup classe
description: Cria um grupo de recursos.
ms.assetid: 715e6086-1c7d-4b20-983a-3ab98e875ca5
ms.tgt_platform: multiple
keywords:
- Criar método Serviços de Área de Trabalho Remota
- Criar método Serviços de Área de Trabalho Remota , Win32_TSGatewayResourceGroup classe
- Win32_TSGatewayResourceGroup classe Serviços de Área de Trabalho Remota , criar método
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Create
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e4de66eff704ab5d061dcb7675c1ab4ef9d847e5e7235e872f5872b8f3376fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871746"
---
# <a name="create-method-of-the-win32_tsgatewayresourcegroup-class"></a>Criar método da classe \_ Win32 TSGatewayResourceGroup

Cria um grupo de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Create(
  [in] string Name,
  [in] string Description,
  [in] string Resources
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ Em\]
</dt> <dd>

Nome do grupo de recursos.

</dd> <dt>

*Descrição* \[ Em\]
</dt> <dd>

Descrição do grupo de recursos.

</dd> <dt>

*Recursos* \[ Em\]
</dt> <dd>

Lista de recursos separados por ponto e vírgula neste grupo de recursos. Um " \* " significa todos os recursos.

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

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

