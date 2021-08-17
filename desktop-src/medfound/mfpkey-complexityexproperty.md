---
description: MFPKEY_COMPLEXITYEX propriedade - especifica a complexidade do algoritmo do codificador.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e658e438909677f326372caa9e4da533e350b7133cc647b8f56562d09ad949e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873533"
---
# <a name="mfpkey_complexityex-property"></a>Propriedade MFPKEY \_ COMPLEXITYEX

Especifica a complexidade do algoritmo do codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

O valor padrão depende da versão do codificador de vídeo, conforme mostrado na tabela a seguir.



| Versão do codificador                 | Valor padrão |
|---------------------------------|---------------|
| Windows Codificador de Vídeo de Mídia 9   | 3             |
| Windows Codificador de Vídeo de Mídia 7/8 | 1             |



 

## <a name="possible-values"></a>Valores possíveis

Os valores possíveis dependem da versão do codificador de vídeo, conforme mostrado na tabela a seguir.



| Versão do codificador                 | Valores possíveis  |
|---------------------------------|------------------|
| Windows Codificador de Vídeo de Mídia 9   | 0, 1, 2, 3, 4, 5 |
| Windows Codificador de Vídeo de Mídia 7/8 | 0, 1             |



 

## <a name="remarks"></a>Comentários

Valores inferiores fazer com que o codec use algoritmos de codificação menos complicados. Embora os algoritmos mais simples produzam uma saída de qualidade inferior, o processo de codificação é mais rápido e requer menos capacidade de processamento. Isso pode ser importante ao codificar conteúdo de uma fonte ao vivo porque o codificador deve processar entradas rápido o suficiente para acompanhar a origem.

Qualquer valor atribuído a essa propriedade será ignorado se a propriedade [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) estiver definida como 1. Nesse caso, MFPKEY \_ COMPLEXITYEX é definido automaticamente como 3.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




