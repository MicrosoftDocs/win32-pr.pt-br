---
description: Especifica se o DSP de captura de voz executa o controle de lucro automático.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: Propriedade MFPKEY_WMAAECMA_FEATR_AGC (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f42c7abd854b8fe18b5cfd4fe23ededb28faa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813506"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>\_ \_ \_ Propriedade AGC do MFPKEY WMAAECMA

Especifica se o DSP de captura de voz executa o controle de lucro automático.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ falso

## <a name="applies-to"></a>Aplica-se A

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O controle de lucro automático é um componente do DSP (processamento de sinal digital) que ajusta o lucro para que o nível de saída do sinal permaneça dentro do mesmo intervalo aproximado.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição                     |
|----------------|---------------------------------|
| VARIANTE \_ falso | Desabilitar o controle de lucro automático. |
| VARIANTE \_ true  | Habilitar o controle de lucro automático.  |



 

O valor padrão dessa propriedade é VARIANT \_ false (Disabled). Antes de definir essa propriedade, você deve definir a propriedade [ \_ modo de \_ recurso \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-feature-modeproperty.md) como Variant \_ true.

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

 

 
