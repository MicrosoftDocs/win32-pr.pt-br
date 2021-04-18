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
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760664"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>Classe WmiMonitorBasicDisplayParams

A classe WMI **WmiMonitorBasicDisplayParams** representa os recursos de exibição básicos de um monitor de computador. O valor da propriedade **VideoInputType** indica se o monitor é analógico ou digital. Os dados nessa classe correspondem aos dados no bloco de parâmetros/recursos de exibição básico de VESA (vídeo de associação padrão de tela de eletrônicos) avançado (E-EDID) padrão de dados de identificação de exibição estendida.

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

A classe **WmiMonitorBasicDisplayParams** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **WmiMonitorBasicDisplayParams** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
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

Característica de transferência de exibição (100 \* gama-100).

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

Exibir recursos com suporte no monitor.

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
| <dl> <dt>0 (0x0)</dt> </dl> | Analog<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

**MaxHorizontalImageSize** e **MaxVerticalImageSize** representam as dimensões de imagem máxima que o monitor pode exibir corretamente para todo o conjunto de combinações de tempo e formato com suporte. A dimensão de imagem máxima é definida pelo padrão da VIAD (linguagem de imagem de vídeo) VESA e é arredondada para o centímetro mais próximo. O sistema de computador host pode usar esses dados para selecionar o tamanho da imagem e a taxa de proporção que permitirá o texto corretamente dimensionado. Lembre-se de que, se um ou ambos os campos forem zero, o sistema não fará suposições sobre o tamanho de exibição. Por exemplo, o tamanho de uma exibição de projeção pode não ser determinado.

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

 

 




