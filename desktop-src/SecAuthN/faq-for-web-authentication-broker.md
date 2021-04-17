---
description: Perguntas frequentes sobre o agente de autenticação da Web.
ms.assetid: 49ACB2E3-CF57-4D8E-9670-E7C18A06F76A
title: Perguntas frequentes sobre o agente de autenticação da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95942a32bba86f7b2ccb12264cc1a50419b248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104505976"
---
# <a name="faq-for-web-authentication-broker"></a>Perguntas frequentes sobre o agente de autenticação da Web

Perguntas frequentes sobre o agente de autenticação da Web.



| Pergunta                                                                                                    | Resposta                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Como posso ter certeza de que minha página do https://funciona com o agente de autenticação da Web?                         | Tente carregar a página no Windows Internet Explorer antes de experimentá-la com o agente de autenticação da Web. Se a sua página da Web for carregada sem erros, ela também será renderizada corretamente pelo agente de autenticação da Web. |
| No caso de um erro, os códigos de erro serão exibidos para o usuário?                                         | Enquanto uma página de erro for exibida para o usuário, o código de erro subjacente não será exibido. Ele é retornado apenas para o aplicativo. Como alternativa, você também pode usar os logs operacionais.                                    |
| Como posso encontrar mais detalhes sobre o erro encontrado?                                                       | Use os logs operacionais para obter detalhes.                                                                                                                                                                             |
| O contêiner de aplicativo SSO (logon único) compartilha seus cookies com o Internet Explorer ou com outros navegadores? | Não.                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Considerações para o desenvolvimento de páginas da Web](considerations-for-the-web-page-development.md)
</dt> <dt>

[Aplicativo de exemplo do SDK do agente de autenticação da Web](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
