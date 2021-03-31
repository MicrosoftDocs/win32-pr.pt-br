---
description: O provedor de classe WDM define a classe WMIBinaryMofResource no \\ \\ namespace raiz WMI para dar suporte à tarefa de manter o controle do status dos dados no repositório WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Classe WMIBinaryMofResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827495"
---
# <a name="wmibinarymofresource-class"></a>Classe WMIBinaryMofResource

O provedor de classe WDM define a classe **WMIBinaryMofResource** no \\ \\ namespace raiz WMI para dar suporte à tarefa de manter o controle do status dos dados no repositório WMI.

## <a name="syntax"></a>Sintaxe

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a>Membros

A classe **WMIBinaryMofResource** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WMIBinaryMofResource** tem essas propriedades.

<dl> <dt>

**HighDateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Metade alta do carimbo de data/hora.

</dd> <dt>

**LowDateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Metade baixa do carimbo de data/hora.

</dd> <dt>

**MofProcessed**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Sinalizador que indica se o arquivo. mof foi totalmente processado.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Nome do driver habilitado para WDM que tem um arquivo MOF binário compilado com êxito no repositório WMI.

</dd> </dl>

## <a name="remarks"></a>Comentários

O provedor de classe WDM cria uma instância de **WMIBinaryMofResource** para cada driver WDM que fornece um arquivo MOF binário.

Sempre que o WMI Inicializa o provedor, o provedor compara o carimbo de data/hora com o carimbo de data/hora do arquivo de imagem do driver. Se os carimbos de data/hora forem diferentes, o WMI recompilará o arquivo MOF.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                     |
| Namespace<br/>                | \\WMI raiz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>WMI. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor WDM](wdm-provider.md)
</dt> </dl>

 

