---
title: Modificando os padrões de segurança para um computador
description: Modificando os padrões de segurança para um computador
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7936e2d0bc1113b651fd40f94e84037f00f4ffbe12b7e0232f1dc6a6cd8aaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105394"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a>Modificando os padrões de segurança para um computador

Não é recomendável que você altere as configurações de segurança em todo o sistema, pois isso afetará todos os aplicativos de servidor COM que não configuram sua própria segurança em todo o processo e podem impedi-los de funcionar corretamente. Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um aplicativo COM específico, deverá alterar as configurações de segurança em todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança em todo o processo, consulte [Configurando Process-Wide Segurança](setting-processwide-security.md).

Determinados valores no Registro determinam as configurações de segurança para aplicativos que não chamam [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Você pode modificar essas configurações usando Dcomcnfg.exe.

Para obter mais informações, consulte estes tópicos:

-   [Valores do Registro para System-Wide Segurança](registry-values-for-machine-wide-security.md)
-   [Definindo System-Wide segurança usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando a segurança em todo o processo](setting-processwide-security.md)
</dt> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




