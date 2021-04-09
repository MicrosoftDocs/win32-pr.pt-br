---
description: Especifica a complexidade do algoritmo do codificador.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: Propriedade MFPKEY_COMPLEXITYEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165405"
---
# <a name="mfpkey_complexityex-property"></a>\_Propriedade MFPKEY COMPLEXITYEX

Especifica a complexidade do algoritmo do codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityEx

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

O valor padrão depende da versão do codificador de vídeo, conforme mostrado na tabela a seguir.



| Versão do codificador                 | Valor padrão |
|---------------------------------|---------------|
| Codificador do Windows Media Video 9   | 3             |
| Codificador de vídeo 7/8 do Windows Media | 1             |



 

## <a name="possible-values"></a>Valores possíveis

Os valores possíveis dependem da versão do codificador de vídeo, conforme mostrado na tabela a seguir.



| Versão do codificador                 | Valores possíveis  |
|---------------------------------|------------------|
| Codificador do Windows Media Video 9   | 0, 1, 2, 3, 4, 5 |
| Codificador de vídeo 7/8 do Windows Media | 0, 1             |



 

## <a name="remarks"></a>Comentários

Valores mais baixos fazem com que o codec use algoritmos de codificação menos complicados. Embora os algoritmos mais simples produzam uma saída de qualidade inferior, o processo de codificação é mais rápido e requer menos capacidade de processamento. Isso pode ser importante ao codificar o conteúdo de uma fonte dinâmica porque o codificador deve processar entradas com rapidez suficiente para acompanhar a origem.

Qualquer valor atribuído a essa propriedade será ignorado se a propriedade [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) for definida como 1. Nesse caso, MFPKEY \_ COMPLEXITYEX é definido automaticamente como 3.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




