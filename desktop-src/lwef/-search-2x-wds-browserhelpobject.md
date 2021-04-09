---
title: Chamando o WDS de páginas da Web
description: Você pode chamar o Microsoft Windows Desktop Search (WDS) de qualquer página da Web criada ou mantida usando o BHO (objeto auxiliar do navegador) e o Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782e7ca8b529c8f69b1f36d44decfae44895e4ec
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "104007220"
---
# <a name="calling-wds-from-web-pages"></a>Chamando o WDS de páginas da Web

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use o [Windows Search](../search/-search-3x-wds-overview.md) em vez disso.

Você pode chamar o Microsoft Windows Desktop Search (WDS) de qualquer página da Web criada ou mantida usando o BHO (objeto auxiliar do navegador) e o Windows Internet Explorer. Você pode ver como isso funciona na página da Web do MSN. Acima da caixa de pesquisa no https://www.msn.com há vários tipos de pesquisa: Web, notícias, imagens, área de trabalho, Encarta e local. Se você clicar em área de trabalho, os parâmetros de pesquisa serão passados para o Windows Desktop Search, que pesquisará o catálogo e exibirá os resultados na interface do usuário do WDS. Para que os usuários iniciem uma pesquisa de desktop de suas páginas da Web, o WDSBHO deve ser instalado e habilitado em seus sistemas, suas páginas da Web devem ser registradas com o WDS como uma URL permitida e você deve criar um link para passar a consulta User-enetered para o WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Habilitando o objeto de ajuda do navegador WDS

O BHO é instalado e habilitado no Internet Explorer por padrão quando você instala o WDS, mas você pode verificar facilmente se ele não foi desabilitado ou desinstalado. No sistema de um usuário, abra o Internet Explorer, selecione **Opções da Internet** no menu **ferramentas** , clique na guia **programas** e, em seguida, clique em **gerenciar** Complementos. Na lista de Complementos, procure a classe dsWebAllowBHO e verifique se ela está habilitada. Quando o BHO estiver desabilitado, o WDS continuará a funcionar normalmente; no entanto, você não poderá pesquisar na área de trabalho de uma página da Web.

As duas opções a seguir para permitir uma pesquisa na área de trabalho executarão a pesquisa localmente com o aplicativo de pesquisa registrado.

## <a name="registering-web-page-urls"></a>Registrando URLs de página da Web

O registro inclui uma lista de URLs de domínio "permitidas" das quais o WDS pode ser chamado. Para incluir suas páginas da Web, você precisa listar suas URLs de domínio como REG \_ sz no registro da seguinte maneira:

**HKEY \_ Software do \_ computador local** \\  \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **permitido**\\*<number>* = <domainURL>

Em que **<number>** é numerada sequencialmente e **<domainURL>** é a URL da página da Web que você deseja permitir que o WDS pesquise. Essa cadeia de caracteres de URL pode incluir o asterisco curinga \* no início ou no final da URL. Por exemplo, se a cadeia de caracteres for " \* . mydomain.com", você poderá iniciar uma pesquisa do WDS do https://www.mydomain.com e do https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Habilitando a pesquisa da área de trabalho por URL

Outra opção que não requer acesso ao registro é usar a seguinte URL em suas páginas da Web:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

em que **consulta** é a cadeia de caracteres codificada na URL na qual o usuário está pesquisando, incluindo quaisquer termos de [sintaxe de consulta avançada](-search-2x-wds-aqsreference.md) .

 

 




