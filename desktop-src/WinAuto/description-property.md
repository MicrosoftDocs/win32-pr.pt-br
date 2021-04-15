---
title: Propriedade Description (recursos de acessibilidade do Windows)
description: A propriedade Descrição de um objeto fornece uma descrição textual sobre a aparência visual de um objeto.
ms.assetid: 1fe3221f-e1dd-44b2-b749-d00bee1b6b89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34320b2959899d049d959037c0f24299780b54b0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454567"
---
# <a name="description-property-windows-accessibility-features"></a>Propriedade Description (recursos de acessibilidade do Windows)

> [!Note]  
> A propriedade **Description** geralmente é usada incorretamente e não é suportada pela automação da interface do usuário da Microsoft. Os desenvolvedores do Microsoft Acessibilidade Ativa Server não devem usar essa propriedade. Se mais informações forem necessárias para cenários de acessibilidade e automação, use as propriedades com suporte pelos elementos de automação da interface do usuário e padrões de controle.

 

A propriedade **Descrição** de um objeto fornece uma descrição textual sobre a aparência visual de um objeto. A descrição é usada principalmente para fornecer um contexto maior para usuários com deficiência visual ou cegas, mas também é usada para pesquisa de contexto ou outros aplicativos. Essa propriedade pode ajudar os usuários a entender um ícone ou a aparência visual geral.

A propriedade **Description** é recuperada chamando [**IAccessible:: get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription).

## <a name="when-to-support-the-description-property"></a>Quando dar suporte à propriedade Description

Os servidores suportarão a propriedade **Descrição** se a descrição não for óbvia ou quando ela não for redundante com base nas propriedades [**nome**](name-property.md), [**função**](role-property.md), [**estado**](state-property.md)e [**valor**](value-property.md) do objeto. Por exemplo, um botão rotulado como "OK" não precisará de informações adicionais, enquanto um botão que mostra uma imagem de um cacto faria. As propriedades **Name**, **role** e [**Help**](help-property.md) para tal botão descrevem sua finalidade, mas a propriedade **Description** transmite informações que são menos tangíveis; por exemplo, "esse botão mostra uma imagem de um cacto".

Um Microsoft Acessibilidade Ativa Server pode adicionar suporte para automação da interface do usuário usando [anotação direta](direct-annotation.md), usando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ou implementando o Microsoft acessibilidade ativa e a automação da interface do usuário lado a lado com ambas as implementações que manipulam a mensagem do [**WM \_ GetObject**](wm-getobject.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando anotação direta](using-direct-annotation.md)
</dt> <dt>

[A interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




