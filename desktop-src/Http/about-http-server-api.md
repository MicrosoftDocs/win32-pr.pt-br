---
title: Sobre a API do servidor HTTP
description: A API do servidor HTTP fornece aos desenvolvedores uma interface de nível baixo para o lado do servidor da funcionalidade HTTP, conforme definido no RFC 2616.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- API do servidor HTTP, visão geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365644"
---
# <a name="about-http-server-api"></a>Sobre a API do servidor HTTP

A API do servidor HTTP fornece aos desenvolvedores uma interface de nível baixo para o lado do servidor da funcionalidade HTTP, conforme definido no [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). A API permite que um aplicativo receba solicitações HTTP direcionadas às URLs e envie respostas HTTP. Para enviar respostas dinâmicas, as interfaces ISAPI ou ASP.NET são recomendadas.

A API do servidor HTTP permite que vários aplicativos coexistam em um sistema, compartilhando a mesma porta TCP (por exemplo, a porta 80 para HTTP ou a porta 443 para HTTPS) e atendendo partes diferentes do namespace da URL.

A API do servidor HTTP requer conhecimento da linguagem de programação C e familiaridade com a programação da API do Windows. Os aplicativos que não exigem acesso de baixo nível ao HTTP devem usar a ISAPI do IIS ou as classes de .NET Framework para soluções baseadas em HTTP.

 

 




