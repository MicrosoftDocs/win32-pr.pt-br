---
title: Configurando a sessão do servidor
description: Configurando a sessão do servidor
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d2710a0d9a0f7f3c70ad6de84336d382ae161b938ee2e22f20ddde5012604
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746586"
---
# <a name="configuring-the-server-session"></a>Configurando a sessão do servidor

A ID de sessão de servidor é criada com a função [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) e usada na chamada para [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). O parâmetro *pPropertyInformation* aponta para a estrutura de configuração para o tipo de propriedade definido. O parâmetro *PropertyInformationLength* especifica o tamanho, em bytes, da estrutura de configuração. Por exemplo, ao definir **HttpServerTimeoutsProperty** , o parâmetro **pPropertyInformation** deve apontar para um buffer que tenha pelo menos o tamanho da estrutura [**de \_ \_ \_ informações de limite de tempo limite http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

Normalmente, um aplicativo HTTP cria uma única sessão de servidor e pode definir propriedades de todo o aplicativo, como o limite de limitação de largura de banda global ou habilitar o log centralizado nessa sessão de servidor. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) substitui as configurações de API do servidor http para o aplicativo de chamada; Ele não afeta as propriedades de toda a API do servidor HTTP. As configurações de sessão de servidor são consultadas chamando [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




