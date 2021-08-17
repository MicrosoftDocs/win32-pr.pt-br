---
description: A autenticação está comprovando quem você é.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Autenticação para páginas da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46a063cdd63631f84aa21980f89a143b3d1e9b42af020799d0f9f1bb7502b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141429"
---
# <a name="authentication-for-web-pages"></a>Autenticação para páginas da Web

A autenticação está comprovando quem você é.

**Objetivo:** Para que o agente de autenticação da Web seja exibido como parte do seu aplicativo.

## <a name="prerequisites"></a>Pré-requisitos

Nenhum

**Tempo para concluir:** 15 minutos.

## <a name="instructions"></a>Instruções

### <a name="1-getting-started"></a>1. Introdução

inicie o arquivo de instalação para instalar um site Contoso no Serviços de Informações da Internet 8 no computador local para hospedar os arquivos HTML e CSS de exemplo.

1.  Os arquivos HTML e CSS de exemplo serão instalados no diretório arquivos de programas do Microsoft \\ contoso.
2.  além disso, um aplicativo de Windows Store "Fabrikam Social" será desempacotado na área de trabalho.

### <a name="2-getting-familiar"></a>2. familiarizando-se

para ter uma ideia de como as páginas de exemplo se parecem no agente de autenticação da Web, abra o arquivo da solução Fabrikam social Visual Studio 11 na pasta "Fabrikam Social" na área de trabalho.

1.  Execute o aplicativo e clique em "Iniciar" para abrir as páginas de exemplo no agente de autenticação da Web.
2.  O aplicativo pode ser redimensionado para um lado ou ativado por meio do compartilhamento de alguns dados para o aplicativo.

### <a name="3-authentication"></a>3. Autenticação

Quando a API de autenticação da Web é invocada pelo aplicativo subjacente para se conectar ao provedor, "contoso social", a página de logon é mostrada. Esta página foi projetada para ser melhor em uma experiência de logon rápida e fluida. Ele também fornece pontos de entrada para algumas outras ações comuns do usuário, como recuperar detalhes da senha, inscrever-se em uma conta e ler instruções sobre privacidade e termos e condições que são concluídas no navegador. ![página de logon da contoso](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

[Tutorial de resumo para autenticação de páginas da Web](tutorial-for-authenticating-web-pages.md)

Próxima [autorização para páginas da Web](authorization-for-web-pages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
