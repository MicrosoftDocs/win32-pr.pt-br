---
description: Contém o tipo de conexão do monitor.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: Classe WmiMonitorConnectionParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 64212c523459696ced37e42689f6a4be0edb056b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170393"
---
# <a name="wmimonitorconnectionparams-class"></a>Classe WmiMonitorConnectionParams

A classe WMI WmiMonitorConnectionParams contém o tipo de conexão do monitor.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorConnectionParams** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorConnectionParams** tem essas propriedades.

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

</dd> <dt>

**VideoOutputTechnology**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de conexão de tecnologia de saída de vídeo. Os valores válidos são documentados na enumeração de [ \_ tecnologia de \_ saída \_ de vídeo D3DKMDT](https://msdn.microsoft.com/library/ms794498.aspx) .

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

 

 




