---
title: Caça de referência com IDirectorySearch
description: Uma referência é o mecanismo que um servidor de diretório usa para direcionar um cliente para outro servidor quando ele não contém dados suficientes sobre o objeto solicitado por uma consulta.
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- Caça de referência com IDirectorySearch ADSI
- ADSI, pesquisa, IDirectorySearch, outras opções de pesquisa, caça de referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917676"
---
# <a name="referral-chasing-with-idirectorysearch"></a>Caça de referência com IDirectorySearch

Uma referência é o mecanismo que um servidor de diretório usa para direcionar um cliente para outro servidor quando ele não contém dados suficientes sobre o objeto solicitado por uma consulta.

Em uma pesquisa de um nível ou de subárvore, as referências são retornadas apenas para contêineres de domínio, esquema ou configuração conhecidos, imediatamente subordinados; ou seja, os domínios filho que são descendentes diretos. Para obter mais informações, consulte [escopo da pesquisa](/windows/desktop/AD/search-scope).

Em um diretório, nem todos os dados estão disponíveis em um único servidor, em vez disso, eles são distribuídos por vários servidores diferentes pela rede. Se os servidores compartilharem os dados que outros servidores podem fornecer, eles poderão fornecer referências a um cliente quando uma consulta solicitada não puder ser resolvida no servidor de origem. Por exemplo, quando um cliente solicita ao servidor A para consultar um objeto de usuário (U), um pode sugerir que o cliente continue a pesquisa no servidor B se U não residir em um, mas é identificado como em B. O cliente tem a opção de buscar a referência ou não. As referências liberam o cliente de ter que ter conhecimento prévio da capacidade de cada servidor, mas o cliente deve especificar o tipo de referências que um servidor deve executar.

Para habilitar ou desabilitar a busca de referência, defina uma opção de pesquisa de **referências do ADS \_ SEARCHPREF \_ Chase \_** com um valor **\_ inteiro ADSTYPE** que contenha um dos [**anúncios \_ Chase \_ referências \_ enum**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) valores de enumeração na matriz de [**\_ \_ informações de SEARCHPREF do ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passada para o método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

O exemplo de código a seguir mostra como habilitar referências de Chase.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



Para obter mais informações sobre referências no Active Directory, consulte [referências](/windows/desktop/AD/referrals).

 

 