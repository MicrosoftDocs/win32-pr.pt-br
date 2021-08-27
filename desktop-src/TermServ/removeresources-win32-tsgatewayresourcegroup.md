---
title: Método RemoveResources da classe Win32_TSGatewayResourceGroup
description: Remove recursos do grupo de recursos.
ms.assetid: 5f339990-8273-4658-843e-b6b7a85808e1
ms.tgt_platform: multiple
keywords:
- Método RemoveResources Serviços de Área de Trabalho Remota
- Método RemoveResources Serviços de Área de Trabalho Remota , Win32_TSGatewayResourceGroup classe
- Win32_TSGatewayResourceGroup classe Serviços de Área de Trabalho Remota , método RemoveResources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.RemoveResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e852f2994c3302e4e53f316496b023c9e8fc115508ff522f384aa4701d2050ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127511"
---
# <a name="removeresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método RemoveResources da classe \_ Win32 TSGatewayResourceGroup

Remove recursos do grupo de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recursos* \[ Em\]
</dt> <dd>

Lista separada por ponto e vírgula dos recursos a serem removidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários recursos estão no *parâmetro Resources* e um dos recursos não pode ser processado, nenhum dos recursos será processado.

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

 

