---
description: Especifica se o DSP de captura de voz executa recorte de centro.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Propriedade MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164926"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a>\_Propriedade de \_ clipe do \_ Centro \_ do MFPKEY WMAAECMA

Especifica se o DSP de captura de voz executa recorte de centro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ true

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O recorte centralizado é um processo que remove resíduos de eco pequeno que permanecem após o processamento de AEC, em situações de uma só conversa (quando a fala ocorre apenas em uma extremidade da linha).

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição              |
|----------------|--------------------------|
| VARIANTE \_ falso | Desabilitar recorte de centro. |
| VARIANTE \_ true  | Habilitar recorte de centro.  |



 

O valor padrão dessa propriedade é VARIANT \_ true (Enabled). Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

O DSP usa essa propriedade somente quando o processamento de AEC está habilitado.

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

 

 
