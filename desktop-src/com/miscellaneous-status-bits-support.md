---
title: Suporte a bits de status diversos
description: Suporte a bits de status diversos
ms.assetid: 3f967371-3d5a-4948-9008-6f4c3052bf07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c281b52283796d67c476e8ee00383436bc2235a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004838"
---
# <a name="miscellaneous-status-bits-support"></a>Suporte a bits de status diversos

Os contêineres de controle ActiveX devem reconhecer e dar suporte aos seguintes \_ bits de status OLEMISC.



| Bit de status                           | Necessário?      | Comentários                                                                                                                                                                                                                                                                                                |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACTIVATEWHENVISIBLE<br/>       | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| IGNOREACTIVATEWHENVISIBLE<br/> | No<br/>  | Necessário para suporte de controle inativo e sem janela. O bit IGNOREACTIVATEWHENVISIBLE é para contêineres que hospedam controles inativos e sem janela. O bit IGNOREACTIVATEWHENVISIBLE é introduzido como parte da especificação de controles ActiveX 96, consulte esta documentação para obter mais detalhes.<br/> |
| Inverso<br/>                 | No<br/>  | Geralmente não é usado com controles ActiveX, mas sim com incorporações de documentos compostos. Observe que isso é diferente de alguma documentação do SDK que diz que esse bit deve ser definido para o ACTIVATEWHENVISIBLE bit a ser definido.<br/>                                                                             |
| INVISIBLEATRUNTIME<br/>        | Yes<br/> | Designa um controle que deve ser visível em tempo de design, mas invisível no tempo de execução.<br/>                                                                                                                                                                                                       |
| ALWAYSRUN<br/>                 | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| ACTSLIKEBUTTON<br/>            | No<br/>  | O suporte é normalmente obrigatório, embora não seja necessário para contêineres de estilo de documento.<br/>                                                                                                                                                                                                    |
| ACTSLIKELABEL<br/>             | No<br/>  | O suporte é normalmente obrigatório, embora não seja necessário para contêineres de estilo de documento.<br/>                                                                                                                                                                                                    |
| NOUIACTIVATE<br/>              | Yes<br/> |                                                                                                                                                                                                                                                                                                         |
| De alinhamento<br/>                 | No<br/>  |                                                                                                                                                                                                                                                                                                         |
| SIMPLEFRAME<br/>               | No<br/>  | Confira [confinamento de site de quadro simples](simple-frame-site-containment.md)<br/>                                                                                                                                                                                                                       |
| SETCLIENTSITEFIRST<br/>        | No<br/>  | O suporte para esse bit é recomendado, mas não obrigatório.<br/>                                                                                                                                                                                                                                       |
| IMEMODE<br/>                   | No<br/>  |                                                                                                                                                                                                                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

 





