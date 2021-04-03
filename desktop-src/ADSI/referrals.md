---
title: Referências (ADSI)
description: As referências ocorrem quando o servidor que você está consultando não contém esses dados, mas pode encontrá-los.
ms.assetid: 2068ce7a-0b94-4d25-a18f-97f26863bd1d
ms.tgt_platform: multiple
keywords:
- ADSI de referências
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79e6b2e8a737f6bb40386effd68f7f31d8d490d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084888"
---
# <a name="referrals-adsi"></a>Referências (ADSI)

As referências ocorrem quando o servidor que você está consultando não contém esses dados, mas pode encontrá-los. O servidor de destino retorna o conjunto de resultados, que pode incluir os dados reais e uma referência a outro servidor para recuperar os dados adicionais. Ao habilitar a busca de *referência*, o código de cliente ADSI subjacente usará esses dados de referência para tentar recuperar o objeto de destino do servidor descrito nos dados de referência. Lembre-se de que a busca de referência de desabilitação pode resultar em um conjunto de resultados menor, enquanto a habilitação da pesquisa de referência pode fazer com que uma consulta abranja vários servidores. Quando possível, a solução recomendada é usar o catálogo global.

Para obter mais informações sobre referências e busca de referência em Active Directory, consulte [referências](/windows/desktop/AD/referrals).

Por exemplo, quando um cliente instrui o servidor A (A) para consultar um objeto de usuário (U), um pode sugerir que o cliente continue a pesquisa no servidor B (B) se o U não residir em um, mas é conhecido como em B. O cliente tem a opção de obter a referência ou não. As referências de pesquisa liberam o cliente de exigir o reconhecimento avançado da capacidade de cada servidor. No entanto, o cliente deve especificar o tipo de referências que um servidor deve fazer.

Active Directory oferece serviços de referência de pesquisa. Um cliente pode escolher qualquer um dos seguintes tipos de caça de referência:

-   Nunca: o servidor não deve gerar uma referência a um cliente, mesmo que ele reconheça que outro servidor armazena os dados solicitados.
-   Externo: o servidor deve gerar referências se a solicitação puder ser resolvida em outro servidor de uma árvore de diretórios diferente. Por exemplo, um cliente consulta "OU = Sales, DC = Fabrikam, DC = COM" no servidor "fab01" no domínio "Fabrikam.com". No entanto, o objeto não pertence a "fab01", mas é conhecido como no servidor "arc01" no domínio "Fabrikam.com". Portanto, "fab01" faz referência ao cliente para "arc01".
-   Subordinado: o servidor deve gerar referências se a solicitação puder ser resolvida em um servidor cujo nome forma um caminho contíguo do servidor de origem. O escopo da pesquisa deve estar no nível da subárvore.

    Por exemplo, o servidor A contém objetos em "DC = Sales, DC = Fabrikam, DC = com". O servidor B contém objetos em "DC = Seattle, DC = Sales, DC = Fabrikam, DC = com". Lembre-se de que o nome do servidor B forma um caminho contíguo do servidor A. Quando um cliente contata o servidor A, o solicita uma pesquisa de subárvore em "DC = Sales, DC = Fabrikam, DC = com" e especifica a referência a ser um tipo subordinado, o seguinte evento ocorre:

    -   O servidor A retorna todos os objetos que ele conhece em seu escopo.
    -   O servidor A informa ao cliente que os objetos em "DC = Seattle, DC = Sales, DC = Fabrikam, DC = COM" podem ser encontrados no servidor B.

    O cliente pode optar por contatar o servidor B. Nesse caso, ocorre o seguinte evento:

    -   O servidor B responde com os objetos solicitados.
    -   Se o servidor B detectar outros servidores no caminho de nomenclatura contíguo e o processo continuar.

-   Sempre: o servidor gerará referências se a pesquisa puder ser resolvida com base no tipo externo ou no tipo subordinado.

> [!Note]  
> No Active Directory, o catálogo global contém todos os objetos em uma determinada empresa. Pesquisar um servidor de catálogo global produz um desempenho melhor do que a busca de referências de um servidor para outro.

 

Na maioria dos casos, a caça de referência será transparente para o chamador. Se a referência for para um objeto em um domínio ou floresta diferente, a API LDAP subjacente tentará usar as credenciais atuais para associar ao destino da referência. Se isso for bem-sucedido, a caça de referência será transparente. Se isso não for bem-sucedido, a referência e um código de erro de referência serão retornados.

Para obter mais informações sobre como usar as opções de caça de referência com uma interface de pesquisa específica, consulte:

-   [Caça de referência com IDirectorySearch](referral-chasing-with-idirectorysearch.md)
-   [Pesquisando com ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Pesquisando com OLE DB](searching-with-ole-db.md)

 

 