---
description: Especifica se o DSP de captura de voz executa a supressão de ruído.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Propriedade MFPKEY_WMAAECMA_FEATR_NS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105786165"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a>\_ \_ \_ Propriedade ns do MFPKEY WMAAECMA

Especifica se o DSP de captura de voz executa a supressão de ruído.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

1

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

A supressão de ruído é um componente de DSP (processamento de sinal digital) que suprime ou reduz o ruído de fundo estacionário no sinal de áudio. A supressão de ruído é aplicada após o processamento do AEC (cancelamento de eco acústico) e da matriz de microfone.

Essa propriedade pode ter os valores a seguir.



| Valor | Descrição                |
|-------|----------------------------|
| 0     | Desabilitar supressão de ruído. |
| 1     | Habilitar supressão de ruído.  |



 

O valor padrão dessa propriedade é 1 (habilitado). Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

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

 

 
