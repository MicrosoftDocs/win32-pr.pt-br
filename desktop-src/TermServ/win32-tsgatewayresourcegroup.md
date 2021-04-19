---
title: Classe Win32_TSGatewayResourceGroup
description: Descreve um grupo de recursos, que mapeia um conjunto de recursos (nomes de computador) para uma única entidade.
ms.assetid: 5715a2ea-9bbc-4704-835e-ba6d93a72368
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSGatewayResourceGroup classe, descrita
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
ms.openlocfilehash: 9ffeda42abafd24526360f5e549f004cae0c3140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810968"
---
# <a name="win32_tsgatewayresourcegroup-class"></a>\_Classe Win32 TSGatewayResourceGroup

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

A classe **Win32 \_ TSGatewayResourceGroup** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSGatewayResourceGroup** tem esses métodos.



| Método                                                                  | Descrição                                                                           |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Addresources**](addresources-win32-tsgatewayresourcegroup.md)       | Adiciona recursos à propriedade **Resources** para este grupo de recursos.<br/>      |
| [**Criar**](create-win32-tsgatewayresourcegroup.md)                   | Cria um grupo de recursos.<br/>                                                  |
| [**Apagar**](delete-win32-tsgatewayresourcegroup.md)                   | Exclui este grupo de recursos.<br/>                                               |
| [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md) | Exclui recursos da propriedade **Resources** para este grupo de recursos.<br/> |
| [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md)   | Define a propriedade **Description** para esse grupo de recursos.<br/>                 |
| [**SetName**](setname-win32-tsgatewayresourcegroup.md)                 | Define a propriedade **Name** para esse grupo de recursos.<br/>                        |
| [**Recursos**](setresources-win32-tsgatewayresourcegroup.md)       | Define a propriedade **Resources** para esse grupo de recursos.<br/>                   |
| [**Cumulativo**](update-win32-tsgatewayresourcegroup.md)                   | Atualiza este grupo de recursos.<br/>                                               |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSGatewayResourceGroup** tem essas propriedades.

<dl> <dt>

**AssociatedRAPs**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista separada por ponto-e-vírgula de Serviços de Área de Trabalho Remota RD RAPs (políticas de autorização de recursos) que estão associadas a esse grupo de recursos.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do grupo de recursos. Essa propriedade pode ser alterada com o método [**SetDescription**](setdescription-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do grupo de recursos. Essa propriedade pode ser alterada com o método [**SetName**](setname-win32-tsgatewayresourcegroup.md) .

</dd> <dt>

**Recursos**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Lista de recursos separados por ponto e vírgula neste grupo de recursos. Um " \* " significa todos os recursos. Essa propriedade pode ser alterada com os métodos [**Setresources**](setresources-win32-tsgatewayresourcegroup.md), [**addresources**](addresources-win32-tsgatewayresourcegroup.md), [**RemoveResources**](removeresources-win32-tsgatewayresourcegroup.md)e [**Update**](update-win32-tsgatewayresourcegroup.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para usar essa classe.

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

[**\_TSGatewayConnection Win32**](win32-tsgatewayconnection.md)
</dt> <dt>

[**\_TSGatewayConnectionAuthorizationPolicy Win32**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayLoadBalancer Win32**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**\_TSGatewayRADIUSServer Win32**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**\_TSGatewayResourceAuthorizationPolicy Win32**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**\_TSGatewayServerSettings Win32**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

