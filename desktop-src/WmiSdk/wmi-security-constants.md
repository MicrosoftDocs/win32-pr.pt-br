---
description: O WMI verifica os direitos de acesso para aplicativos e scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de segurança do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2f3a8ff4727852637fe6e4b808f0b8d3a74c958808cb3beb7bc9df32b0c995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739413"
---
# <a name="wmi-security-constants"></a>Constantes de segurança do WMI

O WMI verifica os direitos de acesso de aplicativos e scripts para objetos como namespaces WMI, impressora, serviços, aplicativos DCOM, arquivos, compartilhamentos e outros objetos protegíveis. O acesso a esses objetos protegíveis é controlado pelas entradas de controle de acesso (ACE). Cada ACE contém listas que designam quais grupos ou usuários têm acesso. Para obter mais informações sobre segurança e listas de controle de acesso (ACLs, DACLs ou SACLs), consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors).

Muitos métodos de provedor no WMI que afetam objetos protegíveis exigem que o administrador habilite determinados privilégios. Qual versão do privilégio que você usa depende da linguagem de programação, conforme mostrado em [**constantes de privilégio**](privilege-constants.md).

As constantes de segurança são definidas nos seguintes tópicos:

-   [**Constantes de segurança de evento**](event-security-constants.md)
-   [**Constantes de direitos de acesso de arquivo e diretório**](file-and-directory-access-rights-constants.md)
-   [**Constantes de direitos de acesso de namespace**](namespace-access-rights-constants.md)
-   [**Constantes do sinalizador ACE do namespace**](namespace-ace-flag-constants.md)
-   [**Constantes de tipo de ACE de namespace**](namespace-ace-type-constants.md)
-   [**Constantes de privilégio**](privilege-constants.md)

 

 
