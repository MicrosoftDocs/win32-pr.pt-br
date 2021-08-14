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
ms.openlocfilehash: a9e71eeda4ab47cba5e88a548421c89815b7d0d87d511709b9a73573e2582077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321532"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a>Classe SupportedDisplayFeaturesDescriptor

O **SupportedDisplayFeaturesDescriptor representa** os recursos de exibição com suporte do monitor. As informações nesta classe correspondem aos dados no padrão E-EDID (Video Input Definition) da VESA (Video Electronics Standard Association).

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

A **classe SupportedDisplayFeaturesDescriptor** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe SupportedDisplayFeaturesDescriptor** tem essas propriedades.

<dl> <dt>

**ActiveOffSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Suporte para energia desligada e muito baixa. A exibição consome menos energia quando recebe um sinal de tempo que está fora do intervalo operacional ativo declarado. A exibição será revertida para a operação normal se o sinal de tempo retornar para o intervalo operacional normal. Exemplos de sinais de tempo fora do intervalo operacional normal não são sinais de sincronização ou nenhum sinal DE.

</dd> <dt>

**DisplayType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de exibição para o monitor. A tabela a seguir lista os valores possíveis.



| Valor                                                                              | Significado                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Exibição de escala de cinza/monocromática<br/> |
| <dl> <dt>1 (0x1)</dt> </dl> | Exibição de cor RGB<br/>            |
| <dl> <dt>2 (0x2)</dt> </dl> | Exibição multicolor não RGB<br/>   |



 

</dd> <dt>

**GTFSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição tem suporte para GTF. Se **True**, a exibição dá suporte a tempos com base no padrão GTF usando valores de parâmetro GTF padrão.

</dd> <dt>

**HasPreferredTimingMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição tem um modo de tempo preferencial. Se **True**, o primeiro bloco de tempo detalhado conterá o modo de tempo preferencial do monitor. O uso do modo de tempo preferencial é exigido pelo EDID v.1.3 e superior.

</dd> <dt>

**sRGBSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **True**, a exibição dá suporte a sRGB.

</dd> <dt>

**StandbySupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição dá suporte à espera do VESA DPMS (Sinalização de Gerenciamento de Energia de Exibição). Se **True**, há suporte para o DPMS em espera.

</dd> <dt>

**SuspendSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a exibição dá suporte à suspensão do VESA DPMS (Sinalização de Gerenciamento de Energia de Exibição). Se **True**, há suporte para a suspensão do DPMS.

</dd> </dl>

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

 

 




