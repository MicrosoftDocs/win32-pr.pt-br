---
title: Definindo Process-Wide segurança com CoInitializeSecurity
description: A função CoInitializeSecurity permite controlar cenários complexos de segurança definindo a segurança para um aplicativo programaticamente.
ms.assetid: 20b66868-fb9a-489f-97a2-59a8a825c8d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c3e601897e9f2313682a3474c1760bc211285d8fa81a82f67d114681a7a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610886"
---
# <a name="setting-process-wide-security-with-coinitializesecurity"></a>Definindo Process-Wide segurança com CoInitializeSecurity

A [**função CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) permite controlar cenários complexos de segurança definindo a segurança para um aplicativo programaticamente. Este tópico descreve cenários em que você pode usar **o CoInitializeSecurity** e fornece alguns detalhes sobre como usá-lo.

Há vários motivos pelos quais você pode querer usar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança em todo o processo em seu programa. Por exemplo, embora você possa definir o nível de autenticação e as permissões de acesso para o aplicativo usando dcomcnfg.exe, o nível de representação padrão para o computador pode não ser aquele que você deseja para seu processo. A única maneira de alterar essa configuração para seu processo é chamar **CoInitializeSecurity**.

Se você quiser usar o provedor de segurança Schannel, deverá especificá-lo como um serviço de autenticação em uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).

Outro cenário comum no qual você pode definir a segurança em todo o processo programaticamente é quando você gostaria de definir a segurança padrão para todo o processo, mas você tem um ou mais objetos dentro desse processo que expõem interfaces com requisitos de segurança especiais. Nesse caso, você pode chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança para o processo, permitindo que o COM processe a maioria das verificações de segurança e você pode chamar outros métodos para definir a segurança para os objetos com necessidades especiais de segurança. Chamar esses métodos e funções é descrito em [Definindo segurança no nível de proxy da interface](setting-security-at-the-interface-proxy-level.md).

Se seu aplicativo tiver requisitos de segurança muito especializados, como permitir que determinados grupos acessem objetos diferentes dependendo da hora do dia, talvez você queira lidar com toda a sua segurança programaticamente, garantindo que o COM não faça nenhuma verificação automática para você. Para fazer isso, você deve chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), definindo o parâmetro *dwAuthnLevel* como none e o *parâmetro pVoid* como **NULL.** Se você tiver seu próprio pacote de segurança, também precisará registrá-lo no *parâmetro pAuthnSvc.* Em seguida, você pode lidar com toda a sua própria segurança programaticamente por meio de chamadas para a interface de nível de proxy e funções descritas em Configurando segurança no [nível de proxy da interface](setting-security-at-the-interface-proxy-level.md).

[**O CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) oferece um conjunto rico de recursos. Se você chamar **CoInitializeSecurity**, os valores do Registro serão ignorados e os valores de inicialização de segurança que você passar para a chamada serão usados. Dependendo do resultado que você deseja, o primeiro parâmetro, *pVoid,* pode apontar para três tipos diferentes de valores: [**um SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) , um [**objeto IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) ou um ponteiro para um AppID. Na maioria dos casos, você usará Windows funções para criar um **\_ DESCRITOR DE SEGURANÇA** para o que *pVoid* apontará.

No entanto, *pVoid* também pode apontar para um [**objeto IAccessControl.**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol)

Para indicar ao [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) que você está passando um objeto [**IAccessControl**](/windows/desktop/api/IAccess/nn-iaccess-iaccesscontrol) para *pVoid*, você deve passar o valor de EOAC ACCESS CONTROL para o parâmetro \_ \_ *dwCapabilities.* Como **CoInitializeSecurity** armazena em cache os resultados das verificações de acesso, a lista de controle de acesso não deve ser alterada depois de chamar **CoInitializeSecurity**.

Outro tipo de valor que você pode passar para o *parâmetro pVoid* é um ponteiro para um GUID, que é o AppID do seu aplicativo. Se *pVoid* for um ponteiro para uma AppID, você deverá especificar EOAC APPID no parâmetro pCapabilities para que a função saiba qual valor esperar \_ em *pVoid*.  Se *pVoid* aponta para uma [**AppID, CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) usa apenas o Registro para valores de autenticação e ignora todos os outros parâmetros para **CoInitializeSecurity**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 