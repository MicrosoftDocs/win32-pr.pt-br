---
description: Permite que o aplicativo substitua as configurações padrão em várias propriedades do DSP de captura de voz.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Propriedade MFPKEY_WMAAECMA_FEATURE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661496"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a>\_Propriedade do \_ modo de recurso MFPKEY WMAAECMA \_

Permite que o aplicativo substitua as configurações padrão em várias propriedades do DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ falso

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

Se essa propriedade for VARIANT \_ true, o aplicativo poderá definir as seguintes propriedades no DSP:

-   [AES do MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-featr-aesproperty.md)
-   [\_AGC MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-featr-agcproperty.md)
-   [\_clipe do \_ \_ Centro \_ do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [MFPKEY \_ WMAAECMA com \_ comprimento de \_ eco \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [\_tamanho do \_ \_ quadro \_ do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [\_ \_ \_ modo MICARR do MFPKEY WMAAECMA \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [MFPKEY \_ WMAAECMA refeito \_ \_ MICARR \_ preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [\_preenchimento de \_ \_ ruído \_ do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [\_ns MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-featr-nsproperty.md)
-   [MFPKEY \_ WMAAECMA para \_ \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)

Se essa propriedade for VARIANT \_ false, o DSP ignorará essas propriedades e usará suas configurações padrão. O valor padrão dessa propriedade é VARIANT \_ false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
