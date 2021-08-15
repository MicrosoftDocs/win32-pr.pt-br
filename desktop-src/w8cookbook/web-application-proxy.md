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

**Servidores – Windows Server 2012** R2  






## <a name="description"></a>Descrição

No Windows Server 2012 R2, adicionamos um novo serviço chamado web Proxy de Aplicativo na função acesso remoto que permite que os administradores publiquem aplicativos para acesso externo. Esse serviço atua como um proxy reverso e como um proxy Serviços de Federação do Active Directory (AD FS) (AD FS) . Na verdade, esse serviço substitui o serviço AD FS proxy como era conhecido no Windows Server 2012.

Com o web Proxy de Aplicativo, uma organização pode disponibilizar recursos da Web locais para acesso externo e, ao mesmo tempo, gerenciar o risco desse acesso controlando políticas de autenticação e autorização no AD FS.

## <a name="manifestation"></a>Manifestação

O AD FS de proxy do Serviços de Federação do Active Directory (AD FS) não está mais sob a função Serviços de Federação do Active Directory (AD FS) (AD FS), mas foi substituído pelo web Proxy de Aplicativo na função acesso remoto. Isso representa uma expansão do serviço de proxy AD FS, incluindo a funcionalidade de proxy reverso para publicação de aplicativos.

## <a name="solution"></a>Solução

Para acessar o web Proxy de Aplicativo, os administradores podem acessar Gerenciador do Servidor e adicionar um novo serviço de função/função. O administrador encontrará o web Proxy de Aplicativo na função Acesso Remoto.

## <a name="resources"></a>Recursos

-   [Guia da solução](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))

 

 