---
title: Práticas recomendadas ao usar o BITS
description: Esta seção contém informações que você deve considerar ao criar um aplicativo que usa BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: bbf69e75b99994eea3e8986d1be9920ff1a12bc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916041"
---
# <a name="best-practices-when-using-bits"></a>Práticas recomendadas ao usar o BITS

Esta seção contém informações que você deve considerar ao criar um aplicativo que usa BITS.

## <a name="user-context-or-service-context"></a>Contexto do usuário ou contexto de serviço

O BITS transfere arquivos somente quando o proprietário do trabalho é conectado ao computador (o usuário deve ter feito logon interativamente). O BITS não oferece suporte ao comando **runas** . Para obter mais detalhes, consulte [usuários e conexões de rede](users-and-network-connections.md).

Se você não precisar do contexto de um usuário para seu aplicativo, considere escrever um serviço em execução como LocalSystem, LocalService ou NetworkService em vez disso. Essas contas de sistema estão sempre conectadas, portanto, a transferência não está sujeita a um logoff de usuário. No entanto, se você representar um usuário ao criar o trabalho, as regras de logon interativo se aplicarão. Para obter mais detalhes, consulte [contas de serviço e bits](service-accounts-and-bits.md).

## <a name="jobs-are-persistent"></a>Os trabalhos são persistentes

Os trabalhos permanecem na fila até que você chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou [**método ibackgroundcopyjob:: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . Os arquivos no trabalho não estarão disponíveis para o usuário até que você chame **Complete**. Normalmente, você chama **Complete** quando o estado do trabalho é **BG \_ Job \_ estado \_ transferido**, e você chama **Cancel** quando o trabalho está no estado de erro **BG do \_ estado do trabalho \_ \_ \_** ou BG erro de **\_ \_ estado \_ de trabalho** de demarcador e não pode mais progredir.

Se você não chamar o método [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou o método [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dentro de 90 dias ( [JobInactivityTimeout](group-policies.md) padrão política de grupo), o serviço cancelará o trabalho. Você sempre deve chamar o método **Complete** ou **Cancel** e não confiar na política JobInactivityTimeout para limpar seus trabalhos. Os trabalhos restantes na fila podem impedir que os usuários criem outros trabalhos se o limite da política MaxJobsPerUser ou MaxJobsPerMachine for atingido.

## <a name="when-to-use-foreground-or-background-priority"></a>Quando usar a prioridade de primeiro plano ou plano de fundo

A menos que o trabalho seja de tempo crítico ou que o usuário esteja aguardando ativamente, você sempre deve usar uma prioridade de plano de fundo. No entanto, há ocasiões em que você talvez queira alternar da prioridade do plano de fundo para a prioridade de primeiro plano, por exemplo, quando o proxy ou o servidor não dá suporte ao cabeçalho do intervalo de conteúdo ou o software antivírus no cliente remove a solicitação de cabeçalho do intervalo. Alternar para a prioridade de primeiro plano funciona apenas para os arquivos cujo tamanho de arquivo é menor que 2 GB. Para obter um exemplo, consulte a implementação para o método [**IBackgroundCopyCallback:: JobError**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) . Observe também que, se o trabalho em primeiro plano for interrompido devido a uma desconexão de rede ou quando o usuário fizer logoff, o trabalho falhará porque o BITS enviará uma solicitação de intervalo para tentar reiniciar a transferência de onde parou.

A partir do Windows 8, você deve configurar trabalhos de download com **\_ \_ \_ \_ conteúdo dinâmico de propriedade de trabalho bits** e BG de **\_ \_ prioridade \_ de trabalho** para destinar servidores que não atendem aos [requisitos de http para downloads de bits](http-requirements-for-bits-downloads.md). Tenha em mente que isso resultará em BITS que precisem reiniciar o download desde o início, se ele for interrompido (por exemplo, devido a problemas de conectividade ou reinicialização do sistema).

Para obter informações sobre as prioridades disponíveis e como o BITS usa o nível de prioridade para agendar trabalhos, consulte [**BG \_ \_ prioridade de trabalho**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Erros transitórios e fatais

Alguns erros são recuperáveis e outros não. Por exemplo, o erro "o servidor está indisponível" é um erro recuperável e o erro "acesso negado" é um erro fatal. O BITS coloca erros recuperáveis em um estado de erro transitório e tenta o trabalho novamente após um intervalo especificado. Se o trabalho não puder fazer o progresso, o BITS moverá o trabalho para um estado de erro fatal. Use os métodos [**método ibackgroundcopyjob:: SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) e [**método ibackgroundcopyjob:: SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para controlar como o bits processa erros transitórios.

Para trabalhos em primeiro plano, você deve limitar a quantidade de tempo que permite que um trabalho permaneça no estado de erro transitório e tentar recuperá-lo. Use o método [**SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para limitar a quantidade de tempo que um trabalho permanece no estado de erro transitório ou para forçar o trabalho para o estado de erro fatal. Se você deixar o trabalho tentar recuperar, deverá usar o método [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) para definir o atraso mínimo de repetição como 60 segundos ou chamar o método [**método ibackgroundcopyjob:: resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para ativar o trabalho novamente.

Para obter mais informações, [**consulte \_ BG \_ estado do trabalho**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [ciclo de vida de um trabalho do bits](life-cycle-of-a-bits-job.md)e [tratamento de erros](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Medição do uso da largura de banda da rede

O BITS pode usar o adaptador de rede do cliente para estimar a largura de banda de rede disponível. Como o BITS não é capaz de medir a largura de banda além do cliente, os BITS podem congestionar o link WAN. Para reduzir o congestionamento no link WAN, você pode usar a política de grupo **MaxInternetBandwidth** para limitar a quantidade de largura de banda que o cliente usa. Para obter mais informações, consulte [largura de banda de rede](network-bandwidth.md) e diretivas de [grupo](group-policies.md).

Se você estiver escrevendo um aplicativo que muitos clientes usarão para baixar arquivos de um determinado servidor, considere um esquema que Escalona as solicitações de download para que você não sobrecarregue o servidor com solicitações.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Configurando credenciais para autenticação de proxy e servidor

Se você espera que o proxy ou o servidor exija credenciais de usuário, você deve fornecer as credenciais para BITS. Para especificar as credenciais, chame o método [**IBackgroundCopyJob2:: SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . O BITS dá suporte a esquemas de autenticação básica, Digest, Negotiate, NTLM e Passport.

Para obter detalhes sobre a autenticação, consulte [autenticação](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Especificando configurações de proxy para contas de usuário e contas de serviço

Por padrão, o BITS usa as configurações de proxy do Internet Explorer do usuário. Para substituir as configurações de proxy do Internet Explorer do usuário, chame o método [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) .

As configurações de proxy do Internet Explorer não se aplicam a contas do sistema, portanto o comportamento de proxy padrão (configuração de **\_ uso de proxy de trabalho \_ \_ \_ BG**) só funcionará corretamente em implantações de WPAD (protocolo de descoberta automática de proxy da Web), a menos que sejam executadas etapas de configuração adicionais. Se o seu aplicativo for um serviço em execução como LocalSystem, LocalService ou NetworkService, considere configurar um token auxiliar em seus trabalhos do BITS ou definir explicitamente as configurações de proxy corretas chamando [**método ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com a **substituição de uso de \_ proxy de trabalho \_ \_ \_ BG**. Como alternativa, você pode usar os comutadores **/util/SetIEProxy** da BitsAdmin.exe para definir as configurações de proxy do Internet Explorer para a conta do sistema LocalSystem, LocalService ou NetworkService. Para obter detalhes, consulte [ferramenta BitsAdmin](bitsadmin-tool.md).

O BITS não reconhece as configurações de proxy que são definidas usando o arquivo Proxycfg.exe.

A partir da atualização do Windows 10 de outubro de 2018 (10,0; Build 17763), o BITS usa a mesma ordem de proxy que o WinHttp usa com AUTOMATIC_PROXY. O BITS usa essa ordenação mais compatível quando BG_JOB_PROXY_USAGE_PRECONFIG é especificado. BG_JOB_PROXY_USAGE_PRECONFIG é o valor padrão para especificar o proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Especificando configurações específicas do usuário para autenticar proxies

Se você estiver usando BITS em um ambiente que exija autenticação de proxy durante a execução como uma conta sem credenciais NTLM ou Kerberos utilizáveis no domínio de rede da máquina, será necessário executar etapas adicionais para autenticar corretamente usando as credenciais de outra conta de usuário que tenha credenciais no domínio. Esse é um cenário típico quando o código BITS está sendo executado como um serviço de sistema, como LocalService, NetworkService ou LocalSystem, pois essas contas não têm credenciais NTLM ou Kerberos utilizáveis.

Para obter detalhes sobre como funciona a autenticação nesse cenário, consulte [autenticação.](authentication.md)

## <a name="scalability"></a>Escalabilidade

Se mais de 100 trabalhos estiverem na fila, o desempenho pode começar a diminuir dependendo da composição do trabalho. O BITS usa a configuração de política [MaxJobsPerMachine](group-policies.md) para impor um limite rígido no número de trabalhos na fila. Os aplicativos devem limitar o número de seus trabalhos a cerca de 10, de modo que vários aplicativos terão menos chance de exceder a diretriz de 100 trabalhos. Normalmente, um aplicativo com um grande número de trabalhos a serem enviados primeiro enviaria 10 trabalhos e, em seguida, enviaria um de cada vez enquanto cada trabalho for concluído.

O número de arquivos no trabalho também deve ser limitado a um máximo de 10 arquivos. Se você quiser transferir um grande número de arquivos para um trabalho, considere a criação de um arquivo CAB que contenha todos os arquivos.

## <a name="http-headers-can-be-in-any-case"></a>Os cabeçalhos HTTP podem estar em qualquer caso

Os padrões HTTP sempre disseram que os cabeçalhos HTTP devem ser tratados como não diferencia maiúsculas de minúsculas (RFC 7230 seção 3,2). O padrão HTTP mais recente, RFC 7540, vai além e informa que o tráfego HTTP/2 deve comparar os cabeçalhos como não diferenciar maiúsculas de minúsculas e deve apresentar cabeçalhos em letras minúsculas (RFC 6540, seção 8.1.2). Mesmo quando o tráfego é enviado com cabeçalhos não minúsculos, os proxies podem optar por forçar os cabeçalhos para letras minúsculas.

## <a name="avoiding-personally-identifiable-information-pii"></a>Evitando informações de identificação pessoal (PII)

Os trabalhos do BITS, incluindo o nome de exibição do trabalho e os nomes de arquivo e descrição, são visíveis para todos os usuários com privilégios de administrador. Eles também podem ser adicionados à telemetria do Windows. Você deve evitar colocar dados confidenciais (como o próprio nome do usuário) nos detalhes do trabalho.
