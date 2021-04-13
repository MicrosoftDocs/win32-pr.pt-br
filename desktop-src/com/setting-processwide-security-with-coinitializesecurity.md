---
title: Definindo Process-Wide segurança com CoInitializeSecurity
description: A função CoInitializeSecurity permite controlar cenários de segurança complexos definindo a segurança de um aplicativo programaticamente.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567a6dfaf47dbd278fc248558cd25969c733b24a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366773"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Definindo Process-Wide segurança com CoInitializeSecurity

A função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) permite controlar cenários de segurança complexos definindo a segurança de um aplicativo programaticamente. Este tópico descreve os cenários em que você pode usar **CoInitializeSecurity** e fornece alguns detalhes sobre como usá-lo.

Há várias razões pelas quais você pode querer usar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança em todo o processo em seu programa. Por exemplo, embora você possa definir o nível de autenticação e as permissões de acesso para o aplicativo usando dcomcnfg.exe, o nível de representação padrão para o computador pode não ser o que você deseja para seu processo. A única maneira de alterar essa configuração para seu processo é chamar **CoInitializeSecurity**.

Se você quiser usar o provedor de segurança Schannel, deverá especificá-lo como um serviço de autenticação em uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Outro cenário comum no qual você pode definir a segurança de todo o processo de forma programática é quando você deseja definir a segurança padrão para todo o processo, mas você tem um ou mais objetos dentro desse processo que expõem interfaces com requisitos de segurança especiais. Nesse caso, você pode chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança para o processo, permitindo que o com manipule a maioria das verificações de segurança, e você pode chamar outros métodos para definir a segurança para os objetos com necessidades de segurança especiais. Chamar esses métodos e funções é descrito em [definindo a segurança no nível do proxy da interface](setting-security-at-the-interface-proxy-level.md).

Se seu aplicativo tiver requisitos de segurança muito especializados, como permitir que determinados grupos acessem objetos diferentes dependendo da hora do dia, você talvez queira lidar com toda a segurança de forma programática, garantindo que o COM não faça nenhuma verificação automática. Para fazer isso, você deve chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), definindo o parâmetro *dwAuthnLevel* como None e o parâmetro *pVoid* como **NULL**. Se você tiver seu próprio pacote de segurança, também precisará registrá-lo no parâmetro *pAuthnSvc* . Em seguida, você pode manipular toda a sua segurança programaticamente por meio de chamadas para a interface de nível de proxy e funções descritas em [definindo a segurança no nível de proxy da interface](setting-security-at-the-interface-proxy-level.md).

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oferece um conjunto avançado de recursos. Se você chamar **CoInitializeSecurity**, os valores do registro serão ignorados e os valores de inicialização de segurança que você passar para a chamada serão usados em vez disso. Dependendo do resultado desejado, o primeiro parâmetro, *pVoid*, pode apontar para três tipos diferentes de valores: um [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , um objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ou um ponteiro para um AppID. Na maioria dos casos, você usará as funções do Windows para criar um **\_ descritor de segurança** para o qual *pVoid* apontará.

No entanto, o *pVoid* também pode apontar para um objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) .

Para indicar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) que você está passando um objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) para *pVoid*, você deve passar o \_ valor de controle de acesso EOAC \_ para o parâmetro *dwCapabilities* . Como **CoInitializeSecurity** armazena em cache os resultados das verificações de acesso, a lista de controle de acesso não deve ser alterada depois de chamar **CoInitializeSecurity**.

Outro tipo de valor que você pode passar para o parâmetro *pVoid* é um ponteiro para um GUID, que é o AppID do seu aplicativo. Se *pVoid* for um ponteiro para uma AppID, você deverá especificar EOAC \_ AppID no parâmetro *pCapabilities* para que a função saiba qual valor esperar em *pVoid*. Se *pVoid* apontar para um AppID, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) usará apenas o registro para valores de autenticação e ignorará todos os outros parâmetros para **CoInitializeSecurity**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 