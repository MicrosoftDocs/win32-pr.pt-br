---
title: Configurando a sessão do servidor
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761727"
---
# <a name="configuring-the-server-session"></a>Configurando a sessão do servidor

A ID de sessão de servidor é criada com a função [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) e usada na chamada para [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). O parâmetro *pPropertyInformation* aponta para a estrutura de configuração para o tipo de propriedade definido. O parâmetro *PropertyInformationLength* especifica o tamanho, em bytes, da estrutura de configuração. Por exemplo, ao definir **HttpServerTimeoutsProperty** , o parâmetro **pPropertyInformation** deve apontar para um buffer que tenha pelo menos o tamanho da estrutura [**de \_ \_ \_ informações de limite de tempo limite http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

Normalmente, um aplicativo HTTP cria uma única sessão de servidor e pode definir propriedades de todo o aplicativo, como o limite de limitação de largura de banda global ou habilitar o log centralizado nessa sessão de servidor. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) substitui as configurações de API do servidor http para o aplicativo de chamada; Ele não afeta as propriedades de toda a API do servidor HTTP. As configurações de sessão de servidor são consultadas chamando [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




