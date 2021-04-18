---
description: Representa os recursos de exibição com suporte do monitor.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Classe SupportedDisplayFeaturesDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810913"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>Classe SupportedDisplayFeaturesDescriptor

O **SupportedDisplayFeaturesDescriptor** representa os recursos de exibição com suporte do monitor. As informações nessa classe correspondem aos dados na definição de entrada de vídeo do padrão de dados de identificação de exibição estendida (E-EDID) avançado da VESA (Video Electronics Standard Association).

## <a name="syntax"></a>Sintaxe

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a>Membros

A classe **SupportedDisplayFeaturesDescriptor** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SupportedDisplayFeaturesDescriptor** tem essas propriedades.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Suporte para ativo e energia muito baixa. A exibição consome menos energia quando recebe um sinal de intervalo que está fora do intervalo de operação do ativo declarado. A exibição será revertida para a operação normal se o sinal de intervalo retornar ao intervalo de operação normal. Exemplos de sinais de tempo fora do intervalo de operação normal não são sinais DE sincronização ou nenhum sinal DE.

</dd> <dt>

**TipoDeExibição**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de exibição do monitor. A tabela a seguir lista os valores possíveis.



| Valor                                                                              | Significado                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Exibição monocromática/escala de cinza<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Exibição de cor RGB<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Exibição de cores não RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição tem suporte GTF. Se **for true**, a exibição dará suporte a intervalos com base no padrão GTF usando valores de parâmetro GTF padrão.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição tem um modo de temporizador preferencial. Se **for true**, o primeiro bloco de tempo detalhado conterá o modo de temporização preferencial do monitor. O uso do modo de temporização preferencial é exigido pelo EDID v. 1.3 e superior.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, a exibição dará suporte a sRGB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição dá suporte à espera de DPMS (sinalização de gerenciamento de energia de vídeo VESA). Se for **true**, o DPMS standby terá suporte.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição dá suporte à suspensão de sinalização de gerenciamento de energia de vídeo VESA (DPMS). Se for **true**, haverá suporte para a suspensão de DPMS.

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

 

 




