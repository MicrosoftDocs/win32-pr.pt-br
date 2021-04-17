---
description: NOUSEROVERRIDE de localidade \_
ms.assetid: ab68d16b-5e1e-4af3-b048-43975cded00a
title: LOCALE_NOUSEROVERRIDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28c2f59358bf71936e3a812c10e061d7a169387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748993"
---
# <a name="locale_nouseroverride"></a>NOUSEROVERRIDE de localidade \_

> [!Caution]  
> Como \_ a localidade NOUSEROVERRIDE desabilita as preferências do usuário, seu uso é altamente desencorajado. Essa constante não garante a estabilidade dos dados, pois as [localidades personalizadas](custom-locales.md), as atualizações de serviço, as diferentes versões do sistema operacional e outros cenários podem alterar os dados de maneiras inesperadas. Para obter mais informações, consulte [usando dados de localidade persistente](using-persistent-locale-data.md).

 

Nenhuma substituição do usuário. Em várias funções, por exemplo, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) e [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex), essa constante faz com que a função ignore qualquer substituição de usuário e use o valor padrão do sistema para qualquer outra constante especificada na chamada de função. As informações são recuperadas do banco de dados de localidade, mesmo se o identificador indicar a localidade atual e o usuário tiver alterado alguns dos valores usando o painel de controle ou se um aplicativo tiver alterado esses valores usando [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa). Se essa constante não for especificada, quaisquer valores que o usuário tiver configurado no painel de controle ou que um aplicativo tenha configurado usando [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa) têm precedência sobre as configurações de banco de dados para a localidade padrão do sistema atual.

 

 



