---
description: Especifica o tipo de barramento de e/s usado pelo adaptador gráfico.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Enumeração D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cece215946406bedcca2cbfdd2b64bfdb5df00208b2d84cf2aa90fdb89b516bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828376"
---
# <a name="d3dbustype-enumeration"></a>Enumeração D3DBUSTYPE

Especifica o tipo de barramento de e/s usado pelo adaptador gráfico.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ outros**
</dt> <dd>

Indica um tipo de barramento diferente dos tipos listados aqui.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**\_PCI D3DBUSTYPE**
</dt> <dd>

Barramento PCI.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**
</dt> <dd>

Barramento PCI-X.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**
</dt> <dd>

Barramento PCI Express.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Barramento AGP (Accelerated Graphics Port).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Modificador D3DBUSIMPL \_ dentro \_ do \_ chipset**
</dt> <dd>

A implementação do adaptador gráfico está em uma ponte norte do chipset da motherboard. Esse sinalizador implica que os dados nunca passam por um barramento de expansão (como PCI ou AGP) quando são transferidos da memória principal para o adaptador gráfico.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL o \_ modificador \_ \_ de tela na placa- \_ mãe para o \_ \_ \_ chip**
</dt> <dd>

Indica que o adaptador gráfico está conectado à ponte norte de um chipset da motherboard controlando a placa-mãe e todos os chips do adaptador gráfico estão soldados na placa-mãe. Esse sinalizador implica que os dados nunca passam por um barramento de expansão (como PCI ou AGP) quando são transferidos da memória principal para o adaptador gráfico.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL o \_ modificador \_ controla \_ na \_ placa-mãe para o \_ \_ \_ soquete**
</dt> <dd>

O adaptador gráfico é conectado à ponte norte do chipset da motherboard por meio de faixas na placa-mãe, e todos os chips do adaptador gráfico são conectados por meio de soquetes à placa-mãe.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_Conector da \_ \_ placa filha do modificador D3DBUSIMPL \_**
</dt> <dd>

O adaptador gráfico é conectado à placa-mãe por meio de um conector do daughterboard.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ \_ Conector da placa filha do modificador D3DBUSIMPL \_ \_ dentro \_ de \_ NUAE**
</dt> <dd>

O adaptador gráfico é conectado à placa-mãe por meio de um conector do daughterboard e o adaptador gráfico está dentro de um compartimento que não é acessível pelo usuário.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificador de D3DBUSIMPL \_ não \_ padrão**
</dt> <dd>

Um dos sinalizadores do modificador do \_ modificador D3DBUSIMPL \_ \_ xxx está definido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Até três sinalizadores podem ser definidos. Os sinalizadores no intervalo de 0x00 a 0x04 (**D3DBUSTYPE \_ xxx**) fornecem o tipo de barramento básico. Os sinalizadores no intervalo 0x10000 por meio de 0x50000 (**D3DBUSIMPL \_ modificador \_ xxx**) modificam a descrição básica. O driver define um sinalizador de tipo de barramento e pode definir zero ou um sinalizador modificador. Se o driver definir um sinalizador de modificador, ele também definirá o sinalizador **D3DBUSIMPL de \_ modificador \_ não \_ padrão** . Os sinalizadores são combinados com um **OR bit a** bit.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>D3d9types. h (incluir D3d9. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de vídeo do Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




