---
title: Virtualização de recursos
description: Virtualização de recursos
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92176ab1431baad424bd4e097f20627f213f6dcba754b9d6f35dce15e9af12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954380"
---
# <a name="resource-virtualization"></a>Virtualização de recursos

A função principal do TBS é compartilhar com eficiência determinados recursos limitados do TPM: chaves, autorização e sessões de transporte.

Quando uma instância de um desses recursos é criada, o TBS cria uma instância virtual do recurso e retorna um handle para essa instância virtual no fluxo de comandos de resultado (em vez da instância de alça real retornada pelo TPM). O TBS mantém um mapeamento entre o alça virtual e o handle real internamente. Se o TPM ficar sem espaço para conter mais recursos de um determinado tipo, as instâncias existentes do recurso serão salvas e despejadas seletivamente até que o TPM possa conter o novo recurso. Quando os recursos antigos são necessários novamente, o TBS carrega os contextos salvos (salvando e despejando outros recursos, se necessário) antes de enviar o comando.

Toda a virtualização no TBS é executada em nome de um contexto específico. Cada contexto só tem permissão para acessar recursos virtuais criados especificamente em seu nome, bem como os recursos físicos no TPM que correspondem a esses recursos virtuais. Por padrão, o número total de todos os recursos virtualizados é limitado a 500. Esse número pode ser alterado criando ou modificando um valor de Registro **DWORD** chamado **MaxResources** em **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Tpm**. O uso de recursos TBS em tempo real pode ser observado usando a Monitor de Desempenho para acompanhar o número de recursos de TBS. Essa restrição se tornou obsoleta com Windows 8 e Windows Server 2012.

Recursos limitados do TPM que não são virtualizados pelo TBS (como contadores e armazenamento NV) devem ser compartilhados de modo cooperativo entre pilhas de software.

> [!Note]  
> Esse lidar com a virtualização faz com que os comandos que incluem os alças de chave no cálculo de parâmetros de autorização HMAC falhem. Como resultado, muitos comandos preterido na versão 1.2 do TPM não podem ser usados pelo software de aplicativo no ambiente TBS.

 

## <a name="resource-limits"></a>Limites de recursos

O TPM permite que os chamadores consultem seus recursos para determinar quanto espaço está disponível para determinados tipos de recursos. Alguns desses limites de recursos, como a quantidade de espaço disponível para chaves, sessões de autorização e sessões de transporte, são efetivamente estendidos pelo TBS por meio da virtualização. As limitações de TBS, que são controladas pela configuração do Registro **MaxResources,** geralmente são muito maiores do que as limitações reais do hardware do TPM subjacente. Nenhum mecanismo é fornecido para consultar limitações de TBS separadamente dos limites de hardware do TPM. Essa limitação de TBS tornou-se obsoleta com Windows 8 e Windows Server 2012.

## <a name="keys"></a>Chaves

O TBS virtualiza os alças de chave para que as chaves possam ser descarregadas de forma transparente do TPM quando não estão sendo usadas e carregadas de volta no TPM quando elas são necessárias. Quando uma chave é criada, o TBS associa um alça virtual à chave carregada. O mesmo alça virtual é usado durante o tempo de vida do recurso. Os alças de chave virtual só são válidos no contexto que os criou e os recursos associados não são preservados além da vida útil do contexto.

-   Criando chaves com LoadKey2 do TPM \_

    Se uma chave for criada usando o comando TPM \_ LoadKey2, TPM2 \_ CreatePrimary, TPM2 Load ou \_ TPM2 LoadExternal, o TBS substituirá o alça no fluxo de byte de retorno por um alça de chave virtual de \_ sua escolha. Como resultado, o TBS garante que cada alça virtual seja exclusiva. Se o TBS detectar uma colisão (um evento extremamente improvável), o TBS descarregará a chave do TPM e informará o software de chamada. Em seguida, o software pode reabrir a operação. Esse processo pode ser repetido até que o TBS obtém um alça de chave exclusivo.

-   Limpando chaves

    O TBS invalida o alça de chave virtual quando recebe uma mensagem \_ TPM FlushSpecific ou TPM2 FlushContext para esse alça virtual do contexto \_ do cliente. Se a chave estiver fisicamente presente no TPM quando a mensagem de liberação for recebida, o TBS liberará a chave do TPM nesse momento.

-   Removendo chaves temporariamente

    Ao despejar uma chave do TPM para dar espaço a um novo item, o TBS executa um comando TPM \_ SaveContext ou TPM2 ContextSave na chave antes de re \_ despejo.

-   Restaurando chaves

    Quando um comando que faz referência a uma chave carregada é enviado para o TBS, ele garante que a chave está fisicamente presente no TPM. Se a chave não estiver presente, o TBS a restaurará com uma chamada para TPM \_ LoadContext ou \_ TPM2 ContextLoad. Se uma chave não puder ser restaurada para o TPM, o TBS retornará TPM \_ E \_ INVALID \_ KEYHANDLE como o resultado do TPM.

O TBS substitui cada alça virtual associada a uma chave em um fluxo de comandos pelo alça físico da chave carregada no TPM. Se um comando for enviado com um alça virtual que não seja reconhecido pelo TBS no contexto do chamador, o TBS formatará um fluxo de erros para o chamador com TPM \_ E \_ INVALID \_ KEYHANDLE.

## <a name="authorization-sessions"></a>Sessões de autorização

As sessões de autorização são criadas chamando TPM \_ OIAP, TPM \_ OSAP ou TPM \_ DSAP. Em cada caso, o fluxo de byte de retorno contém o alça TPM físico da sessão de autorização recém-criada. O TBS substitui isso por um alça virtual. Quando a sessão de autorização é referenciada posteriormente, o TBS substitui o alça virtual no fluxo de comandos pelo alça física da sessão de autorização. O TBS garante que o tempo de vida da sessão de autorização virtual corresponde ao da sessão de autorização física. Se um cliente tentar usar um alça virtual expirado, o TBS formatará um fluxo de erros com o erro TPM \_ INVALIDAUTHHANDLE.

Os slots de sessão são limitados e os TBS podem ficar sem slots externos nos quais salvar contextos de sessão de autorização. Se isso acontecer, o TBS escolherá uma sessão de autorização para invalidar para que o novo contexto possa ser salvo com êxito. Um aplicativo que tenta usar o contexto antigo precisará criar a sessão de autorização.

O TBS invalida a sessão de autorização virtual quando ocorre um dos seguintes casos:

-   O sinalizador continue-use associado à sessão de autorização no fluxo de comando retornado do TPM é **FALSE.**
-   Falha em um comando que usa uma sessão de autorização.
-   Um comando é executado que invalida a sessão de autorização associada ao comando (como TPM \_ CreateWrapKey).
-   Uma chave associada a uma sessão OSAP ou DSAP é ressalvada do TPM com uma chamada para TPM \_ FlushSpecific ou TPM2 FlushContext (sem considerar se esse comando foi originado com o TBS ou com software de nível \_ superior).

    O TBS ressincronizará automaticamente as sessões de autorização após a execução bem-sucedida de determinados comandos não determinísticos para garantir que o estado TBS permaneça consistente com o estado do TPM. Os comandos afetados são:

    -   TPM \_ ORD \_ Delegate \_ Manage
    -   TPM \_ ORD \_ Delegate \_ CreateOwnerDelegation
    -   \_LoadOwnerDelegation delegado ORD \_ do TPM \_

Em cada um dos seguintes casos, a sessão de autorização no TPM é liberado automaticamente pelo TPM:

-   Criando sessões de autorização

    Os alças de sessão de autorização virtual só são válidos no contexto que os criou e os recursos associados não são preservados além da vida útil do contexto associado.

-   Limpando sessões de autorização

    O TBS invalida a sessão de autorização virtual se receber um comando \_ TPM FlushSpecific ou TPM2 FlushContext para o handle virtual do contexto \_ do cliente. Se a sessão de autorização estiver fisicamente presente no TPM quando o comando de liberação for recebido, o TBS liberará a sessão física do TPM imediatamente.

-   Removendo temporariamente sessões de autorização

    Ao despejar uma sessão de autorização do TPM para dar espaço a uma nova entidade, o TBS executa tPM \_ SaveContext ou TPM2 \_ ContextSave nessa sessão de autorização.

-   Restaurando sessões de autorização

    Quando um comando TPM autorizado é enviado para o TBS, o TBS garante que todas as sessões de autorização virtuais referenciadas no comando estão fisicamente presentes no TPM. Se alguma das sessões de autorização não estiver presente, o TBS as restaurará com uma chamada para TPM \_ LoadContext ou \_ TPM2 ContextLoad. Se uma sessão de autorização não puder ser restaurada para o TPM, o TBS retornará TPM \_ E INVALID HANDLE como o resultado do \_ \_ TPM.

O TBS substitui cada alça virtual associada a uma sessão de autorização em um fluxo de comando pelo alça físico da sessão de autorização carregada no TPM.

Se um comando for enviado com um alça virtual que não seja reconhecido pelo TBS no contexto do chamador, o TBS formatará um fluxo de erro para o chamador com o erro TPM \_ E \_ INVALID \_ HANDLE.

## <a name="transport-sessions"></a>Sessões de transporte

> [!Note]  
> A manipulação de sessões de transporte, conforme descrito aqui, é específica Windows Vista e Windows Server 2008.

 

As sessões de transporte são um mecanismo fornecido pelo TPM que permite que uma pilha de software criptografe dados em um comando à medida que passa entre o software e o TPM. Isso impede que um adversário intercepte os dados à medida que passa pelo barramento de hardware.

> [!IMPORTANT]
> Somente os dados de carga são criptografados. Os comandos que estão sendo executados ainda podem ser identificados.

 

Infelizmente, esse mecanismo também impede que o TBS examine dados de carga. Na maioria dos casos, isso não é um problema porque o TBS modifica apenas os alças, não os dados de carga. No entanto, no caso do TPM \_ LoadContext, por exemplo, o alçamento de recurso retornado é coberto pela criptografia. Portanto, o TBS impede tentativas de executar uma operação LoadContext do TPM \_ coberta por uma sessão de transporte.

O TBS bloqueia os seguintes comandos na sessão de transporte:

-   TPM \_ EstablishTransport
-   TPM \_ ExecuteTransport
-   TPM \_ Terminate \_ Handle
-   LoadKey do TPM \_
-   TPM \_ EvictKey
-   SaveKeyContext do TPM \_
-   LoadKeyContext do TPM \_
-   TPM \_ SaveAuthContext
-   TPM \_ LoadAuthContext
-   TPM \_ SaveContext
-   TPM \_ LoadContext
-   TPM \_ FlushSpecific

Quando qualquer um desses comandos é coberto por uma sessão de transporte, o TBS retorna TPM \_ E \_ EMBEDDED COMMAND \_ \_ UNSUPPORTED como o resultado do TPM.

Os alças de sessão de transporte são virtualizados de maneira semelhante a alças de chave e alças de autorização. Há um número limitado de slots de contexto de sessão de transporte salvos disponíveis no TPM.

O TBS invalida a sessão de transporte virtual se qualquer um dos seguintes casos ocorrer:

-   O sinalizador continue-use associado à sessão de transporte no fluxo de comando de retorno do TPM é **FALSE.**

    Assim como acontece com as sessões de autorização acima, o TBS ressincronizará automaticamente as sessões de transporte após a execução bem-sucedida de determinados comandos não determinísticos para garantir que o estado TBS permaneça consistente com o estado do TPM. Os comandos afetados são:

    -   TPM \_ ORD \_ Delegate \_ Manage
    -   TPM \_ ORD \_ Delegate \_ CreateOwnerDelegation
    -   \_LoadOwnerDelegation delegado ORD \_ do TPM \_

Em cada um desses casos, a sessão de transporte no TPM será liberado automaticamente pelo TPM:

-   Criando sessões de transporte

    O TBS cria um alça virtual para cada sessão de transporte criada por um cliente. Os alças de transporte virtual só são válidos no contexto que os criou e os recursos associados não são preservados além da vida útil do contexto associado.

-   Limpando sessões de transporte

    O TBS invalida a sessão de transporte virtual se receber um comando FlushSpecific do TPM para o alça \_ virtual do contexto do cliente. Se a sessão de transporte estiver fisicamente presente no TPM quando o comando de liberação for recebido, o TBS liberará a sessão física do TPM imediatamente.

-   Removendo temporariamente as sessões de transporte

    Ao despejar uma sessão de transporte do TPM para dar espaço a uma nova entidade, o TBS executa o TPM \_ SaveContext nessa sessão de transporte.

-   Restaurando sessões de transporte

    Quando um comando TPM ExecuteTransport é enviado para o TBS, o TBS garante que a sessão de transporte referenciada no comando está fisicamente \_ presente no TPM. Se a sessão de transporte não estiver presente, o TBS a restaurará com uma chamada para \_ LoadContext do TPM.

O TBS substitui o alça virtual associado à sessão de transporte em um fluxo de comando pelo alça físico da sessão de transporte carregada no TPM. Se um comando for enviado com um alça virtual que não seja reconhecido pelo TBS no contexto do chamador, o TBS formatará um fluxo de erros para o chamador usando TPM \_ E \_ INVALID \_ HANDLE.

## <a name="exclusive-transport-sessions"></a>Sessões de transporte exclusivas

As sessões de transporte empacotada exclusivas são uma maneira de o software de nível superior determinar se qualquer outro software acessou o TPM durante uma cadeia de comandos. Eles não impedem que outros softwares acessem o TPM, apenas dão ao criador da sessão de transporte um meio de determinar que algum outro acesso ocorreu. O TBS não faz nada específico para impedir sessões de transporte exclusivas, mas é um pouco incompatível com elas. O TBS tenta duplicar o comportamento natural do TPM sendo transparente, portanto, não favorece comandos de contextos que estabelecem uma sessão de transporte exclusiva. Por exemplo, se o cliente B enviar um comando quando o cliente A estiver em uma sessão de transporte exclusiva, ele invalidará a sessão de transporte exclusiva do cliente A.

Os comandos iniciados pelo TBS também podem encerrar a sessão de transporte exclusiva. Isso acontece quando o cliente A está em uma sessão de transporte exclusiva e um comando executado pelo cliente A chama um recurso que não está fisicamente presente no TPM. Essa situação dispara o gerenciador de virtualização TBS para executar um comando LoadContext do TPM para fornecer esse recurso, que encerra a sessão de transporte exclusiva do \_ cliente A.

 

 




