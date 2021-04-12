---
title: Modificando os padrões de segurança de um computador
description: Modificando os padrões de segurança de um computador
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363641"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modificando os padrões de segurança de um computador

Não é recomendável que você altere as configurações de segurança de todo o sistema, pois isso afetará todos os aplicativos de servidor COM que não definem sua própria segurança de todo o processo e pode impedi-los de funcionar corretamente. Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um determinado aplicativo COM, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [setting Process-Wide Security](setting-processwide-security.md).

Determinados valores no registro determinam as configurações de segurança para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Você pode modificar essas configurações usando Dcomcnfg.exe.

Para mais informações, consulte os seguintes tópicos:

-   [Valores de registro para segurança de System-Wide](registry-values-for-machine-wide-security.md)
-   [Definindo System-Wide segurança usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




