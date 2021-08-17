---
description: Representa parâmetros de entrada para vídeo digital.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Classe WmiMonitorDigitalVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926562"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>Classe WmiMonitorDigitalVideoInputParams

O **WmiMonitorDigitalVideoInputParams** representa parâmetros de entrada para vídeo digital. Os dados nessa classe correspondem aos dados na definição de entrada de vídeo do padrão de dados de identificação de vídeo estendido (E-EDID) avançado de associação de vídeo de eletrônicos (VESA). Uma instância dessa classe está disponível somente quando o valor da propriedade **VideoInputType** da classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) é "digital".

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>Membros

A classe **WmiMonitorDigitalVideoInputParams** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorDigitalVideoInputParams** tem essas propriedades.

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

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

VESA DFP 1. x ou compatível. Se definido, a interface é compatível com sinal com tela plana digital VESA (DFP) 1. x transição de sinal diferencial minimizada (TMDS) CRGB, 1 pixel/relógio, até 8 bits/cor bit mais significativo (MSB) alinhado, DE alto para ativo.

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

 

 




