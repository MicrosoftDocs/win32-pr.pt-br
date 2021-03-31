---
description: O qualificador dinâmico indica uma classe cujas instâncias são criadas dinamicamente. O valor desse qualificador deve ser definido como TRUE.
ms.assetid: 63286687-abbf-49f0-8061-3b47fba75806
ms.tgt_platform: multiple
title: Qualificador dinâmico
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Dynamic
api_type:
- NA
api_location: ''
ms.openlocfilehash: f6530942859c8c3de571ba9ddb94e9b1ce78cc0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827841"
---
# <a name="dynamic-qualifier"></a>Qualificador dinâmico

O qualificador **dinâmico** indica uma classe cujas instâncias são criadas dinamicamente. O valor desse qualificador deve ser definido como **true**.

O qualificador **dinâmico** deve ser especificado em todas as classes que contêm dados e para quais instâncias são criadas dinamicamente. O qualificador de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) normalmente também é especificado para identificar o provedor responsável por fornecer os dados.

As classes que contêm apenas métodos que precisam de implementação não exigem o qualificador **dinâmico** . Somente o qualificador do [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) é necessário para especificar o nome do provedor para fornecer a implementação.

Todas as classes derivadas de uma classe dinâmica devem ser dinâmicas. Você não pode derivar uma classe estática de uma classe dinâmica.

Quando **Dynamic** é especificado em uma propriedade de uma instância, o qualificador **PropertyContext** também deve ser especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores WMI padrão**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

 




