---
title: Propriedade de função
description: A propriedade Role descreve o elemento de interface do usuário de um objeto. Todos os objetos dão suporte à propriedade Role.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2881b301537e9a25dabb260b84bc889cef4e4a6f9f6a5a2c8fab540d78daf8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133719"
---
# <a name="role-property"></a>Propriedade de função

A propriedade **role** descreve o elemento de interface do usuário de um objeto. Todos os objetos dão suporte à propriedade **role** .

Em muitos casos, a função do objeto é óbvia. Por exemplo, o Windows tem a função de [**\_ \_ janela do sistema de função**](object-roles.md) e os botões de push têm a função de [**\_ \_ pressão do sistema de função**](object-roles.md) .

A propriedade **role** é recuperada chamando [**IAccessible:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole).

## <a name="identifying-an-objects-role"></a>Identificando a função de um objeto

O Microsoft Acessibilidade Ativa fornece [constantes de função](object-roles.md), definidas em OleAcc. h, que identificam funções de objeto comuns. É recomendável que os desenvolvedores de servidor usem esses valores de função predefinidos. Se uma constante de função predefinida for retornada, os clientes usarão a função [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) para recuperar uma cadeia de caracteres localizada que descreve a função.

Para controles de animação, como o controle de animação exibido ao copiar arquivos, use a [**\_ \_ animação do sistema de funções**](object-roles.md). Os gráficos que são ocasionalmente animados são descritos como [**\_ \_ elemento gráfico do sistema de funções**](object-roles.md) com a propriedade [**State**](state-property.md) definida como [**estado \_ sistema \_ animado**](object-state-constants.md).

Observe que algumas funções não são fáceis de descrever. Por exemplo, a exibição de ícones grandes de uma pasta permite a disposição arbitrária de ícones, de modo que sua função poderia ser descrita como [**\_ \_ agrupamento do sistema de funções**](object-roles.md). Ou, um controle que fornece itens em linhas e colunas fixas pode ter a função de [**\_ \_ tabela do sistema de função**](object-roles.md) . Como uma função é usada para comunicar o modelo de uso para um usuário final, é importante usar a função apropriada. Por exemplo, se o seu controle atua como um botão, use a ação do [**sistema de função \_ \_**](object-roles.md).

 

 




