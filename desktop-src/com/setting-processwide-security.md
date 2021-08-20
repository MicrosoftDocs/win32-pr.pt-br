---
title: Definindo Process-Wide segurança
description: Há várias maneiras de definir a segurança de todo o processo.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1462cf8ba8922320c1fd3b8ef302166e23a78f516a6e98f22bc6c3968336be79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917945"
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

 

 




