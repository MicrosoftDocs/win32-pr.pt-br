---
description: O desenvolvimento de uma infraestrutura de rede de alto nível segura é uma prioridade para a maioria dos desenvolvedores de aplicativos de rede. No entanto, a segurança do soquete geralmente é ignorada, apesar de ser muito importante ao considerar uma solução totalmente segura.
ms.assetid: b37a3e33-65ee-43b1-bc8b-3280db7ebee4
title: Usando SO_REUSEADDR e SO_EXCLUSIVEADDRUSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa4024f031102cbd634c235bb39f4c7860e6c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662321"
---
# <a name="using-so_reuseaddr-and-so_exclusiveaddruse"></a>Usando o \_ REUSEADDR e, portanto, \_ EXCLUSIVEADDRUSE

O desenvolvimento de uma infraestrutura de rede de alto nível segura é uma prioridade para a maioria dos desenvolvedores de aplicativos de rede. No entanto, a segurança do soquete geralmente é ignorada, apesar de ser muito importante ao considerar uma solução totalmente segura. A segurança de soquete, especificamente, lida com processos que se associam à mesma porta associada anteriormente por outro processo de aplicativo. No passado, era possível que um aplicativo de rede "seqüestrasse" a porta de outro aplicativo, o que poderia facilmente causar um ataque de "negação de serviço" ou roubo de dados.

Em geral, a segurança do soquete se aplica a processos do lado do servidor. Mais especificamente, a segurança de soquete se aplica a qualquer aplicativo de rede que aceite conexões e receba o tráfego de datagrama IP. Esses aplicativos normalmente se associam a uma porta conhecida e são destinos comuns de código de rede mal-intencionado.

Os aplicativos cliente têm menos probabilidade de serem os destinos desses ataques — não porque eles são menos suscetíveis, mas porque a maioria dos clientes se associa a portas locais "efêmeras" em vez de portas "de serviço" estáticas. Os aplicativos de rede do cliente devem sempre ser associados a portas efêmeras (especificando a porta 0 na estrutura [**SOCKADDR**](sockaddr-2.md) apontada pelo parâmetro *Name* ao chamar a função [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) ), a menos que haja um motivo de arquitetura atraente para não. As portas locais efêmeras consistem em portas maiores que a porta 49151. A maioria dos aplicativos de servidor para serviços dedicados se associa a uma porta reservada conhecida que é menor ou igual à porta 49151. Portanto, para a maioria dos aplicativos, geralmente não há um conflito para solicitações de ligação entre aplicativos cliente e servidor.

Esta seção descreve o nível padrão de segurança em várias plataformas do Microsoft Windows e como as opções de soquete específicas são **\_ REUSEADDR** e [, portanto, \_ EXCLUSIVEADDRUSE](so-exclusiveaddruse.md) o impacto e afeta a segurança do aplicativo de rede. Um recurso adicional chamado segurança avançada de soquete está disponível no Windows Server 2003 e posterior. A disponibilidade dessas opções de soquete e a segurança avançada de soquete varia em todas as versões dos sistemas operacionais da Microsoft, conforme mostrado na tabela a seguir.

| Plataforma            | \_REUSEADDR | \_EXCLUSIVEADDRUSE                  | Segurança de soquete aprimorada |
|---------------------|---------------|---------------------------------------|--------------------------|
| Windows 95          | Disponível     | Não disponível                         | Não disponível            |
| Windows 98          | Disponível     | Não disponível                         | Não disponível            |
| Windows me          | Disponível     | Não disponível                         | Não disponível            |
| Windows NT 4.0      | Disponível     | Disponível no Service Pack 4 e posterior | Não disponível            |
| Windows 2000        | Disponível     | Disponível                             | Não disponível            |
| Windows XP          | Disponível     | Disponível                             | Não disponível            |
| Windows Server 2003 | Disponível     | Disponível                             | Disponível                |
| Windows Vista       | Disponível     | Disponível                             | Disponível                |
| Windows Server 2008 | Disponível     | Disponível                             | Disponível                |
| Windows 7and mais recente  | Disponível     | Disponível                             | Disponível                |

## <a name="using-so_reuseaddr"></a>Usando o \_ REUSEADDR

A opção de soquete **\_ REUSEADDR** permite que um soquete seja forçado a ligar a uma porta em uso por outro soquete. O segundo Soquete chama [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) com o parâmetro *OptName* definido como **\_ REUSEADDR** e o parâmetro *optval* definido como um valor booliano de **true** antes de chamar a [**Associação**](/windows/win32/api/winsock/nf-winsock-bind) na mesma porta que o soquete original. Depois que o segundo soquete for associado com êxito, o comportamento de todos os soquetes vinculados a essa porta será indeterminado. Por exemplo, se todos os soquetes na mesma porta fornecerem o serviço TCP, qualquer solicitação de conexão TCP de entrada na porta não poderá ser processada pelo soquete correto — o comportamento é não determinístico. Um programa mal-intencionado pode usar **, portanto, \_ REUSEADDR** para forçar o BIND Sockets em uso para serviços de protocolo de rede padrão a fim de negar acesso a esses serviços. Nenhum privilégio especial é necessário para usar essa opção.

Se um aplicativo cliente for associado a uma porta antes que um aplicativo de servidor seja capaz de se associar à mesma porta, poderão ocorrer problemas. Se o aplicativo de servidor for forçado a se associar usando a opção de soquete **\_ REUSEADDR** para a mesma porta, o comportamento de todos os soquetes vinculados a essa porta será indeterminado.

A exceção a esse comportamento não determinístico são os soquetes multicast. Se dois soquetes estiverem associados à mesma interface e porta e forem membros do mesmo grupo de multicast, os dados serão entregues a ambos os soquetes, em vez de um escolhido arbitrariamente.

## <a name="using-so_exclusiveaddruse"></a>Usando o \_ EXCLUSIVEADDRUSE

Antes que a opção de soquete **\_ EXCLUSIVEADDRUSE** fosse introduzida, havia muito pouco um desenvolvedor de aplicativos de rede a fim de impedir que um programa mal-intencionado se vinculasse à porta na qual o aplicativo de rede tinha seus próprios soquetes ligados. Para resolver esse problema de segurança, o Windows Sockets introduziu a opção de soquete **\_ EXCLUSIVEADDRUSE** , que se tornou disponível no Windows NT 4,0 com Service Pack 4 (SP4) e posterior.

A opção de soquete **\_ EXCLUSIVEADDRUSE** só pode ser usada por membros do grupo de segurança Administradores no Windows XP e versões anteriores. Os motivos pelos quais esse requisito foi alterado no Windows Server 2003 e versões posteriores são discutidos posteriormente neste artigo.

A **opção \_ EXCLUSIVEADDRUSE** é definida chamando a função [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) com o parâmetro *OptName* definido como **\_ EXCLUSIVEADDRUSE** e o parâmetro *optval* definido como um valor booliano de **true** antes de o soquete ser associado. Após a opção ser definida, o comportamento das chamadas de [**ligação**](/windows/win32/api/winsock/nf-winsock-bind) subsequentes difere dependendo do endereço de rede especificado em cada chamada de **ligação** .

A tabela a seguir descreve o comportamento que ocorre no Windows XP e versões anteriores quando um segundo soquete tenta se associar a um endereço associado anteriormente a um primeiro soquete usando opções de soquete específicas.

> [!NOTE]  
> Na tabela abaixo, "wildcard" denota o endereço curinga para o protocolo fornecido (como "0.0.0.0" para IPv4 e "::" para IPv6). "Específico" indica um endereço IP específico atribuído a uma interface. As células da tabela indicam se a ligação foi bem-sucedida ("success") ou se um erro é retornado ("INUSE" para o erro [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; "Acesso" para o erro [WSAEACCES](windows-sockets-error-codes-2.md) ).

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primeira chamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>ligação</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda chamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>ligação</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Padrão</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Padrão</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>INUSE</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Quando dois soquetes estão associados ao mesmo número de porta, mas em diferentes interfaces explícitas, não há conflito. Por exemplo, no caso em que um computador tem duas interfaces IP, 10.0.0.1 e 10.99.99.99, se a primeira chamada para [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) estiver em 10.0.0.1 com a porta definida como 5150 e, **portanto, \_ EXCLUSIVEADDRUSE** especificado, uma segunda chamada para **BIND** on 10.99.99.99 com a porta também será definida como 5150 e nenhuma opção especificada terá sucesso. No entanto, se o primeiro soquete estiver associado ao endereço curinga e à porta 5150, qualquer chamada de associação subsequente para a porta 5150 com o **\_ EXCLUSIVEADDRUSE** definido falhará com [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ou [WSAEACCES](windows-sockets-error-codes-2.md) retornados pela operação de **Associação** .

No caso em que a primeira chamada para [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) define **\_ REUSEADDR** ou nenhuma opção de soquete, a segunda chamada de **ligação** irá "seqüestrar" a porta e o aplicativo não poderá determinar qual dos dois soquetes receberá pacotes específicos enviados para a porta "compartilhada".

Um aplicativo típico que chama a função de [**Associação**](/windows/win32/api/winsock/nf-winsock-bind) não aloca o soquete associado para uso exclusivo, a menos que a opção de soquete **\_ EXCLUSIVEADDRUSE** seja chamada no soquete antes da chamada para a função de **ligação** . Se um aplicativo cliente se associar a uma porta efêmera ou a uma porta específica antes que um aplicativo de servidor seja associado à mesma porta, poderão ocorrer problemas. O aplicativo de servidor pode forçar a ligação com a mesma porta usando a opção de soquete **\_ REUSEADDR** no soquete antes de chamar a função **BIND** , mas o comportamento de todos os soquetes ligados a essa porta é, então, indeterminado. Se o aplicativo de servidor tentar usar a opção de soquete **\_ EXCLUSIVEADDRUSE** para uso exclusivo da porta, a solicitação falhará.

Por outro lado, um soquete com o **\_ EXCLUSIVEADDRUSE** definido não pode necessariamente ser reutilizado imediatamente após o fechamento do soquete. Por exemplo, se um soquete de escuta com o **\_ EXCLUSIVEADDRUSE** Set aceitar uma conexão e, em seguida, for fechado posteriormente, outro soquete (também com **\_ EXCLUSIVEADDRUSE**) não poderá se associar à mesma porta que o primeiro soquete até que a conexão original se torne inativa.

Esse problema pode se tornar complicado porque o protocolo de transporte subjacente pode não encerrar a conexão, embora o soquete tenha sido fechado. Mesmo após o soquete ser fechado pelo aplicativo, o sistema deve transmitir todos os dados armazenados em buffer, enviar uma mensagem de desconexão normal para o par e aguardar uma mensagem de desconexão normal correspondente do par. É possível que o protocolo de transporte subjacente nunca libere a conexão; por exemplo, o par que participa da conexão original pode anunciar uma janela de tamanho zero ou alguma outra forma de configuração de "ataque". Nesse caso, a conexão do cliente permanece em um estado ativo, apesar da solicitação para fechá-la, já que os dados não confirmados permanecem no buffer.

Para evitar essa situação, os aplicativos de rede devem garantir um desligamento normal chamando [**Shutdown**](/windows/win32/api/winsock/nf-winsock-shutdown) com o sinalizador de envio de SD \_ definido e aguardando em um loop de [**recepção**](/windows/win32/api/winsock/nf-winsock-recv) até que zero bytes sejam retornados pela conexão. Isso garante que todos os dados sejam recebidos pelo par e, da mesma forma, confirmam com o par de que ele recebeu todos os dados transmitidos, além de evitar o problema de reutilização de porta mencionado anteriormente.

A \_ opção de soquete remanescente pode ser definida em um soquete para impedir que a porta esteja em transição para um estado de espera "ativa"; no entanto, isso não é recomendado, pois pode levar a efeitos desejados, como conexões de redefinição. Por exemplo, se os dados forem recebidos pelo par, mas permanecerem não confirmados por ele e o computador local fechar o soquete com a \_ configuração remanescente, a conexão entre os dois computadores será redefinida e os dados não confirmados serão descartados pelo par. É difícil escolher um horário adequado para o remanescente, pois um valor de tempo limite menor geralmente resulta em conexões repentinamente anuladas, enquanto valores de tempo limite maiores deixam o sistema vulnerável a ataques de negação de serviço (estabelecendo muitas conexões e potencialmente bloqueando/bloquear threads de aplicativo). Fechar um soquete que tem um valor de tempo limite remanescente diferente também pode fazer com que a chamada [**fechamento**](/windows/win32/api/winsock/nf-winsock-closesocket) seja bloqueada.

## <a name="enhanced-socket-security"></a>Segurança de soquete aprimorada

A segurança avançada de soquete foi adicionada com o lançamento do Windows Server 2003. Em versões anteriores do sistema operacional Microsoft Server, a segurança de soquete padrão permitia facilmente processos para seqüestrar portas de aplicativos desconhecidos. No Windows Server 2003, os soquetes não estão em um estado compartilhável por padrão. Portanto, se um aplicativo quiser permitir que outros processos reutilizem uma porta na qual um soquete já esteja associado, ele deverá habilitá-lo especificamente. Se esse for o caso, o primeiro soquete para chamar a [**ligação**](/windows/win32/api/winsock/nf-winsock-bind) na porta deve ter **\_ REUSEADDR** definido no soquete. A única exceção a esse caso ocorre quando a segunda chamada de **ligação** é executada pela mesma conta de usuário que fez com que a chamada original fosse **associada**. Essa exceção existe apenas para fornecer compatibilidade com versões anteriores.

A tabela a seguir descreve o comportamento que ocorre no Windows Server 2003 e sistemas operacionais posteriores quando um segundo soquete tenta se associar a um endereço associado anteriormente a um primeiro soquete usando opções de soquete específicas.

> [!NOTE]
> Na tabela abaixo, "wildcard" denota o endereço curinga para o protocolo fornecido (como "0.0.0.0" para IPv4 e "::" para IPv6). "Específico" indica um endereço IP específico atribuído a uma interface. As células da tabela indicam se a ligação foi bem-sucedida ("success") ou o erro retornado ("INUSE" para o erro [WSAEADDRINUSE](windows-sockets-error-codes-2.md) ; "Acesso" para o erro [WSAEACCES](windows-sockets-error-codes-2.md) ).
>
> Observe também que nessa tabela específica, ambas as chamadas de [**Associação**](/windows/win32/api/winsock/nf-winsock-bind) são feitas sob a mesma conta de usuário.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primeira chamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>ligação</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda chamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>ligação</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Padrão</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Padrão</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>Sucesso</td>
        <td>ACCESS</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Sucesso</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Sucesso</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>Sucesso</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Sucesso</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Algumas entradas na tabela acima da explicação de mérito.

Por exemplo, se o primeiro chamador definir **, portanto, \_ EXCLUSIVEADDRUSE** em um endereço específico, e o segundo chamador tentar chamar [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) com um endereço curinga na mesma porta, a segunda chamada de **ligação** terá sucesso. Nesse caso em particular, o segundo chamador é associado a todas as interfaces, exceto o endereço específico ao qual o primeiro chamador está associado. Observe que o inverso desse caso não é verdadeiro: se o primeiro conjunto de chamadas for **\_ EXCLUSIVEADDRUSE** e chamar **BIND** com o sinalizador curinga, o segundo chamador não poderá chamar **BIND** com a mesma porta.

O comportamento de associação de soquete é alterado quando as chamadas de ligação de soquete são feitas em contas de usuário diferentes. A tabela a seguir especifica o comportamento que ocorre no Windows Server 2003 e sistemas operacionais posteriores quando um segundo soquete tenta se associar a um endereço associado anteriormente a um primeiro soquete usando opções de soquete específicas e uma conta de usuário diferente.

<table>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2" rowspan="3">Primeira chamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>ligação</strong></a></td>
        <td bgcolor="#C0C0C0" colspan="6">Segunda chamada de <a href="/windows/win32/api/winsock/nf-winsock-bind"><strong>ligação</strong></a></td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" colspan="2">Padrão</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0" colspan="2">SO_EXCLUSIVEADDRUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td bgcolor="#C0C0C0">Específicas</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">Padrão</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Sucesso</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_REUSEADDR</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Êxito</td>
        <td>Êxito</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0" rowspan="2">SO_EXCLUSIVEADDRUSE</td>
        <td bgcolor="#C0C0C0">Curinga</td>
        <td>INUSE</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>ACCESS</td>
    </tr>
    <tr>
        <td bgcolor="#C0C0C0">Específicas</td>
        <td>Sucesso</td>
        <td>INUSE</td>
        <td>Sucesso</td>
        <td>ACCESS</td>
        <td>INUSE</td>
        <td>INUSE</td>
    </tr>
</table>

Observe que o comportamento padrão é diferente quando as chamadas de [**ligação**](/windows/win32/api/winsock/nf-winsock-bind) são feitas em contas de usuário diferentes. Se o primeiro chamador não definir nenhuma opção no soquete e associar-se ao endereço curinga, o segundo chamador não poderá definir a opção for **\_ REUSEADDR** e se associar com êxito à mesma porta. O comportamento padrão sem opções definidas também retorna um erro.

No Windows Vista e posterior, um soquete de pilha dual pode ser criado, que opera em IPv6 e IPv4. Quando um soquete de pilha dupla está associado ao endereço curinga, a porta fornecida é reservada nas pilhas de rede IPv4 e IPv6 e as verificações associadas a **\_ REUSEADDR** e **\_ EXCLUSIVEADDRUSE** (se definido) são feitas. Essas verificações devem ter sucesso em ambas as pilhas de rede. Por exemplo, se um soquete TCP de pilha dupla contiver **\_ EXCLUSIVEADDRUSE** e tentar se associar à porta 5000, nenhum outro soquete TCP poderá ser associado anteriormente à porta 5000 (curinga ou específico). Nesse caso, se um soquete TCP IPv4 tiver sido associado anteriormente ao endereço de loopback na porta 5000, a chamada de [**ligação**](/windows/win32/api/winsock/nf-winsock-bind) para o soquete de pilha dupla falharia com [WSAEACCES](windows-sockets-error-codes-2.md).

## <a name="application-strategies"></a>Estratégias de aplicativo

Ao desenvolver um aplicativo de rede que opere na camada de soquete, é importante considerar o tipo de segurança de soquete necessário. Aplicativos cliente — aplicativos que conectam ou enviam dados a um serviço — raramente exigem etapas adicionais, pois eles se associam a uma porta local aleatória (efêmera). Se o cliente exigir uma associação de porta local específica para funcionar corretamente, você deve considerar a segurança do soquete.

A **opção \_ REUSEADDR** tem muito poucos usos em aplicativos normais além dos soquetes multicast, nos quais os dados são entregues a todos os soquetes ligados na mesma porta. Caso contrário, qualquer aplicativo que define essa opção de soquete deve ser reprojetado para remover a dependência, pois ela está eminentemente vulnerável a "seqüestro de soquete". Desde que a opção de soquete **\_ REUSEADDR** possa ser usada para seqüestrar potencialmente uma porta em um aplicativo de servidor, o aplicativo deve ser considerado como não seguro.

Todos os aplicativos de servidor devem definir **\_ EXCLUSIVEADDRUSE** para um nível forte de segurança de soquete. Isso não apenas impede que software mal-intencionado Capture a porta, mas também indica se outro aplicativo está associado ou não à porta solicitada. Por exemplo, uma chamada para [**ligar**](/windows/win32/api/winsock/nf-winsock-bind) o endereço curinga por um processo com o **\_ EXCLUSIVEADDRUSE** Socket Option Set falhará se outro processo estiver atualmente associado à mesma porta em uma interface específica.

Por fim, embora a segurança de soquete tenha sido aprimorada no Windows Server 2003, um aplicativo sempre deve definir a opção de soquete **\_ EXCLUSIVEADDRUSE** para garantir que ele seja associado a todas as interfaces específicas que o processo solicitou. A segurança de soquete no Windows Server 2003 adiciona um nível maior de segurança para aplicativos herdados, mas os desenvolvedores de aplicativos ainda precisam projetar seus produtos com todos os aspectos da segurança em mente.
