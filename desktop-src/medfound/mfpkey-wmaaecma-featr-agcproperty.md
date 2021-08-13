---
description: Especifica se o DSP de Captura de Voz executa o controle de ganho automático.
ms.assetid: 85ac8de0-ac36-4b34-a93d-0ac792a677b2
title: MFPKEY_WMAAECMA_FEATR_AGC propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f038b18657363677e0953f8fe973c2e3029130ffc2183a08344e1b0cd6905747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343806"
---
# <a name="mfpkey_wmaaecma_featr_agc-property"></a>Propriedade \_ AGC MFPKEY WMAAECMAGCR \_ \_

Especifica se o DSP de Captura de Voz executa o controle de ganho automático.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="default-value"></a>Valor padrão

VARIANT \_ FALSE

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O controle de ganho automático é um componente de DSP (processamento de sinal digital) que ajusta o ganho para que o nível de saída do sinal permaneça dentro do mesmo intervalo aproximado.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição                     |
|----------------|---------------------------------|
| VARIANT \_ FALSE | Desabilite o controle de ganho automático. |
| VARIANT \_ TRUE  | Habilitar controle de ganho automático.  |



 

O valor padrão dessa propriedade é VARIANT \_ FALSE (desabilitado). Antes de definir essa propriedade, você deve definir a [propriedade \_ MFPKEY WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) como VARIANT \_ TRUE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[DSP de Captura de Voz](voicecapturedmo.md)
</dt> </dl>

 

 
