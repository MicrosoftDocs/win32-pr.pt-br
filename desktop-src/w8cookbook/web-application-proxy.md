---
title: Proxy de aplicativo Web
description: Proxy de aplicativo Web
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104084956"
---
# <a name="web-application-proxy"></a>Proxy de aplicativo Web

## <a name="platform"></a>Plataforma

**Servidores-** Windows Server 2012 R2  






## <a name="description"></a>Descrição

No Windows Server 2012 R2, adicionamos um novo serviço chamado proxy de aplicativo Web na função de acesso remoto que permite aos administradores publicar aplicativos para acesso externo. Esse serviço atua como um proxy reverso e como um proxy de Serviços de Federação do Active Directory (AD FS) (AD FS). Na verdade, esse serviço substitui o serviço de proxy AD FS como era conhecido no Windows Server 2012.

Com o proxy de aplicativo Web, uma organização pode tornar os recursos da Web locais disponíveis para acesso externo, ao mesmo tempo em que gerencia o risco desse acesso controlando as políticas de autenticação e autorização no AD FS.

## <a name="manifestation"></a>Manifestação

O serviço proxy de AD FS não está mais na função Serviços de Federação do Active Directory (AD FS) (AD FS), mas foi substituído pelo proxy de aplicativo Web na função de acesso remoto. Isso representa uma expansão do serviço de proxy de AD FS, incluindo a funcionalidade de proxy reverso para publicação de aplicativos.

## <a name="solution"></a>Solução

Para acessar o proxy de aplicativo Web, os administradores podem ir para Gerenciador do Servidor e adicionar um novo serviço de função/função. O administrador encontrará o proxy de aplicativo Web na função de acesso remoto.

## <a name="resources"></a>Recursos

-   [Guia da solução](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 