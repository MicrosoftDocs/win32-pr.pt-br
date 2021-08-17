---
description: Representa os recursos de exibição básicos de um monitor de computador.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: Classe WmiMonitorBasicDisplayParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 958eb9134062d5380a2afda77eeaad3034a2da7430d2f6a3094916ceae211e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926778"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Classe WmiMonitorBasicDisplayParams

A **classe WMI WMI WmiMonitorBasicDisplayParams** representa os recursos de exibição básicos de um monitor de computador. O valor da propriedade **VideoInputType** indica se o monitor é análogo ou digital. Os dados nesta classe correspondem aos dados no bloco Parâmetros de Exibição/Recursos Básicos da VESA (Video Electronics Standard Association) padrão E-EDID (Extended Display Identification Data).

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a>Membros

A **classe WmiMonitorBasicDisplayParams** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe WmiMonitorBasicDisplayParams** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Característica de transferência de exibição (100 \* Gama-100).

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho máximo da imagem horizontal em centímetros. Para obter mais informações, consulte Comentários.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho máximo da imagem vertical em centímetros. Para obter mais informações, consulte Comentários.

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Exibir recursos com suporte pelo monitor.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de entrada de vídeo.



| Valor                                                                              | Significado            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analógico<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

**MaxHorizontalImageSize** e **MaxVerticalImageSize** representam as dimensões máximas de imagem que o monitor pode exibir corretamente para todo o conjunto de combinações de tempo e formato com suporte. A dimensão máxima da imagem é definida pelo PADRÃO VIAD (Definição de Área de Imagem de Vídeo) VESA e arredonda para o centímetro mais próximo. O sistema de computador host pode usar esses dados para selecionar o tamanho da imagem e a taxa de proporção que permitirão o texto dimensionado corretamente. Esteja ciente de que, se um ou ambos os campos são zero, o sistema não faz suposições sobre o tamanho da exibição. Por exemplo, o tamanho de uma exibição de projeção pode ser indeterminado.

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

 

 




