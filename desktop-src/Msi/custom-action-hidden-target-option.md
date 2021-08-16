---
description: Use os sinalizadores de opção a seguir para especificar que o instalador não grave o valor inserido no campo de destino da tabela CustomAction no log. Para definir a opção, adicione o valor nessa tabela ao valor no campo tipo da tabela CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Opção de destino oculto de ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adc0df477510ac7d5d6bec65025b6fed1bfd7971e6ddf35da3a7e4cbc714690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638159"
---
# <a name="custom-action-hidden-target-option"></a>Opção de destino oculto de ação personalizada

Use os sinalizadores de opção a seguir para especificar que o instalador não grave o valor inserido no campo de destino da [tabela CustomAction](customaction-table.md) no log. Para definir a opção, adicione o valor nessa tabela ao valor no campo tipo da tabela CustomAction.



| Constante                            | Hexadecimal | Decimal | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (nenhum)                              | 0x0000      | 0       | O instalador pode gravar o valor na coluna de destino da tabela CustomAction no arquivo de log.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | O instalador é impedido de gravar o valor na coluna de destino da [tabela CustomAction](customaction-table.md) no arquivo de log. A propriedade CustomActionData também não é registrada quando o instalador executa a ação personalizada.<br/> Como o instalador define o valor de CustomActionData de uma propriedade com o mesmo nome que a ação personalizada, essa propriedade deve ser listada na propriedade [**MsiHiddenProperties**](msihiddenproperties.md) para impedir que seu valor apareça no log.<br/> |



 

Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ação personalizada](custom-action-reference.md)
</dt> <dt>

[Sobre ações personalizadas](about-custom-actions.md)
</dt> <dt>

[Usando ações personalizadas](using-custom-actions.md)
</dt> </dl>

 

 




