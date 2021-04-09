---
description: Definições de configuração do localizador de proxy
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Definições de configuração do localizador de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3503a90bcccc990865769b6bf02a65fc383511f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091039"
---
# <a name="proxy-locator-configuration-settings"></a>Definições de configuração do localizador de proxy

Este tópico descreve as definições de configuração para o localizador de proxy padrão. Para obter informações sobre como criar o localizador de proxy com definições de configuração personalizadas, consulte [como configurar o localizador de proxy](how-to-configure-the-proxy-locator.md).

O localizador de proxy pode ser configurado para operar em três modos: *modo manual*, *modo de detecção automática* e *modo de navegador*. Os valores são definidos na enumeração [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) . O aplicativo pode configurar o modo definindo a propriedade [**MFNETSOURCE \_ PROXYSETTINGS**](mfnetsource-proxysettings-property.md) . O localizador de proxy também pode ser configurado para não usar um servidor proxy definindo essa propriedade como **MFNET \_ PROXYSETTING \_ None**. O servidor proxy não será usado se o servidor de mídia for um host local ou o aplicativo solicitar uma classe um endereço (127. x. x. x) — reservado para testes de loopback.

> [!Caution]  
> Um servidor proxy é uma barreira de segurança entre a intranet e a Internet. Não usar um servidor proxy pode expor a rede a ameaças de segurança.

 

-   Modo manual. O aplicativo define esse modo definindo a propriedade [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) como **MFNET \_ PROXYSETTING \_ manual**. O aplicativo deve especificar as seguintes informações de conexão:

    -   Nome do host do servidor proxy: propriedade [**MFNETSOURCE \_ PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) .
    -   Número da porta: propriedade [**MFNETSOURCE \_ PROXYPORT**](mfnetsource-proxyport-property.md) .
    -   Se um servidor proxy deve ser usado para endereços locais: propriedade [**MFNETSOURCE \_ PROXYBYPASSFORLOCAL**](mfnetsource-proxybypassforlocal-property.md) . Essa configuração é opcional. Se isso não for especificado, o localizador de proxy usará um valor padrão de **false**.

        > [!Note]  
        > Ignorando o servidor proxy, o aplicativo pode ser capaz de se conectar a servidores de mídia na intranet mais rapidamente.

         

    -   Lista de endereços de servidor de mídia que não exigem um servidor proxy para estabelecer uma conexão: [**MFNETSOURCE \_ PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) propriedade. Essa configuração é opcional.

-   Modo de detecção automática. O aplicativo define esse modo definindo a propriedade [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) como **MFNET \_ PROXYSETTING \_ auto**. Nesse modo, o localizador de proxy usa o mecanismo do WinHTTP AutoProxy para obter o nome do host e o número da porta para o servidor proxy. Essas informações de conexão são recuperadas usando o script de proxy de WPAD, que é configurado pelo administrador de domínio. Para obter mais informações sobre esse mecanismo, consulte o [site da Microsoft](../winhttp/winhttp-autoproxy-support.md).

    O localizador de proxy armazena em cache as informações de conexão no registro. Em chamadas de detecção de proxy subsequentes, o localizador de proxy lê as informações de proxy do cache do registro para reduzir a sobrecarga envolvida na detecção automática. No entanto, o aplicativo pode forçar a detecção automática de proxy, definindo a propriedade [**MFNETSOURCE \_ PROXYRERUNAUTODETECTION**](mfnetsource-proxyrerunautodetection-property.md) .

-   Modo de navegador. O aplicativo define esse modo definindo a propriedade [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) como **MFNET \_ PROXYSETTING \_ browser**. Nesse modo, o localizador de proxy usa as configurações de proxy do aplicativo de navegador. Esse modo é definido por padrão se o protocolo for HTTP ou HTTP.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte de proxy para fontes de rede](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
