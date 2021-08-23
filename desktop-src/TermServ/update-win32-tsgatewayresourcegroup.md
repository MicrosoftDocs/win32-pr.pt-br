---
title: Método update da classe Win32_TSGatewayResourceGroup dados
description: Atualiza o grupo de recursos.
ms.assetid: b5927046-f461-41cd-861b-0fd77f2008e5
ms.tgt_platform: multiple
keywords:
- Atualizar o método Serviços de Área de Trabalho Remota
- Atualizar a Serviços de Área de Trabalho Remota , Win32_TSGatewayResourceGroup classe
- Win32_TSGatewayResourceGroup classe Serviços de Área de Trabalho Remota , método Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0c2f32e7f0c06f67ad0d32a7754c701097320564c5c01de3c348b9935b8b702
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423906"
---
# <a name="update-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método update da classe \_ Win32 TSGatewayResourceGroup

Atualiza o grupo de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Update(
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

Se vários recursos estão no *parâmetro Resources* e um dos recursos não pode ser processado, nenhum dos recursos será processado.

Você deve ser um membro do grupo Administradores para chamar esse método.

Managed Object Format arquivos (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

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

 

