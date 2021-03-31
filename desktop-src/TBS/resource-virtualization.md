---
title: Virtualização de recursos
description: Virtualização de recursos
ms.assetid: ead0e99a-94da-4e80-bb68-d8f4b199173d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f340b1a1bddfb3fd591452e028c80403b9c7e02f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636341"
---
# <a name="resource-virtualization"></a>Virtualização de recursos

A função principal do TBS é compartilhar com eficiência determinados recursos limitados do TPM: chaves, autorização e sessões de transporte.

Quando uma instância de um desses recursos é criada, o TBS cria uma instância virtual do recurso e retorna um identificador para essa instância virtual no fluxo do comando de resultado (em vez da instância de identificador real retornada pelo TPM). O TBS mantém um mapeamento entre o identificador virtual e o identificador real internamente. Se o TPM ficar sem espaço para conter mais recursos de um determinado tipo, as instâncias existentes do recurso serão salvas e removidas seletivamente até que o TPM possa manter o novo recurso. Quando os recursos antigos forem requeridos novamente, o TBS carregará os contextos salvos (salvando e removendo outros recursos, se necessário) antes de enviar o comando.

Toda a virtualização no TBS é executada em nome de um contexto específico. Cada contexto só tem permissão para acessar recursos virtuais criados especificamente em seu nome, bem como os recursos físicos no TPM que corresponde a esses recursos virtuais. Por padrão, o número total de todos os recursos virtualizados é limitado a 500. Esse número pode ser alterado criando ou modificando um valor de registro **DWORD** chamado **MaxResources** em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **TPM**. O uso de recursos TBS em tempo real pode ser observado usando a ferramenta Monitor de desempenho para controlar o número de recursos TBS. Essa restrição se tornou obsoleta com o Windows 8 e o Windows Server 2012.

Os recursos limitados do TPM que não são virtualizados pelo TBS (como contadores e armazenamento NV) devem ser compartilhados de forma cooperativa entre as pilhas de software.

> [!Note]  
> Essa virtualização de identificador faz com que os comandos que incluem os principais identificadores no cálculo dos parâmetros de autorização HMAC falhem. Como resultado, muitos comandos preteridos no TPM versão 1,2 não podem ser usados pelo software de aplicativo no ambiente TBS.

 

## <a name="resource-limits"></a>Limites de recursos

O TPM permite que os chamadores consultem seus recursos para determinar a quantidade de espaço disponível para determinados tipos de recursos. Alguns desses limites de recursos, como a quantidade de espaço disponível para chaves, sessões de autorização e sessões de transporte, são efetivamente estendidos pelos TBS por meio da virtualização. As limitações do TBS, que são controladas pela configuração do registro **MaxResources** , geralmente são muito maiores do que as limitações reais do hardware do TPM subjacente. Nenhum mecanismo é fornecido para consultar limitações de TBS separadamente dos limites de hardware do TPM. Essa limitação de TBS se tornou obsoleta com o Windows 8 e o Windows Server 2012.

## <a name="keys"></a>simétricas

O TBS virtualiza os principais identificadores para que as chaves possam ser descarregadas de forma transparente do TPM quando não estiverem sendo usadas e carregadas de volta no TPM quando forem necessárias. Quando uma chave é criada, o TBS associa um identificador virtual à chave carregada. O mesmo identificador virtual é usado para o tempo de vida do recurso. Os identificadores de chave virtual são válidos apenas no contexto que os criou, e os recursos associados não são preservados além da vida útil do contexto.

-   Criando chaves com \_ LOADKEY2 TPM

    Se uma chave for criada usando o comando TPM \_ LoadKey2, TPM2 \_ createprimário, TPM2 \_ Load ou TPM2 \_ loadexternal, o TBS substituirá o identificador no fluxo de retorno de bytes por um identificador de chave virtual de sua escolha. Como resultado, o TBS garante que cada identificador virtual seja exclusivo. Se o TBS detectar uma colisão (um evento extremamente improvável), o TBS descarregará a chave do TPM e informará o software de chamada. O software pode enviar a operação novamente. Esse processo pode ser repetido até que o TBS obtenha um identificador de chave exclusivo.

-   Limpando chaves

    O TBS invalida o identificador de chave virtual quando recebe uma mensagem de FlushSpecific do TPM \_ ou TPM2 \_ FlushContext para esse identificador virtual do contexto do cliente. Se a chave estiver fisicamente presente no TPM quando a mensagem de liberação for recebida, o TBS liberará a chave do TPM nesse momento.

-   Removendo chaves temporariamente

    Ao remover uma chave do TPM para liberar espaço para um novo item, o TBS executa um \_ comando TPM SaveContext ou TPM2 \_ ContextSave na chave antes de removê-lo.

-   Restaurando chaves

    Quando um comando que faz referência a uma chave carregada é enviado para o TBS, ele garante que a chave esteja fisicamente presente no TPM. Se a chave não estiver presente, o TBS a restaurará com uma chamada para \_ Loadcontext do TPM ou TPM2 \_ ContextLoad. Se uma chave não puder ser restaurada para o TPM, o TBS retornará um manipulador de chaves do TPM \_ E \_ inválido \_ como resultado do TPM.

O TBS substitui cada identificador virtual associado a uma chave em um fluxo de comando pelo identificador físico da chave carregada no TPM. Se um comando for enviado com um identificador virtual que não é reconhecido pelo TBS no contexto do chamador, o TBS formatará um fluxo de erro para o chamador com o \_ manipulador de \_ keyHandle inválido E o TPM \_ .

## <a name="authorization-sessions"></a>Sessões de autorização

As sessões de autorização são criadas chamando o TPM \_ OIAP, TPM \_ oSAP ou TPM \_ DSAP. Em cada caso, o fluxo de bytes de retorno contém o identificador de TPM físico da sessão de autorização criada recentemente. O TBS substitui isso por um identificador virtual. Quando a sessão de autorização é referenciada posteriormente, o TBS substitui o identificador virtual no fluxo de comando pelo identificador físico da sessão de autorização. O TBS garante que o tempo de vida da sessão de autorização virtual corresponda ao da sessão de autorização física. Se um cliente tentar usar um identificador virtual expirado, o TBS formatará um fluxo de erro com o erro TPM \_ INVALIDAUTHHANDLE.

Os slots de sessão são limitados e os TBS podem ficar sem Slots externos para salvar contextos de sessão de autorização. Se isso acontecer, o TBS escolherá uma sessão de autorização para invalidar, de modo que o novo contexto possa ser salvo com êxito. Um aplicativo que tenta usar o contexto antigo precisará recriar a sessão de autorização.

O TBS invalida a sessão de autorização virtual quando ocorre um dos seguintes casos:

-   O sinalizador continue-use associado à sessão de autorização no fluxo de comando retornado do TPM é **false**.
-   Um comando que usa uma sessão de autorização falha.
-   É executado um comando que invalida a sessão de autorização associada ao comando (como TPM \_ CreateWrapKey).
-   Uma chave associada a uma sessão OSAP ou DSAP é removida do TPM com uma chamada para o TPM \_ FlushSpecific ou TPM2 \_ FlushContext (sem considerar se esse comando foi originado no TBS ou com um software de nível superior).

    O TBS ressincronizará automaticamente as sessões de autorização após a execução bem-sucedida de determinados comandos não determinísticos para garantir que o estado TBS permaneça consistente com o estado do TPM. Os comandos afetados são:

    -   Gerenciar o delegado do TPM \_ Ord \_ \_
    -   \_ \_ CreateOwnerDelegation delegado do TPM Ord \_
    -   \_ \_ LoadOwnerDelegation delegado do TPM Ord \_

Em cada um dos casos a seguir, a sessão de autorização no TPM é liberada automaticamente pelo TPM:

-   Criando sessões de autorização

    Os identificadores de sessão de autorização virtual são válidos apenas no contexto que os criou e os recursos associados não são preservados além da vida útil do contexto associado.

-   Limpando sessões de autorização

    O TBS invalida a sessão de autorização virtual se receber um \_ comando FlushSpecific do TPM ou TPM2 \_ FlushContext para o identificador virtual do contexto do cliente. Se a sessão de autorização estiver fisicamente presente no TPM quando o comando flush for recebido, o TBS liberará a sessão física do TPM imediatamente.

-   Removendo sessões de autorização temporariamente

    Ao remover uma sessão de autorização do TPM para liberar espaço para uma nova entidade, o TBS executa o TPM \_ SaveContext ou o TPM2 \_ ContextSave nessa sessão de autorização.

-   Restaurando sessões de autorização

    Quando um comando TPM autorizado é enviado para o TBS, o TBS garante que todas as sessões de autorização virtual referenciadas no comando estejam fisicamente presentes no TPM. Se qualquer uma das sessões de autorização não estiver presente, o TBS as restaurará com uma chamada para \_ Loadcontext do TPM ou TPM2 \_ ContextLoad. Se uma sessão de autorização não puder ser restaurada para o TPM, o TBS retornará um \_ \_ identificador de TPM E inválido \_ como o resultado do TPM.

O TBS substitui cada identificador virtual associado a uma sessão de autorização em um fluxo de comando com o identificador físico da sessão de autorização carregada no TPM.

Se um comando for enviado com um identificador virtual que não é reconhecido pelo TBS no contexto do chamador, o TBS formatará um fluxo de erro para o chamador com o manipulador do TPM \_ E \_ o \_ identificador inválido.

## <a name="transport-sessions"></a>Sessões de transporte

> [!Note]  
> A manipulação de sessões de transporte, conforme descrito aqui, é específica para o Windows Vista e o Windows Server 2008.

 

As sessões de transporte são um mecanismo fornecido pelo TPM que permite que uma pilha de software criptografe dados em um comando enquanto ele passa entre o software e o TPM. Isso impede que um adversário intercepte os dados conforme eles passam pelo barramento de hardware.

> [!IMPORTANT]
> Somente os dados de carga são criptografados. Os comandos que estão sendo executados ainda podem ser identificados.

 

Infelizmente, esse mecanismo também impede que os TBS examinem os dados de carga. Na maioria dos casos, isso não é um problema porque o TBS modifica apenas os identificadores, não os dados de carga. No entanto, no caso do TPM \_ loadcontext, por exemplo, o identificador de recurso retornado é coberto pela criptografia. Portanto, o TBS impede tentativas de executar uma \_ operação Loadcontext do TPM coberta por uma sessão de transporte.

O TBS bloqueia os seguintes comandos na sessão de transporte:

-   \_ESTABLISHTRANSPORT TPM
-   \_EXECUTETRANSPORT TPM
-   \_Identificador de término do TPM \_
-   \_LOADKEY TPM
-   \_EVICTKEY TPM
-   \_SAVEKEYCONTEXT TPM
-   \_LOADKEYCONTEXT TPM
-   \_SAVEAUTHCONTEXT TPM
-   \_LOADAUTHCONTEXT TPM
-   \_SAVECONTEXT TPM
-   Contexto loadtpm \_
-   \_FLUSHSPECIFIC TPM

Quando qualquer um desses comandos é coberto por uma sessão de transporte, o TBS retorna o \_ comando TPM E \_ Embedded \_ \_ sem suporte como resultado do TPM.

Os identificadores de sessão de transporte são virtualizados de maneira semelhante a identificadores de chave e identificadores de autorização. Há um número limitado de Slots de contexto de sessão de transporte salvos disponíveis no TPM.

O TBS invalida a sessão de transporte virtual se qualquer um dos seguintes casos ocorrer:

-   O sinalizador continue-use associado à sessão de transporte no fluxo de comando de retorno do TPM é **false**.

    Assim como nas sessões de autorização acima, o TBS ressincronizará automaticamente as sessões de transporte após a execução bem-sucedida de determinados comandos não determinísticos para garantir que o estado TBS permaneça consistente com o estado do TPM. Os comandos afetados são:

    -   Gerenciar o delegado do TPM \_ Ord \_ \_
    -   \_ \_ CreateOwnerDelegation delegado do TPM Ord \_
    -   \_ \_ LoadOwnerDelegation delegado do TPM Ord \_

Em cada um desses casos, a sessão de transporte no TPM será liberada automaticamente pelo TPM:

-   Criando sessões de transporte

    O TBS cria um identificador virtual para cada sessão de transporte criada por um cliente. Os identificadores de transporte virtual são válidos apenas no contexto que os criou, e os recursos associados não são preservados além da vida útil do contexto associado.

-   Limpando sessões de transporte

    O TBS invalida a sessão de transporte virtual se receber um \_ comando FlushSpecific do TPM para o identificador virtual do contexto do cliente. Se a sessão de transporte estiver fisicamente presente no TPM quando o comando flush for recebido, o TBS liberará a sessão física do TPM imediatamente.

-   Removendo sessões de transporte temporariamente

    Ao remover uma sessão de transporte do TPM para liberar espaço para uma nova entidade, o TBS executa o \_ SaveContext do TPM nessa sessão de transporte.

-   Restaurando sessões de transporte

    Quando um \_ comando ExecuteTransport do TPM é enviado para o TBS, o TBS garante que a sessão de transporte referida no comando esteja fisicamente presente no TPM. Se a sessão de transporte não estiver presente, o TBS a restaurará com uma chamada para \_ Loadcontext do TPM.

O TBS substitui o identificador virtual associado à sessão de transporte em um fluxo de comando pelo identificador físico da sessão de transporte carregada no TPM. Se um comando for enviado com um identificador virtual que não é reconhecido pelo TBS no contexto do chamador, o TBS formata um fluxo de erro para o chamador usando o TPM E o \_ \_ identificador inválido \_ .

## <a name="exclusive-transport-sessions"></a>Sessões de transporte exclusivas

As sessões de transporte encapsuladas exclusivas são uma maneira para o software de nível superior determinar se algum outro software acessou o TPM durante uma cadeia de comandos. Eles não impedem que outro software acesse o TPM, basta dar ao criador da sessão de transporte um meio de determinar que algum outro acesso ocorreu. O TBS não faz nada específico para impedir sessões de transporte exclusivas, mas é um pouco compatível com elas. O TBS tenta duplicar o comportamento natural do TPM, sendo transparente, de modo que não favorece comandos de contextos que estabelecem uma sessão de transporte exclusiva. Por exemplo, se o cliente B enviar um comando quando o cliente A estiver em uma sessão de transporte exclusiva, ele invalidará a sessão de transporte exclusiva do cliente A.

Os comandos iniciados por TBS também podem encerrar a sessão de transporte exclusiva. Isso acontece quando o cliente A está em uma sessão de transporte exclusiva e um comando executado pelo cliente A chama um recurso que não está fisicamente presente no TPM. Essa situação dispara o Gerenciador de virtualização de TBS para executar um \_ comando Loadcontext do TPM para fornecer esse recurso, que encerra a sessão de transporte exclusiva do cliente a.

 

 




