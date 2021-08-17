---
description: Se esse bit for definido para um controle de texto estático, o controle tentará formatar automaticamente o texto exibido como um número que representa uma contagem de bytes.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formatar atributo de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34df03c87ceb742b543f32b770c201646185ce02df6386e38c9c5af02c6a1a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636024"
---
# <a name="formatsize-control-attribute"></a>Formatar atributo de controle

Se esse bit for definido para um controle de texto estático, o controle tentará formatar automaticamente o texto exibido como um número que representa uma contagem de bytes. Para formatação adequada, o texto do controle deve ser definido como uma cadeia de caracteres que representa um número expresso em unidades de 512 bytes. Em seguida, o valor exibido é formatado em kilobytes (KB), megabytes (MB) ou gigabytes (GB) e exibido com a cadeia de caracteres apropriada que representa as unidades. Para obter mais informações, consulte [controle de texto](text-control.md).



| Valor numérico do texto original | Cadeia de caracteres de unidade usada |
|----------------------------------|------------------|
| Menos de 20480                  | KB               |
| Menos de 20971520               | MB               |
| Menos de 10737418240            | GB               |



 

## <a name="valid-controls"></a>Controles válidos



| Decimal | Hexadecimal | Control                          |
|---------|-------------|----------------------------------|
| 524288  | 0x00080000  | msidbControlAttributesFormatSize |



 

## <a name="remarks"></a>Comentários

Para definir esse atributo em um controle, inclua os bits de formatação na coluna atributos do registro do controle na [tabela de controle](control-table.md). O texto do controle deve ser definido como uma cadeia de caracteres que representa um número expresso em unidades de 512 bytes. O texto das cadeias de caracteres de unidade é definido na [tabela UIText](uitext-table.md). O posicionamento da cadeia de caracteres de unidade é controlado pela propriedade [**LeftUnit**](leftunit.md) . Se a propriedade **LeftUnit** for definida como qualquer valor, a cadeia de caracteres de unidade será exibida antes do valor numérico. Se algo diferente de caracteres numéricos aparecer no texto associado ao controle, o valor exibido será indefinido.

Em tempo de execução, o instalador resolve a propriedade [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) para o número total de bytes necessários para a instalação em unidades de 512. Um controle de texto estático com um bit de formatação pode ser usado para formatar e rotular automaticamente o número total de bytes necessários para a instalação em KB, MB ou GB, conforme apropriado. Para os fins deste exemplo, suponha que o número total de bytes seja 18.336.768. O instalador define o valor da propriedade PrimaryVolumeSpaceRequired como 18.336.768 dividido por 512 ou 35.814. O número exibido pelo controle de texto com Formatize seria 17MB.

Os valores numéricos do texto original são fornecidos em unidades de 512. Na tabela acima, a cadeia de caracteres 20.480 corresponde à cadeia de caracteres KB porque 20.480 vezes 512 gera um resultado de 10.485.760 bytes ou 10.240 KB.

As cadeias de caracteres de unidade listadas na tabela anterior referem-se às chaves na [tabela UIText](uitext-table.md), em que o texto da cadeia de caracteres da unidade é definido.

O posicionamento da cadeia de caracteres de unidade é controlado pela propriedade [**LeftUnit**](leftunit.md) . Se a propriedade **LeftUnit** for definida como qualquer valor, a cadeia de caracteres de unidade será exibida antes do valor numérico.

Se algo diferente de caracteres numéricos aparecer no texto associado ao controle, o valor exibido será indefinido.

Para obter mais informações, consulte [controlar atributos](control-attributes.md) e [controles](controls.md).

 

 



