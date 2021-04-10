---
description: Especifica a complexidade do algoritmo do codificador.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Propriedade MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165404"
---
# <a name="mfpkey_complexity-property"></a>\_Propriedade de complexidade MFPKEY

\[[**MFPKEY \_ A complexidade**](mfpkey-complexityexproperty.md) está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use **MFPKEY \_ COMPLEXITYEX**.\]

Especifica a complexidade do algoritmo do codificador.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCComplexityMode

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

O valor padrão depende da versão do codificador de vídeo, conforme mostrado na tabela a seguir.



| Versão do codificador                 | Valor padrão |
|---------------------------------|---------------|
| Codificador do Windows Media Video 9   | 3             |
| Codificador de vídeo 7/8 do Windows Media | 1             |



 

## <a name="remarks"></a>Comentários

Esse valor inteiro varia de 0 a 3. Valores mais baixos fazem com que o codec use algoritmos de codificação menos complicados. Embora os algoritmos mais simples produzam uma saída de qualidade inferior, o processo de codificação é mais rápido e requer menos capacidade de processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




