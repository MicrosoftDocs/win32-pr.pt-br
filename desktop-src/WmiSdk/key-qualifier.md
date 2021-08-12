---
description: O qualificador key indica se a propriedade faz parte do alça de namespace.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificador de chave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae5525aa85ab744e7e6824bb6079511a3611643d53594503e70c8e587f363cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555884"
---
# <a name="key-qualifier"></a>Qualificador de chave

O **qualificador** key indica se a propriedade faz parte do alça de namespace. Se mais de uma propriedade tiver o **qualificador** Key, todas essas propriedades formarão coletivamente a chave (uma chave composta). Quando juntas, as propriedades de chave devem fornecer uma referência exclusiva para cada instância de classe. Se esse qualificador for colocado em uma propriedade, somente o valor **TRUE** será permitido.

Você pode usar qualquer tipo de propriedade, exceto pelo seguinte:

-   Matrizes
-   Números reais e de ponto flutuante
-   Objetos inseridos
-   Caracteres inferiores ao ASCII 32 (ou seja, caracteres de espaço em branco)
-   Cadeias de caracteres do tipo **char16** ou cadeias de caracteres definidas como chaves devem conter valores maiores que U+0020. Isso porque o WMI usa valores de chave em caminhos de objeto e você não pode usar caracteres sem impressão em um caminho de objeto.

Quando uma classe pai especifica uma chave, todas as classes derivadas da classe pai herdam essa chave. As classes derivadas não podem alterar a chave herdada nem definir nenhuma nova propriedade de chave. No entanto, quando você deriva uma subclasse de uma classe abstrata sem uma chave, pode introduzir uma chave na subclasse.

Todas as classes que definem mais de uma instância devem especificar uma chave. Como as classes abstratas não definem nenhuma instância, elas não precisam especificar chaves. Como as classes singleton definem apenas uma instância, elas não podem especificar chaves.

As chaves são escritas uma vez na insta instação do objeto e não devem ser modificadas posteriormente. Não faz sentido aplicar um valor padrão a uma propriedade qualificada por chave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



 

 




