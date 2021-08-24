---
title: Práticas recomendadas ao usar BITS
description: Esta seção contém informações que você deve considerar ao criar um aplicativo que usa BITS.
ms.assetid: f4a09a80-2a85-4b59-b0fd-c23c128973f7
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: cbc11365cde74e092ae179c8b41562a16de9a6c36f0d85e51787a979c9332863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702086"
---
# <a name="best-practices-when-using-bits"></a>Práticas recomendadas ao usar BITS

Esta seção contém informações que você deve considerar ao criar um aplicativo que usa BITS.

## <a name="user-context-or-service-context"></a>Contexto do usuário ou contexto de serviço

O BITS transfere arquivos somente quando o proprietário do trabalho está conectado ao computador (o usuário deve ter feito logo on interativamente). O BITS não dá suporte **ao comando RunAs.** Para obter mais detalhes, consulte [Usuários e Conexões de Rede](users-and-network-connections.md).

Se você não precisar do contexto de um usuário para seu aplicativo, considere escrever um serviço em execução como LocalSystem, LocalService ou NetworkService. Essas contas do sistema estão sempre conectados, portanto, a transferência não está sujeita a um logo off do usuário. No entanto, se você representar um usuário ao criar o trabalho, as regras de logon interativo serão aplicadas. Para obter mais detalhes, consulte [Contas de serviço e BITS.](service-accounts-and-bits.md)

## <a name="jobs-are-persistent"></a>Os trabalhos são persistentes

Os trabalhos permanecem na fila até que você chame o [**método IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) [**ou IBackgroundCopyJob::Cancel.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) Os arquivos no trabalho não estarão disponíveis para o usuário até que você chame **Concluir**. Normalmente, você  chama Concluir quando o estado do trabalho é **BG \_ JOB STATE \_ \_ TRANSFERRED** e chama Cancelar quando o trabalho está no estado ERRO TRANSITÓRIO DE ESTADO DO TRABALHO  **BG \_ \_ \_ \_** ou ERRO DE ESTADO DO TRABALHO BG e não pode mais fazer progresso. **\_ \_ \_**

Se você não chamar o [](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) [**método Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou Cancelar dentro de 90 dias [(jobInactivityTimeout](group-policies.md) padrão Política de Grupo), o serviço cancelará o trabalho. Você sempre deve chamar o **método Complete** ou **Cancel** e não contar com a política JobInactivityTimeout para limpar seus trabalhos. Os trabalhos deixados na fila poderão impedir que os usuários criarem outros trabalhos se o limite de política MaxJobsPerUser ou MaxJobsPerMachine for atingido.

## <a name="when-to-use-foreground-or-background-priority"></a>Quando usar a prioridade em primeiro plano ou em segundo plano

A menos que o trabalho seja crítico ou o usuário esteja aguardando ativamente, você sempre deverá usar uma prioridade em segundo plano. No entanto, há ocasiões em que você pode querer alternar de prioridade em segundo plano para prioridade de primeiro plano, por exemplo, quando o proxy ou o servidor não dá suporte ao header Content-Range ou software antivírus no cliente remove a solicitação de título de intervalo. Alternar para prioridade de primeiro plano funciona apenas para os arquivos cujo tamanho de arquivo é menor que 2 GB. Para ver um exemplo, consulte a implementação do [**método IBackgroundCopyCallback::JobError.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) Observe também que, se o trabalho em primeiro plano for interrompido devido a uma desconexão de rede ou o logo off do usuário, o trabalho falhará porque o BITS enviará uma solicitação de intervalo para tentar reiniciar a transferência de onde ela foi interrompida.

A partir do Windows 8, você deve configurar trabalhos de download com CONTEÚDO DINÂMICO DA PROPRIEDADE DE TRABALHO BITS e PRIORIDADE DO TRABALHO **BG \_ \_ \_ FOREGROUND** ao direcionar servidores que não atendem aos Requisitos HTTP para [downloads de BITS.](http-requirements-for-bits-downloads.md) **\_ \_ \_ \_** Tenha em mente que isso fará com que o BITS tenha que reiniciar o download desde o início se ele for interrompido (por exemplo, devido a problemas de conectividade ou reinicialização do sistema).

Para obter informações sobre as prioridades disponíveis e como o BITS usa o nível de prioridade para agendar trabalhos, consulte [**BG \_ JOB \_ PRIORITY**](/windows/desktop/api/Bits/ne-bits-bg_job_priority).

## <a name="transient-and-fatal-errors"></a>Erros transitórios e fatais

Alguns erros podem ser recuperados e outros não. Por exemplo, o erro "O servidor não está disponível" é um erro recuperável e o erro "Acesso Negado" é um erro fatal. O BITS coloca erros recuperáveis em um estado de erro transitório e tenta o trabalho novamente após um intervalo especificado. Se o trabalho não conseguir fazer progresso, o BITS move o trabalho para um estado de erro fatal. Use os métodos [**IBackgroundCopyJob::SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) e [**IBackgroundCopyJob::SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para controlar como o BITS processa erros transitórios.

Para trabalhos em primeiro plano, você deve limitar a quantidade de tempo que deixa um trabalho permanecer no estado de erro transitório e tentar se recuperar. Use o [**método SetNoProgressTimeout**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnoprogresstimeout) para limitar a quantidade de tempo que um trabalho permanece no estado de erro transitório ou para forçar o trabalho no estado de erro fatal. Se você deixar o trabalho tentar se recuperar, deverá usar o método [**SetMinimumRetryDelay**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setminimumretrydelay) para definir o atraso mínimo de tentativa como 60 segundos ou chamar o método [**IBackgroundCopyJob::Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) para ativar o trabalho novamente.

Para obter mais informações, [**consulte BG \_ JOB \_ STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state), [Ciclo de vida de um](life-cycle-of-a-bits-job.md)trabalho bits e Tratamento [de erros](handling-errors.md).

## <a name="measuring-network-bandwidth-usage"></a>Medindo o uso de largura de banda de rede

O BITS pode usar o adaptador de rede do cliente para estimar a largura de banda de rede disponível. Como o BITS não é capaz de medir a largura de banda além do cliente, o BITS pode usar o link wan. Para reduzir o congestionamento no link wan, você pode usar a política de grupo **MaxInternetBandwidth** para limitar a quantidade de largura de banda que o cliente usa. Para obter mais informações, consulte [Largura de banda de rede](network-bandwidth.md) e políticas de [grupo.](group-policies.md)

Se você estiver escrevendo um aplicativo que muitos clientes usarão para baixar arquivos de um determinado servidor, considere um esquema que escalone as solicitações de download para não sobrecarregar o servidor com solicitações.

## <a name="setting-credentials-for-proxy-and-server-authentication"></a>Configurando credenciais para autenticação de proxy e servidor

Se você espera que o proxy ou o servidor exigir credenciais de usuário, forneça as credenciais para o BITS. Para especificar as credenciais, chame o [**método IBackgroundCopyJob2::SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) O BITS dá suporte a esquemas de autenticação Básico, Digest, Negotiate, NTLM e Passport.

Para obter detalhes sobre autenticação, consulte [Autenticação](authentication.md).

## <a name="specifying-proxy-settings-for-user-accounts-and-service-accounts"></a>Especificando configurações de proxy para contas de usuário e contas de serviço

Por padrão, o BITS usa as configurações de proxy Internet Explorer do usuário. Para substituir as configurações de proxy Internet Explorer do usuário, chame o [**método IBackgroundCopyJob::SetProxySettings.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings)

As configurações de proxy Internet Explorer não se aplicam a contas do sistema, portanto, o comportamento de proxy padrão **\_ \_ \_ \_ (PRECONFIG** DE USO DO PROXY DE TRABALHO BG) só funcionará corretamente em implantações do WPAD (Protocolo de Descoberta Automática de Proxy Web), a menos que etapas de configuração adicionais sejam realizadas. Se seu aplicativo for um serviço em execução como LocalSystem, LocalService ou NetworkService, considere configurar um token auxiliar em seus trabalhos bits ou definir explicitamente as configurações de proxy corretas chamando [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) com SUBSTITUIÇÃO DE USO DO PROXY DE TRABALHO **BG \_ \_ \_ \_**. Como alternativa, você pode usar as opções **/Util /SetIEProxy** do BitsAdmin.exe para definir Internet Explorer configurações de proxy para a conta do sistema LocalSystem, LocalService ou NetworkService. Para obter detalhes, consulte [BitsAdmin Tool](bitsadmin-tool.md).

O BITS não reconhece as configurações de proxy definidas usando o arquivo Proxycfg.exe dados.

Começando com o Atualização de outubro de 2018 para o Windows 10 (10.0; Build 17763), o BITS usa a mesma ordem de proxy que o WinHttp usa com AUTOMATIC_PROXY. O BITS usa essa ordenação mais compatível quando BG_JOB_PROXY_USAGE_PRECONFIG é especificado. BG_JOB_PROXY_USAGE_PRECONFIG é o valor padrão para especificar o proxy HTTP.

## <a name="specifying-user-specific-settings-for-authenticating-proxies"></a>Especificando configurações específicas do usuário para autenticar proxies

Se você estiver usando BITS em um ambiente que requer autenticação de proxy durante a execução como uma conta sem credenciais NTLM ou Kerberos usáveis no domínio de rede do computador, você deverá executar etapas extras para autenticar corretamente usando as credenciais de outra conta de usuário que tenha credenciais no domínio. Esse é um cenário típico quando o código BITS está em execução como um serviço do sistema, como LocalService, NetworkService ou LocalSystem, pois essas contas não têm credenciais NTLM ou Kerberos usáveis.

Para obter detalhes sobre como a autenticação funciona nesse cenário, consulte [Autenticação.](authentication.md)

## <a name="scalability"></a>Escalabilidade

Se mais de 100 trabalhos estão na fila, o desempenho pode começar a diminuir dependendo da composição do trabalho. O BITS usa a configuração de política [MaxJobsPerMachine](group-policies.md) para impor um limite rígido ao número de trabalhos na fila. Os aplicativos devem limitar o número de seus trabalhos a cerca de 10, para que vários aplicativos tenham menos chance de exceder a diretriz de 100 trabalhos. Normalmente, um aplicativo com um grande número de trabalhos a enviar primeiro enviaria 10 trabalhos e, em seguida, enviaria um de cada vez à medida que cada trabalho é final.

O número de arquivos no trabalho também deve ser limitado a um máximo de 10 arquivos. Se você quiser transferir um grande número de arquivos para um trabalho, considere criar um arquivo CAB que contenha todos os arquivos.

## <a name="http-headers-can-be-in-any-case"></a>Cabeçalhos HTTP podem ser em qualquer caso

Os padrões HTTP sempre dizem que os cabeçalhos HTTP devem ser tratados como sem maiúsculas de minúsculas (RFC 7230 seção 3.2). O padrão HTTP mais recente, RFC 7540, vai além e diz que o tráfego HTTP/2 deve comparar os cabeçalhos como sem maiúsculas de minúsculas e deve apresentar cabeçalhos em minúsculas (RFC 6540, seção 8.1.2). Mesmo quando o tráfego é enviado com os headers que não são de menor valor, os proxies podem optar por forçar os headers a reduzir.

## <a name="avoiding-personally-identifiable-information-pii"></a>Evitando pii (informações de identificação pessoal)

Os trabalhos bits, incluindo o nome de exibição do trabalho, a descrição e os nomes de arquivo, são visíveis para todos os usuários com privilégios de administrador. Eles também podem ser adicionados Windows Telemetria. Você deve evitar colocar dados confidenciais (como o próprio nome do usuário) nos detalhes do trabalho.
