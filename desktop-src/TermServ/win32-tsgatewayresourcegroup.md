---
title: Win32_TSGatewayResourceGroup classe
description: Descreve um grupo de recursos, que mapeia um conjunto de recursos (nomes de computador) para uma única entidade.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayResourceGroup classe Serviços de Área de Trabalho Remota
- Win32_TSGatewayResourceGroup classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup
- Win32_TSGatewayResourceGroup.Name
- Win32_TSGatewayResourceGroup.Description
- Win32_TSGatewayResourceGroup.AssociatedRAPs
- Win32_TSGatewayResourceGroup.Resources
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ba4ec4545502d82a3449cee39954deb9b5b2e68bf7c657423e673c582d1c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603878"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>Classe Win32 \_ TSGatewayResourceGroup

Descreve um grupo de recursos, que mapeia um conjunto de recursos (nomes de computador) para uma única entidade.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayResourceGroup
{
  string Name;
  string Description;
  string AssociatedRAPs;
  string Resources;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSGatewayResourceGroup** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Win32 TSGatewayResourceGroup** tem esses métodos.



| Método                                                                  | Descrição                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**AddResources**](addresources-win32-tsgatewayresourcegroup.md)       | Adiciona recursos à propriedade **Recursos** para esse grupo de recursos.<br/>      |
| [**Criar**](create-win32-tsgatewayresourcegroup.md)                   | Cria um grupo de recursos.<br/>                                                  |
| [**Excluir**](delete-win32-tsgatewayresourcegroup.md)                   | Exclui esse grupo de recursos.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Exclui recursos da propriedade **Recursos** para esse grupo de recursos.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Define a **propriedade Description** para este grupo de recursos.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Define a **propriedade Name** para este grupo de recursos.<br/>                        |
| [**SetResources**](setresources-win32-tsgatewayresourcegroup.md)       | Define a **propriedade Recursos** para esse grupo de recursos.<br/>                   |
| [**Atualização**](update-win32-tsgatewayresourcegroup.md)                   | Atualiza esse grupo de recursos.<br/>                                               |



 

### <a name="properties"></a>Propriedades

A **classe \_ Win32 TSGatewayResourceGroup** tem essas propriedades.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista separada por ponto e vírgula de Serviços de Área de Trabalho Remota raps de autorização de recursos (RAPs de RD) que estão associadas a esse grupo de recursos.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do grupo de recursos. Essa propriedade pode ser alterada com o [**método SetDescription.**](setdescription-win32-tsgatewayresourcegroup.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do grupo de recursos. Essa propriedade pode ser alterada com o [**método SetName.**](setname-win32-tsgatewayresourcegroup.md)

</dd> <dt>

**Recursos**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de recursos separados por ponto e vírgula neste grupo de recursos. Um " \* " significa todos os recursos. Essa propriedade pode ser alterada com os métodos [**SetResources,**](setresources-win32-tsgatewayresourcegroup.md) [**AddResources,**](addresources-win32-tsgatewayresourcegroup.md) [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)e [**Update.**](update-win32-tsgatewayresourcegroup.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

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

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

