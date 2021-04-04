---
title: Encobrimento (COM)
description: O encobrimento é uma funcionalidade de segurança COM que determina qual identidade o cliente projeta para o servidor durante a representação.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588651cfa37def4e174ef0f2fdba9b79b0c60ca8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103837538"
---
# <a name="cloaking-com"></a>Encobrimento (COM)

O encobrimento é uma funcionalidade de segurança COM que determina qual identidade o cliente projeta para o servidor durante a representação. Quando o encobrimento é definido, o servidor intermediário mascara sua própria identidade e apresenta a identidade do cliente para o servidor que ele chama em nome do cliente. Basicamente a identidade do cliente que é vista pelo servidor é a identidade associada ao proxy. A identidade do proxy é determinada por vários fatores, um dos quais é o tipo de encobrimento definido (se houver). Não há suporte para o encobrimento do provedor de segurança Schannel.

Os tópicos a seguir fornecem mais informações sobre o encobrimento:

-   [Tipos de encobrimento](#types-of-cloaking)
-   [Como o encobrimento afeta a identidade do cliente](#how-cloaking-affects-client-identity)
-   [Configurando o encobrimento](#setting-cloaking)
-   [Níveis de encobrimento e representação](#cloaking-and-impersonation-levels)
-   [Cenários de encobrimento](#cloaking-scenarios)
-   [Tópicos relacionados](#related-topics)

## <a name="types-of-cloaking"></a>Tipos de encobrimento

Há dois tipos de encobrimento: encobrimento *estático* e encobrimento *dinâmico* :

-   Com o encobrimento estático \_ ( \_ encobrimento estático EOAC), o servidor vê o token de thread da primeira chamada de um cliente para o servidor. Para a primeira chamada, se a identidade de proxy tiver sido definida anteriormente durante uma chamada para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), essa identidade de proxy será usada. No entanto, se a identidade de proxy não tiver sido definida anteriormente, o token de thread será usado. Se nenhum token de thread estiver presente, o token de processo será usado. Para todas as chamadas futuras, o conjunto de identidades na primeira chamada é usado.
-   Com o encobrimento dinâmico (EOAC \_ Dynamic \_ encobrimento), em cada chamada, o token de thread atual (se houver um token de thread) é usado para determinar a identidade do cliente. Se não houver nenhum token de thread, o token de processo será usado. Isso significa que os servidores chamados em nome do cliente durante a representação veem a identidade do cliente COM que originou a chamada, que geralmente é o comportamento desejado. (É claro que, para que a representação tenha sucesso, o cliente deve ter dado a autoridade de servidor para representar definindo um nível de representação apropriado. Para obter mais informações, consulte [níveis de representação](impersonation-levels.md).) Esse tipo de encobrimento é caro.

## <a name="how-cloaking-affects-client-identity"></a>Como o encobrimento afeta a identidade do cliente

Quando uma chamada criptografada é feita e o servidor solicita sua identidade ao cliente, ele geralmente obtém a identidade vinculada ao proxy. (Às vezes, o serviço de autenticação executa uma conversão da identidade real, mas geralmente a identidade do proxy é a identidade que o servidor vê.) O proxy apresenta uma identidade para o servidor que depende do tipo de encobrimento definido e de outros fatores.

Para resumir, a identidade do cliente é uma função do conjunto de sinalizadores de encobrimento, o token do processo, a presença ou a ausência de um token de thread e se a identidade do proxy foi definida anteriormente. A tabela a seguir mostra a identidade de proxy resultante (identidade do cliente) quando esses fatores variam.



| Sinalizadores de encobrimento                     | Presença de token de thread  | Identidade de proxy definida anteriormente | Identidade do proxy (identidade do cliente)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Encobrimento não definido<br/>        | Não se preocupe<br/>  | Não se preocupe<br/>         | Token de processo ou identidade de autenticação<br/> |
| \_encobrimento estático EOAC \_<br/>  | Presente<br/>     | No<br/>                 | Token de thread<br/>                             |
| \_encobrimento estático EOAC \_<br/>  | Presente<br/>     | Yes<br/>                | Identidade do proxy atual<br/>                   |
| \_encobrimento estático EOAC \_<br/>  | Não está presente<br/> | No<br/>                 | Token de processo<br/>                            |
| \_encobrimento estático EOAC \_<br/>  | Não está presente<br/> | Yes<br/>                | Identidade do proxy atual<br/>                   |
| \_encobrimento dinâmico EOAC \_<br/> | Presente<br/>     | Não se preocupe<br/>         | Token de thread<br/>                             |
| \_encobrimento dinâmico EOAC \_<br/> | Não está presente<br/> | Não se preocupe <br/>        | Token de processo<br/>                            |



 

O fluxograma a seguir ilustra como a identidade do proxy é determinada em situações diferentes.

![Diagrama que mostra o fluxo para determinar a identidade do proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Configurando o encobrimento

O encobrimento é definido como um sinalizador de recurso em uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que define o encobrimento para todo o processo. Em seguida, o recurso de encobrimento é definido até que o cliente o altere por meio de uma chamada para IClientSecurity::[**setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)), que define o encobrimento para o proxy.

Por padrão, o encobrimento não está definido. Para defini-lo, passe \_ \_ o encobrimento estático EOAC ou \_ \_ o encobrimento dinâmico EOAC para o [](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)parâmetro *pCapabilities* em [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou.

Quando o encobrimento estático é habilitado usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), cada proxy pega um token (thread ou processo) na primeira vez que você faz uma chamada no proxy. Quando o encobrimento estático é habilitado usando [**setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), o proxy pega o token no thread naquele momento. Se nenhum token de thread estiver disponível quando **setampla** for chamado, o token de processo será usado para a identidade do proxy. Basicamente,  corrige a identidade do proxy.

Com o encobrimento dinâmico, a identidade do proxy é determinada da mesma forma, independentemente de o encobrimento dinâmico ser definido usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou com [**setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). O token de thread atual será usado se houver um; caso contrário, o token de processo será usado.

Se o encobrimento estiver definido para todo o processo por meio de uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e você quiser fazer chamadas com o token do processo, não se represente ao fazer chamadas.

## <a name="cloaking-and-impersonation-levels"></a>Níveis de encobrimento e representação

Conforme mencionado anteriormente, o recurso de encobrimento determina qual identidade é apresentada a um servidor durante a representação. O encobrimento fornece uma maneira de um servidor projetar uma identidade diferente de sua própria para outro servidor que está chamando em nome do cliente. O nível de representação indica a quantidade de autoridade que o cliente atribuiu ao servidor.

A representação sem encobrir funciona, mas pode não ser a melhor opção porque, em alguns casos, o servidor final precisa saber a identidade do chamador inicial. Isso não pode ser obtido sem o uso do encobrimento porque é difícil garantir que somente clientes autorizados possam acessar um computador remoto. Quando a representação é usada sem encobrimento, a identidade apresentada a um servidor downstream é a do processo de chamada imediata.

No entanto, o encobrimento não é útil sem representação. O encobrimento faz sentido apenas quando o cliente tiver definido um nível de representação de representar ou delegar. (Com níveis inferiores de representação, o servidor não pode fazer chamadas encobertas.) Se o encobrimento for bem-sucedido, dependerá do número de limites do computador cruzado e do nível de representação, que indica a quantidade de autoridade que o servidor deve agir em nome do cliente.

Em algumas situações, faz sentido que o servidor defina o encobrimento quando o cliente define o nível de representação para a representação do nível de imp do RPC \_ C \_ \_ \_ . No entanto, algumas limitações estão em vigor. Se o cliente original definir o nível de representação para o nível de Requery do RPC \_ C \_ \_ \_ , o servidor intermediário (agindo como um cliente no mesmo computador) poderá se encobrir entre apenas um limite de computador. Isso ocorre porque um token de representação de nível representativo pode ser passado entre apenas um limite de computador. Depois que o limite do computador tiver sido ultrapassado, somente os recursos locais poderão ser acessados. A identidade apresentada ao servidor depende do tipo de encobrimento definido. Se nenhum encobrimento estiver definido, a identidade apresentada a um servidor será a do processo que faz a chamada imediata.

Para encobrir os limites de vários computadores, você deve especificar um sinalizador de recurso de cobertura apropriado e uma representação de nível de delegado. Com esse tipo de representação, as credenciais locais e de rede do cliente são dadas ao servidor, portanto, o token de representação pode cruzar qualquer número de limites de computador. Novamente, a identidade apresentada ao servidor depende do tipo de encobrimento definido. Se nenhum encobrimento for definido com representação de nível delegado, a identidade apresentada a um servidor será a do processo que faz a chamada.

Por exemplo, suponha que o Process A chama B e B chame C. B tenha definido o encobrimento e um tenha definido o nível de representação como Impersonate. Se A, B e C estiverem no mesmo computador, passar o token de representação de a para B e, em seguida, para C funcionará. Mas se a e C estiverem no mesmo computador e B não estiver, passar o token funcionará entre A e B, mas não de B para C. A chamada de B para C falhará porque B não pode chamar C durante o encobrimento. No entanto, se um definir o nível de representação como delegado, o token poderá ser passado de B para C e a chamada poderá ter êxito.

## <a name="cloaking-scenarios"></a>Cenários de encobrimento

Na ilustração a seguir, processe uma chamada B, chamadas C, chamadas D quando o encobrimento não está definido. Como resultado, cada processo intermediário vê a identidade do processo que o chamou.

![Diagrama que mostra o processo quando o encobrimento não está definido.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Com o encobrimento estático, o servidor vê a identidade do proxy que foi definida durante a primeira chamada do cliente para o servidor. A figura a seguir mostra um exemplo da identidade do proxy que está sendo definida durante uma chamada de B para C. Em uma chamada subsequente, o processo D vê a identidade de B quando o encobrimento estático é definido por B e C.

![Diagrama que mostra o processo de encobrimento estático.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Com o encobrimento dinâmico, a identidade do chamador durante a representação é baseada no token do thread atual, se houver. A ilustração a seguir mostra a situação em que B e C definem o encobrimento dinâmico e D vê a identidade de A, apesar de uma chamada anterior de B para C.

![Diagrama que mostra o processo de encobrimento dinâmico.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Delegação e representação](delegation-and-impersonation.md)
</dt> </dl>

 

