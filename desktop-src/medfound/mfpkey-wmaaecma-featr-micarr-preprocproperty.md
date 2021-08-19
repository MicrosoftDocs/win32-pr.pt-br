---
description: Especifica se o DSP de Captura de Voz executa o pré-processamento da matriz de microfone.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbba5faeb1a1e70feb1ef6182d3ac2a397a52c4a56f27e767be93f4a3fff773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873010"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a>Propriedade \_ PREPROC MFPKEY WMAAECMA \_ \_ MICARR \_ MICARR

Especifica se o DSP de Captura de Voz executa o pré-processamento da matriz de microfone.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

BOOL da VT \_

## <a name="default-value"></a>Valor padrão

VARIANT \_ TRUE

## <a name="applies-to"></a>Aplica-se A

-   [DSP de Captura de Voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentários

O pré-processamento pode remover tons fixos que interferem no processamento, como um tom com um tom fixo.

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição            |
|----------------|------------------------|
| VARIANT \_ FALSE | Desabilite o pré-processamento. |
| VARIANT \_ TRUE  | Habilitar o pré-processamento.  |



 

O valor padrão dessa propriedade é VARIANT \_ TRUE (habilitado). Antes de definir essa propriedade, você deve definir a [propriedade \_ MFPKEY WMAAECMA \_ FEATURE \_ MODE](mfpkey-wmaaecma-feature-modeproperty.md) como VARIANT \_ TRUE.

O DSP usa essa propriedade somente quando o processamento da matriz de microfone está habilitado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[DSP de Captura de Voz](voicecapturedmo.md)
</dt> </dl>

 

 
