---
description: Essa classe foi preterida. Em vez disso, recomendamos derivar da \_ classe de serviço CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: Classe CIM_NetworkService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkService
- CIM_NetworkService.Keywords
- CIM_NetworkService.ServiceURL
- CIM_NetworkService.StartupConditions
- CIM_NetworkService.StartupParameters
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b141e6e38f2fafefdf6e75670b975e0fcdd2961c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760865"
---
# <a name="cim_networkservice-class"></a>Classe do CIM \_ NetworkService

Essa classe foi preterida. Em vez disso, recomendamos derivar da classe de [**\_ serviço CIM**](cim-service.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Deprecated("CIM_Service"), Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_NetworkService : CIM_Service
{
  string Keywords[];
  string ServiceURL;
  string StartupConditions[];
  string StartupParameters[];
};
```

## <a name="members"></a>Membros

A classe do **CIM \_ NetworkService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe do **CIM \_ NetworkService** tem essas propriedades.

<dl> <dt>

**Palavras-chave**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")
</dt> </dl>

Essa propriedade foi preterida e não deve ser usada.

> [!Note]  
> Descrição preterida: uma matriz de palavras-chave que pode ser usada em consultas.

 

</dd> <dt>

**ServiceURL**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Essa propriedade é preterida. Em vez disso, recomendamos a classe **CIM \_ ServiceAccessURI** .

> [!Note]  
> Descrição preterida: uma URL que fornece o protocolo, o local de rede e outras informações específicas do serviço necessárias para acessar o serviço.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")
</dt> </dl>

Essa propriedade foi preterida e não deve ser usada.

> [!Note]  
> Descrição preterida: as pré-condições que devem ser atendidas para que esse serviço seja iniciado corretamente.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor")
</dt> </dl>

Essa propriedade foi preterida e não deve ser usada.

> [!Note]  
> Descrição preterida: os parâmetros que devem ser fornecidos ao método **StartService** para que esse serviço seja iniciado corretamente.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

