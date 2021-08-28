---
title: Chamando o WDS de páginas da Web
description: Você pode chamar o Microsoft Windows Desktop Search (WDS) em qualquer página da Web que você criar ou manter usando o BHO (Objeto Auxiliar do Navegador) e Windows Internet Explorer.
ms.assetid: 8d9fa541-530e-4917-a6d9-4e04549ce32e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2be6be30889e8f759ee3cf7529250a5513ce58
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883709"
---
# <a name="calling-wds-from-web-pages"></a>Chamando o WDS de páginas da Web

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para o Windows XP e Windows Server 2003. Em versões posteriores, use [Windows Search.](../search/-search-3x-wds-overview.md)

Você pode chamar o Microsoft Windows Desktop Search (WDS) em qualquer página da Web que você criar ou manter usando o BHO (Objeto Auxiliar do Navegador) e Windows Internet Explorer. Você pode ver como isso funciona na página da Web do MSN. Acima da caixa de pesquisa em estão vários tipos https://www.msn.com de pesquisa: Web, Notícias, Imagens, Área de Trabalho, Encarta e Local. Se você clicar em Área de Trabalho, os parâmetros de pesquisa serão passados para Windows Desktop Search, que pesquisa o catálogo e exibe os resultados na interface do usuário do WDS. Para que os usuários iniciem uma pesquisa de área de trabalho em suas páginas da Web, o WDSBHO deve ser instalado e habilitado em seus sistemas, suas páginas da Web devem ser registradas com o WDS como uma URL permitida e você deve criar um link para passar a consulta eneterada pelo usuário para o WDS.

## <a name="enabling-the-wds-browser-help-object"></a>Habilitando o objeto de ajuda do navegador WDS

O BHO é instalado e habilitado no Internet Explorer por padrão ao instalar o WDS, mas você pode verificar facilmente se ele não foi desabilitado ou desinstalado. No sistema de um usuário, abra Internet Explorer , selecione Opções da  **Internet** no **menu** Ferramentas, clique na guia Programas e clique em Gerenciar **Complementos**. Na lista de complementos, procure a Classe dsWebAllowBHO e certifique-se de que ela está habilitada. Quando o BHO estiver desabilitado, o WDS continuará funcionando normalmente; no entanto, você não poderá pesquisar a área de trabalho em uma página da Web.

Ambas as opções a seguir para permitir uma pesquisa de área de trabalho executarão a pesquisa localmente com o aplicativo de pesquisa registrado.

## <a name="registering-web-page-urls"></a>Registrando URLs de página da Web

O Registro inclui uma lista de URLs de domínio "permitidas" das quais o WDS pode ser chamado. Para incluir suas páginas da Web, você precisa listar suas URLs de domínio como REG SZ no Registro \_ da seguinte forma:

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows Desktop Search** \\ **DSW** \\ **Domínio** \\ *&lt; de número &gt;*  =  &lt; permitidoURL&gt;

Em **&lt; que o &gt;** número é numerado sequencialmente e **&lt; domainURL &gt;** é a URL da Página da Web da qual você deseja permitir pesquisas do WDS. Essa cadeia de caracteres de URL pode incluir o asterisco \* curinga no início ou no final da URL. Por exemplo, se a cadeia de caracteres for " .mydomain.com", você poderá iniciar uma \* pesquisa de WDS de https://www.mydomain.com e https://mydomain.com .

## <a name="enabling-desktop-search-by-url"></a>Habilitando a Pesquisa de Área de Trabalho por URL

Outra opção que não exige acesso ao Registro é usar a SEGUINTE URL em suas páginas da Web:

https://toolbar.msn.com/desktop/results.aspx?q=QUERY

em **que QUERY** é a cadeia de caracteres codificada por URL na qual o usuário está pesquisando, incluindo quaisquer termos de [Sintaxe de Consulta](-search-2x-wds-aqsreference.md) Avançada.

 

 




