---
title: Com (Com)
description: A identificação é uma funcionalidade de segurança COM que determina qual identidade o cliente projeta em relação ao servidor durante a representação.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5d36ec4561b0cc3290f21f4c46dc338b6df455bc694464812f2274b8c1345f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462940"
---
# <a name="cloaking-com"></a>Com (Com)

A identificação é uma funcionalidade de segurança COM que determina qual identidade o cliente projeta em relação ao servidor durante a representação. Quando a reação é definida, o servidor intermediário mascara sua própria identidade e apresenta a identidade do cliente para o servidor que ele chama em nome do cliente. Basicamente, a identidade do cliente vista pelo servidor é a identidade associada ao proxy. A identidade do proxy é determinada por vários fatores, um dos quais é o tipo de reação definida (se for o caso). Não há suporte para a reação de dados pelo provedor de segurança Schannel.

Os tópicos a seguir fornecem mais informações sobre a ressarção:

-   [Tipos de ressarção](#types-of-cloaking)
-   [Como a ressarção afeta a identidade do cliente](#how-cloaking-affects-client-identity)
-   [Definindo a fixação](#setting-cloaking)
-   [Níveis de redução e representação](#cloaking-and-impersonation-levels)
-   [Cenários de ressarção](#cloaking-scenarios)
-   [Tópicos relacionados](#related-topics)

## <a name="types-of-cloaking"></a>Tipos de ressarção

Há dois tipos de reação: *desastagem* estática e *reação* dinâmica:

-   Com a desastagem estática (EOAC STATIC STATIC, o servidor vê o token de thread da primeira chamada de um \_ \_ cliente para o servidor. Para a primeira chamada, se a identidade do proxy tiver sido definida anteriormente durante uma chamada para [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), essa identidade de proxy será usada. No entanto, se a identidade do proxy não tiver sido definida anteriormente, o token de thread será usado. Se nenhum token de thread estiver presente, o token de processo será usado. Para todas as chamadas futuras, a identidade definida na primeira chamada é usada.
-   Com a desaqueciação dinâmica (EOAC DYNAMIC TAMBÉM), em cada chamada, o token de thread atual (se houver um token de thread) é usado para determinar a identidade \_ \_ do cliente. Se não houver nenhum token de thread, o token de processo será usado. Isso significa que os servidores chamados em nome do cliente durante a representação veem a identidade do cliente COM que originou a chamada, que geralmente é o comportamento desejado. (É claro que, para que a representação seja bem-sucedida, o cliente deve ter dado a autoridade de servidor para representar definindo um nível de representação apropriado. Para obter mais informações, consulte [Níveis de representação](impersonation-levels.md).) Esse tipo de reação é caro.

## <a name="how-cloaking-affects-client-identity"></a>Como a ressarção afeta a identidade do cliente

Quando uma chamada criptografada é feita e o servidor solicita sua identidade ao cliente, ele geralmente obtém a identidade vinculada ao proxy. (Às vezes, o serviço de autenticação executa uma tradução da identidade real, mas geralmente a identidade do proxy é a identidade que o servidor vê.) O proxy apresenta uma identidade para o servidor que depende do tipo de desajuste definido e outros fatores.

Para resumir, a identidade do cliente é uma função do conjunto de sinalizadores de desaqueamento, o token de processo, a presença ou a ausência de um token de thread e se a identidade do proxy foi definida anteriormente. A tabela a seguir mostra a identidade de proxy resultante (identidade do cliente) quando esses fatores variam.



| Sinalizadores de reação                     | Presença de token de thread  | Identidade de proxy definida anteriormente | Identidade de proxy (identidade do cliente)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| A reação não está definida<br/>        | Não se preocupe<br/>  | Não se preocupe<br/>         | Processar token ou identidade de autenticação<br/> |
| EOAC \_ STATIC \_ STATIC STATICING<br/>  | Presente<br/>     | Não<br/>                 | Token de thread<br/>                             |
| EOAC \_ STATIC \_ STATIC STATICING<br/>  | Presente<br/>     | Sim<br/>                | Identidade de proxy atual<br/>                   |
| EOAC \_ STATIC \_ STATIC STATICING<br/>  | Não está presente<br/> | Não<br/>                 | Token de processo<br/>                            |
| EOAC \_ STATIC \_ STATIC STATICING<br/>  | Não está presente<br/> | Sim<br/>                | Identidade de proxy atual<br/>                   |
| EOAC \_ DYNAMIC QUE ESTÁ SENDO \_ DESACOMPACIADO<br/> | Presente<br/>     | Não se preocupe<br/>         | Token de thread<br/>                             |
| EOAC \_ DYNAMIC QUE ESTÁ SENDO \_ DESACOMPACIADO<br/> | Não está presente<br/> | Não se preocupe <br/>        | Token de processo<br/>                            |



 

O fluxograma a seguir ilustra como a identidade do proxy é determinada em situações diferentes.

![Diagrama que mostra o fluxo para determinar a identidade do proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Definindo a fixação

A fixação é definida como um sinalizador de funcionalidade em uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que define a reação de todo o processo. A funcionalidade de fixação é definida até que o cliente o mude por meio de uma chamada para IClientSecurity::[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou para [**CoSetProxyBlanket),**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)que define a redução para o proxy.

Por padrão, a desaquete não está definida. Para defini-lo, passe EOAC \_ STATIC \_ STATICING ou EOAC DYNAMIC CODING para o parâmetro \_ \_ *pCapabilities* em [**CoInitializeSecurity ou**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).

Quando a estática é habilitada usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), cada proxy escolhe um token (thread ou processo) na primeira vez que você faz uma chamada no proxy. Quando a isenção estática é habilitada usando [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), o proxy escolhe o token no thread no momento. Se nenhum token de thread estiver disponível quando **SetBlanket** for chamado, o token de processo será usado para a identidade do proxy. Basicamente, **SetBlanket** corrige a identidade do proxy.

Com a desinformação dinâmica, a identidade do proxy é determinada da mesma maneira, independentemente de a reação dinâmica ser definida usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou com [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). O token de thread atual será usado se houver um; caso contrário, o token de processo será usado.

Se a reação for definida para todo o processo por meio de uma chamada para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e você quiser fazer chamadas com o token de processo, não represente ao fazer chamadas.

## <a name="cloaking-and-impersonation-levels"></a>Níveis de redução e representação

Conforme mencionado anteriormente, a funcionalidade de redução determina qual identidade é apresentada a um servidor durante a representação. A desajuste fornece uma maneira para um servidor projetar uma identidade diferente de sua própria para outro servidor que ele está chamando em nome do cliente. O nível de representação indica a autoridade que o cliente deu ao servidor.

A representação sem desajuste funciona, mas pode não ser a melhor opção porque, em alguns casos, o servidor final precisa saber a identidade do chamador inicial. Isso não pode ser feito sem usar a desarmagem porque é difícil garantir que somente clientes autorizados possam acessar um computador remoto. Quando a representação é usada sem desajuste, a identidade apresentada a um servidor downstream é a do processo de chamada imediata.

No entanto, a redução de dados não é útil sem representação. A redução faz sentido somente quando o cliente definiu um nível de representação de representação ou delegado. (Com níveis de representação inferiores, o servidor não pode fazer chamadas desproporções.) Se a desajuste é bem-sucedida depende do número de limites de computador cruzados e do nível de representação, o que indica a quantidade de autoridade que o servidor precisa agir em nome do cliente.

Em algumas situações, faz sentido para o servidor definir a redução quando o cliente define o nível de representação como RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE. No entanto, determinadas limitações estão em vigor. Se o cliente original define o nível de representação como RPC \_ C \_ IMP LEVEL \_ IMPERSONATE, o servidor intermediário (atuando como um cliente no mesmo computador) pode passar por apenas um limite de \_ computador. Isso porque um token de representação no nível de representação pode ser passado em apenas um limite de computador. Depois que o limite do computador tiver sido cruzado, somente os recursos locais poderão ser acessados. A identidade apresentada ao servidor depende do tipo de desajuste definido. Se nenhuma replicação for definida, a identidade apresentada a um servidor será a do processo que está fazendo a chamada imediata.

Para se apropriar de vários limites de computador, você deve especificar um sinalizador de capacidade de desaprodução apropriado e representação de nível delegado. Com esse tipo de representação, as credenciais locais e de rede do cliente são fornecidas ao servidor, para que o token de representação possa cruzar qualquer número de limites do computador. Novamente, a identidade apresentada ao servidor depende do tipo de desajuste definido. Se nenhuma redução for definida com representação de nível delegado, a identidade apresentada a um servidor será a do processo que está fazendo a chamada.

Por exemplo, suponha que o Processo A chama B e B chama C. B definiu a redução e A definiu o nível de representação para representar. Se A, B e C estiverem no mesmo computador, passar o token de representação de a para B e, em seguida, para C funcionará. Mas se a e C estiverem no mesmo computador e B não estiver, passar o token funcionará entre A e B, mas não de B para C. A chamada de B para C falhará porque B não pode chamar C durante o encobrimento. No entanto, se um definir o nível de representação como delegado, o token poderá ser passado de B para C e a chamada poderá ter êxito.

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

 

