---
title: Propriedade da ajuda
description: A propriedade Help fornece informações que dizem ao usuário sobre a função de um objeto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292120"
---
# <a name="help-property"></a>Propriedade da ajuda

A propriedade **Help** fornece informações que dizem ao usuário sobre a função de um objeto.

A propriedade **Help** é recuperada chamando [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Essa propriedade contém informações de estilo de balão (conforme encontradas em dicas de ferramenta) que são usadas para descrever o que o objeto faz ou como usá-lo. Por exemplo, a propriedade da **ajuda** para um botão da barra de ferramentas que mostra uma impressora pode fornecer o seguinte texto: "imprime o documento atual".

O texto da propriedade da **ajuda** não precisa ser exclusivo na interface do usuário.

## <a name="when-to-support-the-help-property"></a>Quando dar suporte à propriedade Help

Os servidores não oferecerão suporte à propriedade de **ajuda** se outras propriedades fornecerem informações suficientes sobre a finalidade do objeto e as ações que o objeto executa. Os objetos acessíveis que expõem os controles fornecidos pelo sistema não oferecem suporte à propriedade da **ajuda** .

 

 




