---
description: Gerencia as coleções no host do Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663487"
---
# <a name="msvm_collectionmanagementservice-class"></a>\_Classe Msvm CollectionManagementService

Gerencia as coleções no host do Hyper-V.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CollectionManagementService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **Msvm \_ CollectionManagementService** tem esses métodos.



| Método                                                                          | Descrição                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddMember**](msvm-collectionmanagementservice-addmember.md)                 | Adiciona o Managedelement especificado como um membro do objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.<br/>                                                                                           |
| [**Definocollection**](msvm-collectionmanagementservice-definecollection.md)   | Cria um novo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .<br/>                                                                                                                                        |
| [**Destruicollection**](msvm-collectionmanagementservice-destroycollection.md) | Exclui o objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.<br/>                                                                                                                                    |
| [**RemoveMember**](msvm-collectionmanagementservice-removemember.md)           | Remove o Managedelement especificado como um membro do objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.<br/>                                                                                        |
| [**RemoveMemberById**](msvm-collectionmanagementservice-removememberbyid.md)   | Remove o Managedelement especificado como um membro do [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) com o identificador fornecido. Isso terá sucesso mesmo se o objeto com esse identificador não estiver presente.<br/> |
| [**Renomecollection**](msvm-collectionmanagementservice-renamecollection.md)   | Atualiza o ElementName do objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) fornecido.<br/>                                                                                                                    |
| [**StartService**](msvm-collectionmanagementservice-startservice.md)           | Inicia o serviço.<br/>                                                                                                                                                                                                |
| [**StopService**](msvm-collectionmanagementservice-stopservice.md)             | Interrompe o serviço.<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

 




