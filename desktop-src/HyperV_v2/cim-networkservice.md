---
description: Essa classe foi preterida. Em vez disso, recomendamos derivar da classe serviço \_ CIM.
ms.assetid: 67b3a96e-4549-41e0-8097-f8d145df0c49
title: CIM_NetworkService classe
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
ms.openlocfilehash: cfb2ea7b122516cc3b62f675684649e22577171f713856638f97985d9713e8d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694686"
---
# <a name="cim_networkservice-class"></a>Classe CIM \_ NetworkService

Essa classe foi preterida. Em vez disso, recomendamos derivar da [**classe serviço CIM. \_**](cim-service.md)

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

A **classe \_ NetworkService cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ NetworkService cim** tem essas propriedades.

<dl> <dt>

**Palavras-chave**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sem valor")
</dt> </dl>

Essa propriedade foi preterida e não deve ser usada.

> [!Note]  
> Descrição preterida: uma matriz de palavras-chave que podem ser usadas em consultas.

 

</dd> <dt>

**Serviceurl**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ ServiceAccessURI")
</dt> </dl>

Essa propriedade é preterida. Em vez disso, recomendamos a **classe Cim \_ ServiceAccessURI.**

> [!Note]  
> Descrição preterida: uma URL que fornece o protocolo, o local da rede e outras informações específicas do serviço necessárias para acessar o serviço.

 

</dd> <dt>

**StartupConditions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sem valor")
</dt> </dl>

Essa propriedade foi preterida e não deve ser usada.

> [!Note]  
> Descrição preterida: as pré-condições que devem ser atendidas para que esse serviço inicie corretamente.

 

</dd> <dt>

**StartupParameters**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sem valor")
</dt> </dl>

Essa propriedade foi preterida e não deve ser usada.

> [!Note]  
> Descrição preterida: os parâmetros que devem ser fornecidos ao **método StartService** para que esse serviço inicie corretamente.

 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Serviço \_ CIM**](cim-service.md)
</dt> </dl>

 

