---
description: Um aplicativo de console do MUI pode dar suporte a configurações do sistema ou configurações específicas do aplicativo para seus idiomas de interface do usuário. Este tópico discute a filtragem de idiomas para esse tipo de aplicativo.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrando linguagens em um aplicativo de console do MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828581"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtrando linguagens em um aplicativo de console do MUI

Um aplicativo de console do MUI pode dar suporte a configurações do sistema ou configurações específicas do aplicativo para seus idiomas de interface do usuário. Este tópico discute a filtragem de idiomas para esse tipo de aplicativo.

## <a name="limit-the-languages-to-display"></a>Limitar os idiomas a serem exibidos

Ao contrário de uma janela gráfica, o console do Windows não pode exibir [scripts complexos](uniscribe-glossary.md), como árabe, Hebraico, persa, híndi, Urdu, tailandês e muitos outros. Portanto, muitos idiomas de interface do usuário não podem ser exibidos pelo console do em nenhuma circunstância.

O console do pode exibir somente caracteres da [página de código OEM](code-pages.md) única associada ao idioma atual para aplicativos não Unicode. Para cada página de código OEM, o console do usa uma fonte específica, e isso pode não fornecer cobertura completa para essa página de código.

Essas limitações relacionadas ao console reduzem o número de idiomas de interface do usuário que o console do pode exibir em um determinado computador. Por exemplo, se o idioma atual para aplicativos não-Unicode for japonês e o usuário tentar exibir o texto em alemão no console, os caracteres com trema não serão exibidos corretamente. Se o idioma atual para aplicativos não-Unicode for alemão e o usuário quiser exibir texto em japonês no console, os resultados serão muito piores, renderizando o texto quase incompreensível.

> [!Note]  
> Ao fornecer suporte ao console para seus aplicativos MUI, lembre-se de que o console do fornece apenas suporte limitado para [editores de método de entrada](input-method-manager.md).

 

## <a name="set-the-language-for-console-output"></a>Definir o idioma da saída do console

No Windows Vista e posterior, um aplicativo de console define o idioma para dar suporte à exibição do console chamando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Nesta chamada, o aplicativo passa o \_ filtro do console \_ do MUI no parâmetro *dwFlags* e **nulo** para *pwszLanguagesBuffer*. Uma alternativa é chamar [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) com um identificador de idioma de 0. Essa configuração faz com que a função selecione o idioma que melhor dá suporte à exibição do console.

No Windows XP, o aplicativo só pode definir o idioma da saída do console chamando [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) com um identificador de idioma 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo preferências de idioma do aplicativo](setting-application-language-preferences.md)
</dt> </dl>

 

 
