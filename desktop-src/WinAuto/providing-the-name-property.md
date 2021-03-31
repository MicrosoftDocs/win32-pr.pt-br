---
title: Fornecendo a propriedade Name
description: Os desenvolvedores de servidor devem tomar cuidado ao criar controles predefinidos e comuns para garantir que o Microsoft Acessibilidade Ativa possa expor a propriedade Name para o controle.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d7a4c30c6bc228785a886d9a41717f8cdb8dda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917400"
---
# <a name="providing-the-name-property"></a>Fornecendo a propriedade Name

Os desenvolvedores de servidor devem tomar cuidado ao criar controles predefinidos e comuns para garantir que o Microsoft Acessibilidade Ativa possa expor a [Propriedade Name](name-property.md) para o controle. Dependendo do tipo de controle, o texto da propriedade Name é proveniente de um dos seguintes:

-   O texto da janela do controle (ou legenda)
-   Texto estático que rotula o controle

Para localizar o texto da janela do controle, o Microsoft Acessibilidade Ativa envia a mensagem de [**\_ gettext do WM**](/windows/desktop/winmsg/wm-gettext) para o controle. Esse texto corresponde ao parâmetro text na instrução de definição de recurso do controle. Para alguns controles, como botões, esse é o mesmo texto que é exibido com o controle. Para outros controles, como barras de ferramentas, esse texto não é exibido. Portanto, os desenvolvedores de servidor devem fornecer texto significativo na instrução de definição de recurso do controle para ajudar os usuários de utilitários cliente a identificar o controle.

Para localizar o rótulo do controle, o Microsoft Acessibilidade Ativa procura um controle de texto estático chamando [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) com o \_ sinalizador GW HWNDPREV. A pesquisa será interrompida se um controle de texto estático for encontrado ou se for encontrado um controle que tenha o grupo WS-in de estilos do Windows \_ \| WS \_ TabStop. Essa ordem de pesquisa corresponde à ordem de tabulação inversa em uma caixa de diálogo. Os desenvolvedores de servidor devem observar a ordem de tabulação ao criar controles para que um controle de texto estático preceda imediatamente o controle que ele rotula.

Para obter mais informações sobre as técnicas que o Microsoft Acessibilidade Ativa usa para expor a [Propriedade Name](name-property.md), consulte [referência de elemento de interface do usuário](user-interface-element-reference.md).

 

 