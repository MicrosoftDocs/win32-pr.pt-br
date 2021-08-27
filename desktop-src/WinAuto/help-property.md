---
title: Propriedade da ajuda
description: A propriedade Help fornece informações que dizem ao usuário sobre a função de um objeto.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6f8b226c483e3a3d68f878fccb940fc1a9f69f18b6fde62eed4b5a7a8ea9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122186"
---
# <a name="help-property"></a>Propriedade da ajuda

A propriedade **Help** fornece informações que dizem ao usuário sobre a função de um objeto.

A propriedade **Help** é recuperada chamando [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).

Essa propriedade contém informações de estilo de balão (conforme encontradas em dicas de ferramenta) que são usadas para descrever o que o objeto faz ou como usá-lo. Por exemplo, a propriedade da **ajuda** para um botão da barra de ferramentas que mostra uma impressora pode fornecer o seguinte texto: "imprime o documento atual".

O texto da propriedade da **ajuda** não precisa ser exclusivo na interface do usuário.

## <a name="when-to-support-the-help-property"></a>Quando dar suporte à propriedade Help

Os servidores não oferecerão suporte à propriedade de **ajuda** se outras propriedades fornecerem informações suficientes sobre a finalidade do objeto e as ações que o objeto executa. Os objetos acessíveis que expõem os controles fornecidos pelo sistema não oferecem suporte à propriedade da **ajuda** .

 

 




