---
description: A autorização define a quais recursos você tem acesso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorização para páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141319"
---
# <a name="authorization-for-web-pages"></a>Autorização para páginas da Web

A autorização define a quais recursos você tem acesso.

**Objetivo:** Para permitir que os usuários acessem seu aplicativo.

## <a name="prerequisites"></a>Pré-requisitos

Nenhum

**Tempo para concluir:** 2 minutos.

## <a name="instructions"></a>Instruções

### <a name="1-authorization"></a>1. Autorização

Quando o usuário insinte suas credenciais e clica no botão Logon, a página de permissões é mostrada. Essa página é melhor para permitir que os usuários controlem permissões granulares ao conceder ao aplicativo acesso aos dados da Contoso. ![página de permissões contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Como usar o exemplo

Você precisa saber sobre os seguintes arquivos HTML e CSS.

1.  Os arquivos HTML a seguir correspondem às duas páginas no fluxo de autorização da Web
    -   WebAuthLogin.html – HTML de exemplo para a página de logon
    -   WebAuthPermissions.html – HTML de exemplo para a página de permissões
2.  Os arquivos CSS contêm Windows 8 estilos para ajudar a criar uma página da Web do Windows Store.
    -   ui-light.css – isso foi derivado da folha de estilos base para Windows 8 controles.
    -   ui-webauth.css – isso fornece estilo incremental para otimizar o layout para páginas de auth da Web.
    -   theme-colors.css – isso fornece o estilo incremental para substituir as cores de destaque padrão dos controles pela cor da marca do provedor.

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

Tutorial [de resumo para autenticação de páginas da Web](tutorial-for-authenticating-web-pages.md)

Próximas [práticas recomendadas para criar páginas da Web de autenticação](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicativo de exemplo do SDK do Agente de Autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
