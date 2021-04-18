---
description: Contém métodos que gerenciam o brilho do monitor.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: Classe WmiMonitorBrightnessMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 36fe823703d5d5e4f1f6008d02c600828fe2b53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810206"
---
# <a name="wmimonitorbrightnessmethods-class"></a>Classe WmiMonitorBrightnessMethods

A classe WMI **WmiMonitorBrightnessMethods** contém métodos que gerenciam o brilho do monitor.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorBrightnessMethods** tem estes tipos de membros:

-   [Métodos](#wmimonitorbrightnessmethods-class)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **WmiMonitorBrightnessMethods** tem esses métodos.



| Método                                                                                                         | Descrição                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Define o brilho de volta para a configuração de política.<br/>     |
| [**WmiSetALSBrightness**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Define o valor de brilho do sensor de luz ambiente.<br/>     |
| [**WmiSetALSBrightnessState**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Controla o estado de brilho do sensor de luz ambiente.<br/> |
| [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Define o brilho do monitor.<br/>                        |



 

### <a name="properties"></a>Propriedades

A classe **WmiMonitorBrightnessMethods** tem essas propriedades.

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

 

 




