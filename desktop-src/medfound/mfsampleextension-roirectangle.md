---
description: Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Atributo MFSampleExtension_ROIRectangle (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311b17cab20de16a83d145563e8ba0b8ead6f055428ffc6a3823c99deab05fc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240321"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>\_Atributo MFSampleExtension ROIRectangle

Especifica os limites da região de interesse que indica a região do quadro que requer qualidade diferente.

## <a name="data-type"></a>Tipo de dados

**[**ROI \_ ÁREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** armazenada como **blob**

## <a name="remarks"></a>Comentários

Depois de configurar com êxito [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) para um valor diferente de zero em um MFT do codificador, o aplicativo pode definir esse atributo em exemplos de entrada e esperar que ele seja respeitado.

Se [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) não for definido como um valor diferente de zero, o \_ atributo MFSampleExtension ROIRectangle será ignorado em exemplos de entrada.

MFSampleExtension \_ ROIRectangle é definido em um exemplo de entrada e é aplicado somente à amostra de entrada atual.

O campo **QPDelta** na estrutura [**da \_ área de ROI**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) especifica o Delta de parâmetro de quantificação para a região especificada a partir do restante do quadro. Se **QPDelta** for positivo, isso indicará que o aplicativo quer que o retângulo tenha uma qualidade menor do que o restante do quadro.

**Codificadores H. 264/AVC:** **QPDelta** deve estar entre \[ -25, + 25 \] . O codificador deve garantir que a QP final esteja em um intervalo válido para o padrão de vídeo.

A região especificada não precisa ser alinhada em MB. Os codificadores têm flexibilidade para decidir o limite real. É recomendável cobrir toda a região especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Aplicativos de aplicativos UWP da área de trabalho R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




