---
title: Indicação de busca com IDirectorySearch
description: Uma indicação é o mecanismo que um servidor de diretório usa para direcionar um cliente para outro servidor quando ele não contém dados suficientes sobre o objeto solicitado por uma consulta.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Busca de indicação com ADSI de IDirectorySearch
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, busca de indicação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7fcc74103c5c09816976e9ff91c17ecca8578fcbf596b731df890a350e922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690685"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Indicação de busca com IDirectorySearch

Uma indicação é o mecanismo que um servidor de diretório usa para direcionar um cliente para outro servidor quando ele não contém dados suficientes sobre o objeto solicitado por uma consulta.

Em uma pesquisa de um nível ou subárvore, as indicações são retornadas apenas para contêineres de configuração, esquema ou domínio subordinados conhecidos e imediatamente subordinados; ou seja, domínios filho que são descendentes diretos. Para obter mais informações, consulte [Escopo da pesquisa.](/windows/desktop/AD/search-scope)

Em um diretório, nem todos os dados estão disponíveis em um único servidor, em vez disso, eles são distribuídos em vários servidores diferentes pela rede. Se os servidores compartilharem os dados que outros servidores podem fornecer, eles poderão fornecer indicações a um cliente quando uma consulta solicitada não puder ser resolvida no servidor de origem. Por exemplo, quando um cliente solicita ao Servidor A para consultar um U (objeto de usuário), A pode sugerir que o cliente continue a pesquisa no Servidor B se U não residir em A, mas for identificado como B. O cliente tem a opção de buscar a indicação ou não. As indicações liberam o cliente de ter conhecimento anterior da funcionalidade de cada servidor, mas o cliente deve especificar o tipo de indicações que um servidor deve executar.

Para habilitar ou desabilitar a busca de indicação, de definir uma opção de pesquisa **ADS \_ SEARCHPREF \_ SEARCH \_ REFERRALS** com um valor **INTEIRO ADSTYPE \_** que contém um dos valores de enumeração ENUM ADS [**\_ SEARCH \_ REFERRALS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) na matriz ADS [**\_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

O exemplo de código a seguir mostra como habilitar indicações de busca.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Para obter mais informações sobre indicações no Active Directory, consulte [Indicações](/windows/desktop/AD/referrals).

 

 