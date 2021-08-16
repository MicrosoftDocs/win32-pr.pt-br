---
description: Os sinalizadores listados na tabela a seguir especificam o tipo de barramento de e/s usado pelo adaptador gráfico.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: Sinalizadores de tipo de barramento OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4989a91c308a7dc82bb15e9cd577a6facd89a0a6de9a32f0ef95f400917ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972995"
---
# <a name="opm-bus-type-flags"></a>Sinalizadores de tipo de barramento OPM

Os sinalizadores listados na tabela a seguir especificam o tipo de barramento de e/s usado pelo adaptador gráfico.



| Constante/valor                                                                                                                                                                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ Tipo de barramento \_ \_ outro**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Indica um tipo de barramento diferente dos tipos listados aqui.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ Tipo de barramento \_ \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | Barramento PCI.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ Tipo de barramento \_ \_ PCIX**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | Barramento PCI-X.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ Tipo de barramento \_ \_ PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | Barramento PCI Express.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ Tipo de barramento \_ \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Barramento AGP (Accelerated Graphics Port).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ Modificador \_ de implementação de barramento dentro \_ do \_ chipset**</dt> <dt>0x00010000</dt> </dl>                                                                      | A implementação do adaptador gráfico está em uma ponte norte do chipset da motherboard. Esse sinalizador implica que os dados nunca passam por um barramento de expansão (como PCI ou AGP) quando são transferidos da memória principal para o adaptador gráfico. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ O \_ \_ modificador \_ de implementação de barramento acompanha \_ \_ a placa-mãe no \_ \_ \_ chip**</dt> <dt>0x00020000</dt> </dl>                            | O adaptador gráfico é conectado à ponte norte do chipset da motherboard por meio de faixas na placa-mãe, e todos os chips do adaptador gráfico (circuitos integrados) são soldados na placa-mãe. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ O \_ \_ modificador de implementação de barramento \_ acompanha \_ \_ \_ a placa-mãe para o \_ \_ soquete**</dt> <dt>0x00030000</dt> </dl>                      | O adaptador gráfico é conectado à ponte norte do chipset da motherboard por meio de faixas na placa-mãe, e todos os chips do adaptador gráfico são conectados por meio de soquetes à placa-mãe.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ \_Conector da \_ \_ \_ placa \_ auxiliar do modificador de implementação de barramento**</dt> <dt>0x00040000</dt> </dl>                                                 | O adaptador gráfico é conectado à placa-mãe por meio de um conector do daughterboard.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ \_ \_ \_ \_ Conector da placa auxiliar do modificador \_ de implementação de barramento \_ dentro \_ de \_ NUAE**</dt> <dt>0x00050000</dt> </dl> | O adaptador gráfico é conectado à placa-mãe por meio de um conector do daughterboard e o adaptador gráfico está dentro de um compartimento que não é acessível pelo usuário.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ \_Modificador de implementação de barramento \_ \_ não \_ padrão**</dt> <dt>0x80000000</dt> </dl>                                                                                      | Modificador não padrão. (Opcional).<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ \_Tipo de barramento compatível com Copp \_ \_ \_ integrado**</dt> <dt>0x80000000</dt> </dl>                                                                                                     | Barramento integrado. Esse sinalizador é usado somente no modo de emulação COPP. Isso indica que os sinais de comando e status entre o adaptador gráfico e outros subsistemas no computador não estão disponíveis em um barramento de expansão que tenha uma especificação pública e um tipo de conector padrão, a menos que seja um barramento de memória. Esse sinalizador pode ser combinado com um sinalizador de **\_ tipo de barramento OPM \_ \_ xxx** .<br/> |



## <a name="remarks"></a>Comentários

Até três sinalizadores podem ser definidos, usando um **OR bit a** bit. Os sinalizadores no intervalo de 0x00 a 0x04 **( \_ tipo de barramento OPM \_ \_ xxx**) fornecem o tipo de barramento básico. Os sinalizadores no intervalo de 0x10000 a 0x50000 **( \_ \_ \_ modificador de \_ implementação do barramento OPM xxx**) modificam a descrição básica. O driver define um sinalizador de tipo de barramento e pode, opcionalmente, configurar um sinalizador de modificador. Além disso, o driver pode, opcionalmente, definir o sinalizador de **modificação de barramento OPM, \_ \_ \_ \_ não \_ padrão** .

No modo de emulação de COPP, o driver não usa os sinalizadores de modificador, mas pode definir o sinalizador **\_ integrado de \_ \_ \_ tipo \_ de barramento compatível com Copp de OPM** .

Os sinalizadores do tipo de bug de OPM \_ \_ \_ xxxx e o sinalizador **\_ integrado do \_ \_ tipo de barramento \_ \_ compatível com a Copp de OPM** são equivalentes aos valores da enumeração de [**\_ BusType Copp**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) usada no protocolo Copp (certificado de proteção de saída).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de OPM](opm-enumerations.md)
</dt> </dl>

 

 
