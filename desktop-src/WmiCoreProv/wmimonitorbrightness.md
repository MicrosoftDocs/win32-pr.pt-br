---
description: Representa os parâmetros de brilho de um monitor de computador.
ms.assetid: 01fa3efc-2a1d-4405-989f-2c180842c6b9
title: Classe WmiMonitorBrightness
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightness
- WmiMonitorBrightness.Active
- WmiMonitorBrightness.CurrentBrightness
- WmiMonitorBrightness.InstanceName
- WmiMonitorBrightness.Level
- WmiMonitorBrightness.Levels
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 10343b33e5bc1881440af9d13029913d470880289e71b4c7a33fb4748e56ef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821517"
---
# <a name="wmimonitorbrightness-class"></a>Classe WmiMonitorBrightness

A **classe WMI WmiMonitorBrightness** representa os parâmetros de brilho de um monitor de computador.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorBrightness : MSMonitorClass
{
  boolean Active;
  uint8   CurrentBrightness;
          InstanceName;
  uint8   Level[];
  uint32  Levels;
};
```

## <a name="members"></a>Membros

A **classe WmiMonitorBrightness** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe WmiMonitorBrightness** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o monitor de destino está ativo.

</dd> <dt>

**CurrentBrightness**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Brilho atual. Esse valor deve ser um valor retirado dos *Níveis*.

Exemplo: 100

</dd> <dt>

InstanceName
</dt> <dd> <dl> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: Chave
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz que contém os possíveis níveis de brilho.

Exemplo: \[ 0, 1, 2, ..., 100 \] .

</dd> <dt>

**Níveis**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número total de níveis de brilho compatíveis com o monitor, conforme descrito em *Nível*.

Exemplo: 101

</dd> </dl>

## <a name="examples"></a>Exemplos

Para obter mais informações e exemplos de código sobre como usar essa classe no [PowerShell,](https://blogs.technet.com/b/heyscriptingguy/archive/2013/07/25/use-powershell-to-report-and-set-monitor-brightness.aspx)consulte Usar o PowerShell para relatar e definir o brilho do monitor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI \\ raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




