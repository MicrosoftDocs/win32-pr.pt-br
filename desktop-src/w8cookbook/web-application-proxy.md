---
title: Proxy de aplicativo Web
description: Proxy de aplicativo Web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a346297dca0a81d8c2269b61e8a5d581f03f95fab56e044bedce7513882535f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211321"
---
# <a name="web-application-proxy"></a>Proxy de aplicativo Web

## <a name="platform"></a>Plataforma

**servidores-** Windows Server 2012 R2  






## <a name="description"></a>Descrição

no Windows Server 2012 R2, adicionamos um novo serviço chamado Proxy de aplicativo Web na função de acesso remoto que permite aos administradores publicar aplicativos para acesso externo. Esse serviço atua como um proxy reverso e como um proxy de Serviços de Federação do Active Directory (AD FS) (AD FS). Na verdade, esse serviço substitui o serviço de proxy AD FS como ele era conhecido no Windows Server 2012.

Com o proxy de aplicativo Web, uma organização pode tornar os recursos da Web locais disponíveis para acesso externo, ao mesmo tempo em que gerencia o risco desse acesso controlando as políticas de autenticação e autorização no AD FS.

## <a name="manifestation"></a>Manifestação

O serviço proxy de AD FS não está mais na função Serviços de Federação do Active Directory (AD FS) (AD FS), mas foi substituído pelo proxy de aplicativo Web na função de acesso remoto. Isso representa uma expansão do serviço de proxy de AD FS, incluindo a funcionalidade de proxy reverso para publicação de aplicativos.

## <a name="solution"></a>Solução

Para acessar o proxy de aplicativo Web, os administradores podem ir para Gerenciador do Servidor e adicionar um novo serviço de função/função. O administrador encontrará o proxy de aplicativo Web na função de acesso remoto.

## <a name="resources"></a>Recursos

-   [Guia da solução](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 