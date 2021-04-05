---
description: A autorização define a quais recursos você tem acesso.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorização para páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827597"
---
# <a name="authorization-for-web-pages"></a>Autorização para páginas da Web

A autorização define a quais recursos você tem acesso.

**Objetivo:** Para permitir que os usuários acessem seu aplicativo.

## <a name="prerequisites"></a>Pré-requisitos

Nenhum

**Tempo para conclusão:** 2 minutos.

## <a name="instructions"></a>Instruções

### <a name="1-authorization"></a>1. autorização

Quando o usuário insere suas credenciais e clica no botão de logon, a página permissões é mostrada. Essa página é melhor para permitir que os usuários controlem as permissões granulares ao conceder ao aplicativo acesso aos dados da contoso. ![página de permissões da contoso](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. como usar o exemplo

Você precisa saber sobre os seguintes arquivos HTML e CSS.

1.  Os seguintes arquivos HTML correspondem às duas páginas no fluxo de autorização da Web
    -   WebAuthLogin.html – HTML de exemplo para a página de logon
    -   WebAuthPermissions.html – HTML de exemplo para a página de permissões
2.  Os arquivos CSS contêm estilos do Windows 8 para ajudar a criar uma página da Web do aplicativo da Windows Store.
    -   UI-Light. css – isso foi derivado da folha de estilos base para controles do Windows 8.
    -   UI-webauth. css – fornece estilo incremental para otimizar o layout para páginas de autenticação na Web.
    -   Theme-Colors. css – fornece o estilo incremental para substituir as cores de destaque padrão dos controles pela cor da marca do provedor.

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

[Tutorial de resumo para autenticação de páginas da Web](tutorial-for-authenticating-web-pages.md)

Próximas [práticas recomendadas para a criação de páginas da Web de autenticação](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
