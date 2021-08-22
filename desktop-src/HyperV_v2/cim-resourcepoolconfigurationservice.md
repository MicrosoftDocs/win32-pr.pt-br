---
description: Gerencia a configuração de pools de recursos usando trabalhos.
ms.assetid: cc0f0236-2335-4dd9-9132-51b3e6b9fcf4
title: CIM_ResourcePoolConfigurationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6a289c21f4a741778bb88a154f5923cf844f0c78390c50b558d40a5bcc32aff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647661"
---
# <a name="cim_resourcepoolconfigurationservice-class"></a>Classe CIM \_ ResourcePoolConfigurationService

Gerencia a configuração de pools de recursos usando trabalhos.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ResourcePoolConfigurationService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe CIM \_ ResourcePoolConfigurationService** tem esses métodos.



| Método                                                                                                          | Descrição                                                                   |
|:----------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**AddResourcesToResourcePool**](cim-resourcepoolconfigurationservice-addresourcestoresourcepool.md)           | Inicia um trabalho para adicionar recursos a um pool de recursos.<br/>                  |
| [**ChangeParentResourcePool**](cim-resourcepoolconfigurationservice-changeparentresourcepool.md)               | Inicie um trabalho para alterar o pool de recursos pai de um pool de recursos.<br/> |
| [**CreateChildResourcePool**](cim-resourcepoolconfigurationservice-createchildresourcepool.md)                 | Inicie um trabalho para criar um pool de recursos de um pool de recursos pai.<br/> |
| [**CreateResourcePool**](cim-resourcepoolconfigurationservice-createresourcepool.md)                           | Inicia um trabalho para criar um pool de recursos raiz.<br/>                       |
| [**DeleteResourcePool**](cim-resourcepoolconfigurationservice-deleteresourcepool.md)                           | Inicie um trabalho para excluir um pool de recursos.<br/>                             |
| [**RemoveResourcesFromResourcePool**](cim-resourcepoolconfigurationservice-removeresourcesfromresourcepool.md) | Inicia um trabalho para remover recursos de um pool de recursos.<br/>             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ CIM**](cim-service.md)
</dt> </dl>

 

 




