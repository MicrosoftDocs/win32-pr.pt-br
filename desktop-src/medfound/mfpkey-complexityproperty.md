---
description: Propriedade MFPKEY_COMPLEXITY-especifica a complexidade do algoritmo do codificador.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Propriedade MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bb611c95451f590df2e9ff4c1df02b17eda2d1dc00e256381931cbacde435f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113436"
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
| Windows Codificador de vídeo de mídia 9   | 3             |
| Windows Codificador de vídeo de mídia 7/8 | 1             |



 

## <a name="remarks"></a>Comentários

Esse valor inteiro varia de 0 a 3. Valores mais baixos fazem com que o codec use algoritmos de codificação menos complicados. Embora os algoritmos mais simples produzam uma saída de qualidade inferior, o processo de codificação é mais rápido e requer menos capacidade de processamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




