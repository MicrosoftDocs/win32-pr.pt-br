---
description: Um aplicativo de console da MUI pode dar suporte a configurações do sistema ou configurações específicas do aplicativo para suas linguagens de interface do usuário. Este tópico discute a filtragem de idiomas para esse tipo de aplicativo.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrando linguagens em um aplicativo de console da MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcdd8fc0f7f63b5771f5b75b86ce5e76ab2420d407832d77b731ad952174cee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041316"
---
# <a name="filtering-languages-in-a-mui-console-application"></a>Filtrando linguagens em um aplicativo de console da MUI

Um aplicativo de console da MUI pode dar suporte a configurações do sistema ou configurações específicas do aplicativo para suas linguagens de interface do usuário. Este tópico discute a filtragem de idiomas para esse tipo de aplicativo.

## <a name="limit-the-languages-to-display"></a>Limitar os idiomas a exibir

Ao contrário de uma janela gráfica, o console Windows não pode exibir [scripts complexos,](uniscribe-glossary.md)como árabe, hebraico, hebraico, hebraico, híndi, urdu, tailandês e muitos outros. Portanto, muitas linguagens de interface do usuário não podem ser exibidas pelo console em nenhuma circunstância.

O console pode exibir apenas caracteres da página [de código OEM única](code-pages.md) associada à linguagem atual para aplicativos não Unicode. Para cada página de código OEM, o console usa uma fonte específica e isso pode não fornecer cobertura completa para essa página de código.

Essas limitações relacionadas ao console reduzem o número de linguagens de interface do usuário que o console pode exibir em um computador específico. Por exemplo, se o idioma atual para aplicativos não Unicode for japonês e o usuário tentar exibir texto alemão no console, os caracteres com umlauts não serão exibidos corretamente. Se o idioma atual para aplicativos não Unicode for alemão e o usuário quiser exibir texto japonês no console, os resultados serão muito piores, tornando o texto quase incomputível.

> [!Note]  
> Ao fornecer suporte ao console para seus aplicativos MUI, lembre-se de que o console fornece suporte limitado apenas para [editores de método de entrada](input-method-manager.md).

 

## <a name="set-the-language-for-console-output"></a>Definir o idioma para saída do console

No Windows Vista e posterior, um aplicativo de console define o idioma para dar suporte à exibição do console chamando [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Nesta chamada, o aplicativo passa o FILTRO DO CONSOLE da MUI no parâmetro \_ \_ *dwFlags* e **NULL** para *pwszLanguagesBuffer.* Uma alternativa é chamar [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) com um identificador de idioma 0. Essa configuração faz com que a função selecione o idioma que melhor dá suporte à exibição do console.

No Windows XP, o aplicativo só pode definir o idioma para a saída do console chamando [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) com um identificador de idioma de 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo preferências de idioma do aplicativo](setting-application-language-preferences.md)
</dt> </dl>

 

 
