---
title: Valores de registro para segurança de System-Wide
description: Valores de registro para segurança de System-Wide
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916133"
---
# <a name="registry-values-for-system-wide-security"></a>Valores de registro para segurança de System-Wide

Não é recomendável que você altere as configurações de segurança de todo o sistema, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente. Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um determinado aplicativo COM, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [setting Process-Wide Security](setting-processwide-security.md).

Determinados valores no registro são usados para determinar as configurações de segurança para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Você pode usar Dcomcnfg.exe para modificar essas configurações de segurança padrão para um computador. Para obter procedimentos passo a passo que descrevem como usar Dcomcnfg.exe para essa finalidade, consulte Definindo a [segurança de System-Wide usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Outra maneira de alterar as configurações padrão de todo o sistema é manipular valores de registro diretamente. No entanto, somente administradores e o sistema têm acesso total à parte do registro que contém as configurações padrão de segurança de chamada do sistema. Todos os outros usuários têm acesso somente leitura.

Os valores nomeados que afetam os padrões de segurança em todo o sistema são os seguintes:

-   [DefaultLaunchPermission](defaultlaunchpermission.md)
-   [DefaultAccessPermission](defaultaccesspermission.md)
-   [LegacyAuthenticationLevel](legacyauthenticationlevel.md)
-   [LegacyImpersonationLevel](legacyimpersonationlevel.md)
-   [LegacySecureReferences](legacysecurereferences.md)
-   [SRPRunningObjectChecks](srprunningobjectchecks.md)
-   [SRPActivateAsActivatorChecks](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 




