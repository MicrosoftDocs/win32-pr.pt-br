---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de imagem.
ms.assetid: fb1707a7-16b0-4073-b21d-2ba2f4fd76f7
title: Propriedades da imagem (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 959a008d9c30991058226e52db6e45ed417ee6e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753893"
---
# <a name="image-properties"></a>Propriedades da imagem

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de imagem.



| Propriedade                                                                                                                                       | VarType     | Descrição                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_BITDEPTH de imagem WPD \_**                                                                                                                       | **\_UI4 VT** | A profundidade de bits da imagem.                                                                                                                                                                                                                                                                                                                     |
| <span id="wpd_image_color_corrected_status"></span><span id="WPD_IMAGE_COLOR_CORRECTED_STATUS"></span>**\_ \_ status corrigido da cor da imagem WPD \_ \_** | **\_UI4 VT** | Uma enumeração de [**\_ \_ \_ \_ valores de status corrigido de cor WPD**](wpd-color-corrected-status-values.md) que especifica se o arquivo foi corrigido por cores. Isso impede que vários dispositivos corrijam automaticamente a imagem durante o pós-processamento.<br/>                                                                       |
| **\_ \_ status cortado da imagem WPD \_**                                                                                                                | **\_UI4 VT** | Uma enumeração de [**\_ \_ \_ valores de status cortados WPD**](wpd-cropped-status-values.md) que especifica se o arquivo foi cortado. Isso impede que vários dispositivos cortem automaticamente a imagem durante o pós-processamento.<br/>                                                                                                        |
| **\_índice de \_ exposição de imagem WPD \_**                                                                                                                | **\_UI4 VT** | Um valor que identifica as configurações de velocidade do filme quando esta imagem foi capturada. As configurações correspondem às designações ISO de ASA/DIN.<br/> Normalmente, um dispositivo dá suporte a valores enumerados discretos, mas o controle contínuo sobre um intervalo é possível.<br/> Um valor de 0xFFFFFFFF corresponde à configuração ISO automática.<br/> |
| **\_tempo de \_ exposição da imagem WPD \_**                                                                                                                 | **\_UI4 VT** | Identifica a velocidade do obturador do dispositivo quando esta imagem foi capturada. As unidades estão em segundos dimensionadas por 10000.<br/>                                                                                                                                                                                                                        |
| **\_FNUMBER de imagem WPD \_**                                                                                                                        | **\_UI4 VT** | Identifica a configuração de abertura da lente quando esta imagem foi capturada. As unidades são iguais ao número f dimensionado por 100.<br/>                                                                                                                                                                                                              |
| **\_ \_ resolução horizontal de imagem WPD \_**                                                                                                         | **R8 de VT \_**  | Indica a resolução horizontal de uma imagem, em pontos por polegada (DPI).                                                                                                                                                                                                                                                                       |
| **\_ \_ resolução vertical da imagem WPD \_**                                                                                                           | **R8 de VT \_**  | Indica a resolução vertical de uma imagem, em pontos por polegada (DPI).                                                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




