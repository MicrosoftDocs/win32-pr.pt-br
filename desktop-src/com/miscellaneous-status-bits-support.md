---
title: Suporte a bits de status diversos
description: Suporte a bits de status diversos
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d491e4f9ab3e41cf42510beeeb037e3b58e80a5f02ebe8e86e8bb07f3be5cb2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096916"
---
# <a name="miscellaneous-status-bits-support"></a>Suporte a bits de status diversos

ActiveX Os contêineres de controle devem reconhecer e dar suporte aos seguintes \_ bits de status OLEMISC.



| Bit de status                           | Obrigatório?      | Comentários                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Sim<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | Não<br/>  | Necessário para suporte de controle inativo e sem janela. O bit IGNOREACTIVATEWHENVISIBLE é para contêineres que hospedam controles inativos e sem janela. o bit IGNOREACTIVATEWHENVISIBLE é introduzido como parte da especificação de ActiveX controles 96, consulte esta documentação para obter mais detalhes.<br/> |
| Inverso<br/>                 | Não<br/>  | geralmente não é usado com controles ActiveX, mas sim com incorporações de documentos compostos. Observe que isso é diferente de alguma documentação do SDK que diz que esse bit deve ser definido para o ACTIVATEWHENVISIBLE bit a ser definido.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Sim<br/> | Designa um controle que deve ser visível em tempo de design, mas invisível no tempo de execução.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Sim<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | Não<br/>  | O suporte é normalmente obrigatório, embora não seja necessário para contêineres de estilo de documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | Não<br/>  | O suporte é normalmente obrigatório, embora não seja necessário para contêineres de estilo de documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Sim<br/> |                                                                                                                                                                                                                                                                                                         |
| De alinhamento<br/>                 | Não<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | Não<br/>  | Confira [confinamento de site de quadro simples](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | Não<br/>  | O suporte para esse bit é recomendado, mas não obrigatório.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | Não<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 





