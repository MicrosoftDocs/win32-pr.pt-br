---
title: Definindo Process-Wide segurança
description: Há várias maneiras de definir a segurança de todo o processo.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105768220"
---
# <a name="setting-process-wide-security"></a>Definindo Process-Wide segurança

Há várias maneiras de definir a segurança de todo o processo. A primeira maneira, usando a ferramenta Dcomcnfg.exe, é mais fácil porque não requer programação. A segunda técnica oferece ao programador mais controle e requer uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Outra técnica é definir a segurança de todo o processo no registro usando a chave [AppID](appid-key.md) .

Para obter mais informações sobre essas técnicas, consulte os seguintes tópicos:

-   [Definindo Process-Wide segurança usando DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)
-   [Definindo Process-Wide segurança com CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md)
-   [Configurando a segurança do Process-Wide por meio do registro](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança no nível de proxy da interface](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[Definindo a segurança para aplicativos COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




