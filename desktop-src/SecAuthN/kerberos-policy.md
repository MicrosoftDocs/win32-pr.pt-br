---
description: A política de tíquete Kerberos é definida no nível de domínio e implementada pelo centro de distribuição de chaves do domínio (KDC).
ms.assetid: 4774218b-7cbd-4e8d-a064-44ebdc37e534
title: Política do Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4559353e65a25a380c0c2aa4bb7e5d56f7681af1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752011"
---
# <a name="kerberos-policy"></a>Política do Kerberos

A política de tíquete Kerberos é definida no nível de domínio e implementada pelo [*centro de distribuição de chaves*](../secgloss/k-gly.md) do domínio (KDC). A política Kerberos é armazenada no Active Directory como um subconjunto dos atributos da política de segurança de domínio. Por padrão, as opções de política podem ser definidas somente por membros do grupo Administradores de domínio. A diretiva de domínio inclui opções que:

-   Dar suporte a tíquetes pós-datados
-   Suporte à delegação restrita (somente Windows Server 2003)
-   Tíquetes de suporte que podem ser encaminhados
-   Dar suporte a tíquetes renováveis
-   Definir idade máxima do tíquete
-   Definir idade de renovação máxima
-   Definir idade máxima do tíquete de proxy
-   Fazer logoff forçado dos usuários quando os tíquetes expiram

Com a [*delegação restrita*](../secgloss/c-gly.md), um computador pode ser definido para permitir o encaminhamento de credenciais somente para uma lista específica de serviços. Esses serviços devem residir no mesmo domínio que o computador que encaminha as credenciais. Sob a *delegação restrita*, os tíquetes não são mais enviados do cliente para o servidor. O computador servidor cria tíquetes de serviço para encaminhar conforme necessário das informações usadas para autenticar o cliente.

Embora a diretiva Kerberos para um domínio possa permitir a autenticação delegada permitindo que os tíquetes sejam encaminhados, esse aspecto da diretiva não precisa se aplicar a todos os usuários ou a todos os computadores. Um atributo de uma conta de usuário individual pode ser definido para desabilitar o encaminhamento das [*credenciais*](../secgloss/c-gly.md) desse usuário por qualquer servidor. Um atributo de uma conta de computador individual pode ser definido para desabilitar o encaminhamento de credenciais de qualquer usuário. Em ambos os casos, a delegação pode ser desabilitada por meio da criação de uma política de grupo para ser aplicada a todos os usuários ou a todos os computadores em uma unidade organizacional do Active Directory.

**Windows XP/2000:** Não há suporte para a delegação restrita.

 

 
