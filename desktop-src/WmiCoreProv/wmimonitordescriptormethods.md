---
description: Contém métodos que obtêm o conteúdo bruto da definição de entrada de vídeo dos dados de identificação de vídeo avançado (VESA) avançados de associação de exibição estendida de vídeo (E-EDID) v. 1. x Standard 128-bytes de dados.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 7e8fe02540cd68047e3e74c052a8ea833a67d829228979da31bb12e13e84d9f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120956"
---
# <a name="wmimonitordescriptormethods-class"></a>Classe WmiMonitorDescriptorMethods

A classe WMI **WmiMonitorDescriptorMethods** contém métodos que obtêm o conteúdo bruto da definição de entrada de vídeo dos dados de identificação de vídeo (VESA) avançados de associação de exibição estendida (E-EDID) v. 1. x os blocos de dados padrão de 128 bytes.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorDescriptorMethods** tem estes tipos de membros:

-   [Métodos](#wmimonitordescriptormethods-class)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **WmiMonitorDescriptorMethods** tem esses métodos.



| Método                                                                                           | Descrição                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**WmiGetMonitorRawEEdidV1Block**](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | Acessa os dados brutos para um bloco de descritor do EDID v. 1. x especificado.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **WmiMonitorDescriptorMethods** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




