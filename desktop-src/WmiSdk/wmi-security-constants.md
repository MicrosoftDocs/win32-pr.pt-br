---
description: O WMI verifica os direitos de acesso para aplicativos e scripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: Constantes de segurança do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171653"
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

 

 
