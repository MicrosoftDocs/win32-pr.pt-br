---
description: A \_ classe NIC HWConfig é a classe de tipo de evento para eventos de configuração de placa de interface de rede. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: Classe HWConfig_NIC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1d9b82f8a97c1ca47734b5bb0a1db09167510978c53f86870df01f2acc59b2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394720"
---
# <a name="hwconfig_nic-class"></a>\_Classe NIC HWConfig

A **classe \_ NIC HWConfig** é a classe de tipo de evento para eventos de configuração de placa de interface de rede.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a>Membros

A **classe \_ NIC HWConfig** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ NIC HWConfig** tem essas propriedades.

<dl> <dt>

NICName
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId (1), StringTermination ("NullTerminated"), Format ("w")
</dt> </dl>

Nome da placa de interface de rede.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HWConfig**](hwconfig.md)
</dt> </dl>

 

 




