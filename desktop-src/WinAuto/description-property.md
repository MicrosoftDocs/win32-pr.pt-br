---
title: Propriedade Description (Windows recursos de acessibilidade)
description: A propriedade Description de um objeto fornece uma descrição textual sobre a aparência visual de um objeto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c695ae4ed8968620776aa0786358c98372940749be4a1c4335cb89f84b373ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994226"
---
# <a name="description-property-windows-accessibility-features"></a>Propriedade Description (Windows recursos de acessibilidade)

> [!Note]  
> A **propriedade Description** geralmente é usada incorretamente e não é suportada pela Microsoft Automação da Interface do Usuário. Microsoft Active Accessibility desenvolvedores de servidores não devem usar essa propriedade. Se mais informações são necessárias para cenários de acessibilidade e automação, use as propriedades com suporte Automação da Interface do Usuário elementos e padrões de controle.

 

A propriedade Description de **um** objeto fornece uma descrição textual sobre a aparência visual de um objeto. A descrição é usada principalmente para fornecer um contexto maior para usuários com visão baixa ou com deficiências, mas também é usada para pesquisa de contexto ou outros aplicativos. Essa propriedade pode ajudar os usuários a entender um ícone ou a aparência visual geral.

A **propriedade Description** é recuperada chamando [**IAccessible::get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Quando dar suporte à propriedade Description

Os servidores **darão** suporte à propriedade Description se a descrição não [](name-property.md)for óbvia ou quando não for redundante com base nas propriedades Nome, Função [**,**](role-property.md) [**Estado**](state-property.md)e Valor [**do**](value-property.md) objeto. Por exemplo, um botão rotulado como "OK" não precisaria de informações adicionais, enquanto um botão que mostra uma imagem de um dela. As **propriedades Name**, **Role** e [**Help**](help-property.md) para esse botão descrevem sua finalidade, mas a propriedade **Description** transmite informações menos tangíveis; por exemplo, "Esse botão mostra uma imagem de um homem".

Um servidor Microsoft Active Accessibility pode adicionar suporte ao Automação da Interface do Usuário usando a Anotação [Direta,](direct-annotation.md)usando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ou implementando o Microsoft Active Accessibility e o Automação da Interface do Usuário lado a lado com ambas as implementações que manipulam a mensagem [**WM \_ GETOBJECT.**](wm-getobject.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando anotação direta](using-direct-annotation.md)
</dt> <dt>

[A interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




