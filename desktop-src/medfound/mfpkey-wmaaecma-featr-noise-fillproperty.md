---
description: Especifica se o DSP de captura de voz executa o preenchimento de ruído.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Propriedade MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790616"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a>\_Propriedade de \_ preenchimento de \_ ruído MFPKEY WMAAECMA \_

Especifica se o DSP de captura de voz executa o preenchimento de ruído.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ true

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O preenchimento de ruído adiciona uma pequena quantidade de ruído a partes do sinal em que o recorte de centro removeu os ecos residuais. Isso resulta em uma melhor experiência para o usuário do que deixar lacunas silenciosas no sinal.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição            |
|----------------|------------------------|
| VARIANTE \_ true  | Habilite o preenchimento de ruído.  |
| VARIANTE \_ falso | Desabilite o preenchimento de ruído. |



 

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

 

 
