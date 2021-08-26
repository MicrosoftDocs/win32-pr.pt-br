---
title: Determinando suas necessidades de segurança
description: A maneira como você configura a segurança COM para seu aplicativo depende de qual tipo de segurança seu aplicativo precisa. Há várias situações comuns que determinam o que você deve fazer.
ms.assetid: db5c9adb-b04b-4621-b738-2959cac40985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57ccbbc8fc96b7c94e90fd3925dfb2ffff07225c34ebe1da34353f42b08b3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993226"
---
# <a name="determining-your-security-needs"></a>Determinando suas necessidades de segurança

A maneira como você configura a segurança COM para seu aplicativo depende de qual tipo de segurança seu aplicativo precisa. Há várias situações comuns que determinam o que você deve fazer.

Se você decidir usar os padrões de segurança COM, não precisará fazer anythingâ € "COM tudo isso. Para obter informações sobre o que são essas configurações padrão, consulte [padrões de segurança com](com-security-defaults.md).

Você também pode impedir qualquer chamada remota em seu computador desabilitando totalmente o DCOM (COM entre computadores remotos). Para obter mais informações, consulte [definindo System-Wide segurança usando DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).

Para aplicativos herdados ou novos, você pode definir a segurança de todo o processo no registro. Para obter mais informações, consulte [Configurando a segurança do processwide por meio do registro](setting-processwide-security-through-the-registry.md).

Você também pode substituir as configurações de segurança padrão para chamadas para determinadas interfaces no processo ao definir a segurança padrão para o restante do processo (para permitir que o COM manipule os casos gerais). Para obter mais informações, consulte [definindo a segurança no nível de proxy da interface](setting-security-at-the-interface-proxy-level.md).

Para requisitos de segurança complexos, você pode manipular toda a segurança programaticamente, em vez de permitir que o COM a manipule para você. Para fazer isso, chame [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para desabilitar a autenticação automática e, em seguida, controle todas as configurações de segurança definindo a segurança em uma base proxy por interface. Para obter mais informações, consulte [definindo a segurança do processwide com CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md) e [definindo a segurança no nível do proxy da interface](setting-security-at-the-interface-proxy-level.md).

Em alguns cenários, talvez você queira desativar completamente a segurança. Você pode decidir que seu aplicativo não precisa de segurança, ou talvez você queira desabilitar a segurança durante o tempo de desenvolvimento para que você possa habilitar os recursos de segurança individualmente. Para saber como desabilitar a segurança COM, consulte [desativando a segurança](turning-off-security.md).

A segurança em COM conta COM os serviços de autenticação administrados por pacotes de segurança. O NTLMSSP funciona bem para muitos aplicativos, mas não fornece a segurança mais robusta oferecida por outros pacotes. Portanto, o COM dá suporte ao pacote de segurança Schannel e ao protocolo de segurança Kerberos v5. Para obter mais detalhes sobre como usar esses pacotes de segurança, consulte [pacotes de segurança e com](com-and-security-packages.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




