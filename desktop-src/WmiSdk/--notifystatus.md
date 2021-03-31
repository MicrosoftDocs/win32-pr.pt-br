---
description: Serve como a classe pai para classes de erro definidas pelo provedor.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: Classe __NotifyStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663135"
---
# <a name="__notifystatus-class"></a>\_\_Classe NotifyStatus

A classe de sistema abstrata **\_ \_ NotifyStatus** serve como a classe pai para classes de erro definidas pelo provedor.

A sintaxe a seguir é simplificada do código formato MOF (MF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ NotifyStatus** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ NotifyStatus** tem essas propriedades.

<dl> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Contém um código de erro ou informações para uma operação. Pode ser qualquer código definido pelo usuário, mas o valor 0 (zero) geralmente é reservado para indicar êxito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Embora a classe **\_ \_ NotifyStatus** possa ser a classe pai para classes de erro definidas pelo provedor, é recomendável que os provedores derivem classes Error de [**\_ \_ ExtendedStatus**](--extendedstatus.md) em vez disso. O uso de **\_ \_ ExtendedStatus** permite uma maior padronização das classes Error.

Os provedores nunca devem criar instâncias do **\_ \_ NotifyStatus** diretamente, pois essas instâncias não transmitem mais informações do que um código de retorno simples.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




