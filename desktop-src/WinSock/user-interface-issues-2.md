---
description: Uma das alterações mais óbvias de IPv4 para IPv6 é o tamanho do endereço IP. Muitas interfaces de usuário fornecem caixas de diálogo que permitem que um usuário insira um endereço IP, como exemplificado na figura a seguir.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Problemas de interface do usuário para aplicativos Winsock do IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764415"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Problemas de interface do usuário para aplicativos Winsock do IPv6

Uma das alterações mais óbvias de IPv4 para IPv6 é o tamanho do endereço IP. Muitas interfaces de usuário fornecem caixas de diálogo que permitem que um usuário insira um endereço IP, como exemplificado na figura a seguir.

![caixa de endereço IPv4 comum em uma interface do usuário](images/portingguide001.jpg)

O endereçamento no IPv6, devido a muitos fatores, como comprimento, complexidade e o significado das seções dentro do espaço de endereço IPv6, não é voltado para modificação ou especificação por usuários. Portanto, a necessidade de fornecer aos usuários a capacidade de especificar seu próprio endereço é reduzida. Além disso, devido à complexidade associada ao endereçamento IPv6, é provável que os administradores com a capacidade de especificar informações de endereço IPv6 não ocorram em uma base por nó.

A exibição de um endereço IPv6 na interface do usuário não é inconcebível e, portanto, os desenvolvedores devem considerar a variabilidade no tamanho de um endereço IPv6 ao modificar um aplicativo para dar suporte a IPv6.

O restante desta seção aborda a diferença entre a previsibilidade de comprimento de endereço IPv4 e as considerações de comprimento de endereço IPv6. Esta seção presume que os endereços IPv6 estejam sendo exibidos em sua representação hexadecimal.

Os endereços IPv4 são previsíveis em tamanho, pois eles seguem rigidamente a notação decimal pontilhada, como ilustra o seguinte exemplo de endereço:

``` syntax
10.10.256.1
```

Os endereços IPv6 não são tão previsíveis, devido à Convenção de endereço IPv6 que permite o uso de dois-pontos duplos (::) para representar uma série de zeros. Assim, as seguintes representações de endereço IPv6 são equivalentes ao mesmo endereço IPv6:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

A capacidade de representar uma série de zeros com dois pontos duplos resulta em um comprimento imprevisível para qualquer IPv6 específico, o que exige que os programadores Tomem essa capacidade em consideração ao criar exibições de interface do usuário de endereços IPv6. Certamente, os desenvolvedores devem garantir que a interface do usuário seja capaz de exibir endereços IP que não usam dois-pontos duplos para representar uma série de zeros (primeiro endereço abaixo), além de ser capaz de exibir o endereço IPv6 mais longo possível (segundo endereço abaixo, com o endereço IPv4 inserido) ao criar sua interface de usuário compatível com IPv6. Observe também que a adição do identificador de escopo (ID) para o seguinte endereço aumentaria seu comprimento até outros onze caracteres:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Outra consideração importante é se os endereços baseados em nome são mais apropriados do que os endereços IPv6 baseados em número. Se os endereços baseados em nome forem mais apropriados, a consideração para convenções de nomenclatura deve ser incorporada à interface do usuário, incluindo qualquer verificação de erro de entrada apropriada para a tarefa.

Há outras complexidades associadas à exibição de endereços IPv6 que os desenvolvedores devem levar em consideração ao modificar seus aplicativos e ao criar representações de interface do usuário de endereços IPv6. Algumas dessas considerações são as seguintes:

-   O endereço deve conter todas as sequências de zeros ou usar a notação de dois-pontos duplo?
-   É mais apropriado usar uma representação de endereço baseada em número ou uma representação baseada em nome?
-   O usuário está interessado em discernir um determinado aspecto do esquema de endereçamento, como o prefixo de sub-rede, o identificador de escopo ou outros subcampos?
-   O usuário está interessado em determinar outros aspectos do endereço, como o identificador TLA, o identificador de NLA ou o identificador SLA?
-   Sua interface do usuário será capaz de distinguir endereços IPv6 incorporados e, nesse caso, como eles serão tratados e exibidos? Você fará discernimento entre endereços compatíveis com IPv4 e endereços IPv6 mapeados por IPv4 ao exibir informações de endereço para o usuário?

Também há outras considerações, e os desenvolvedores devem considerar cuidadosamente seu público-alvo do cliente ao desenvolver interfaces de usuário de endereço IP.

Práticas Recomendadas

-   Os desenvolvedores devem considerar a abordagem apropriada para cada interface do usuário ao modificar seu aplicativo para dar suporte a IPv6. Garantir que a interface do usuário contenha comprimento suficiente para exibir endereços IPv6 é imperativo, como está determinando se esse endereço é baseado em número ou nome.
-   Sempre que possível, use as funções Winsock e IP auxiliar existentes ao usar endereços IPv6 em vez de implementar novamente essa lógica. Por exemplo, as funções [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa), [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw), [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)e [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) podem ser usadas para converter entre os endereços IPv6 e representações de cadeia de caracteres desses endereços IPv6.

Código a ser evitado

-   Os elementos da interface do usuário que dependem de um endereço de tamanho IPv4 devem sofrer investigações e parte dessa investigação deve incluir se as informações que você estava fornecendo (em IPv4) são apropriadas para IPv6.
-   A capacidade de especificar um endereço IP também deve depender se o IPv4 está em uso ou se o IPv6 está disponível. Se o IPv6 estiver disponível, é apropriado especificar endereços baseados em números (hexadecimais) ou endereços com base em nomes?

Tarefas de codificação

**Para revisar sua base de código existente de IPv4 para IPv4-interoperabilidade de IPv6**

1.  Execute uma revisão Visual da interface do usuário, procurando qualquer elemento que seja dependente de um comprimento específico para a cadeia de caracteres do endereço IP. Controles com a notação decimal com quatro seções facilmente identificada são fáceis de detectar, mas outros não. Pode haver lugares onde os endereços IP podem ser exibidos, como nas caixas de diálogo, em que um endereço IPv6 pode ficar sem espaço de exibição.
2.  Após encontrar qualquer um desses controles, mostre se é apropriado exibir o endereço ao usar o IPv6. Se for possível que o IPv4 ou o IPv6 esteja em uso, verifique se a interface do usuário pode acomodar um deles. Substitua ou amplie todos os controles com controles de interface do usuário que possam exibir um endereço IPv6 inteiro.
3.  Acompanhamento do teste da interface do usuário para garantir que as alterações que habilitam a exibição de endereço IPv6 mantenham a usabilidade pretendida ao usar endereços IPv4. Além disso, teste para locais de exibição de endereço de protocolo, como caixas de diálogo informativas, para garantir que eles manipulem adequadamente os endereços IPv6.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia IPv6 para aplicativos do Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Alterando estruturas de dados para aplicativos Winsock do IPv6](changing-data-structures-2.md)
</dt> <dt>

[Soquetes de pilha dupla para aplicativos Winsock do IPv6](dual-stack-sockets.md)
</dt> <dt>

[Chamadas de função para aplicativos Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Uso de endereços IPv4 codificados](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Protocolos subjacentes para aplicativos Winsock IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
