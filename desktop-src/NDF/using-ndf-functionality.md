---
title: Usando a funcionalidade NDF
description: A Microsoft fornece acesso à funcionalidade NDF por meio de uma API pública. Quando ocorre um problema, o aplicativo pode usar essa API para aproveitar essa funcionalidade dentro do contexto de um aplicativo específico.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca74a8a80f7babca75182625ec71dc1ec47cbc7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/10/2020
ms.locfileid: "104365817"
---
# <a name="using-ndf-functionality"></a>Usando a funcionalidade NDF

A Microsoft fornece acesso à funcionalidade NDF por meio de uma API pública. Quando ocorre um problema, o aplicativo pode usar essa API para aproveitar essa funcionalidade dentro do contexto de um aplicativo específico.

Há três estágios de executar o diagnóstico com o NDF: Criando um incidente, executando o diagnóstico e os reparos e fechando o incidente. Esta visão geral indica quais funções NDF podem ser relevantes para um cenário específico. Informações detalhadas sobre cada função podem ser encontradas na seção de [referência do NDF](ndf-reference.md) .

## <a name="creating-an-incident"></a>Criando um incidente

Uma sessão de diagnóstico NDF requer um incidente específico para diagnosticar. Há várias funções que podem ser usadas para criar um incidente. Escolha a função que mais se aproximará do que o aplicativo estava tentando fazer quando a falha ocorreu.

-   [**NdfCreateConnectivityIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident): problemas gerais de conectividade com a Internet que não precisam de informações adicionais.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex): conectando-se a uma URL http ou HTTPS.
-   [**NdfCreateSharingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident): acessando um caminho UNC ou compartilhamento de arquivos.
-   [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident): resolvendo um nome de host DNS.
-   [**NdfCreatePnrpIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident): resolvendo um nome de par PNRP.
-   [**NdfCreateGroupingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident): Ingressando em um grupo ponto a ponto.
-   [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident): conectando-se a um destino usando um soquete (quando nenhuma das outras funções se aplicam especificamente).
-   [**NdfCreateIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident): usado quando nenhum outro cenário é apropriado e a classe auxiliar NDF específica a ser invocada é conhecida (juntamente com os argumentos necessários). Usado principalmente para fins de teste por desenvolvedores de aplicativos que escreveram sua própria classe auxiliar.

## <a name="running-diagnosis-and-repairs"></a>Executando diagnóstico e reparos

Há duas maneiras de iniciar a funcionalidade de diagnóstico e reparo.

-   Usando a interface do usuário do Windows (recomendado)

    Ao executar na interface do usuário padrão do Windows, você pode simplesmente chamar a função [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) . O assistente do NDF será iniciado e ajudará o usuário a identificar (e se possível, e resolver) o problema. A função retornará após a conclusão desse processo. A interface do usuário é opcionalmente modal para seu aplicativo.

-   Usando uma interface do usuário personalizada (somente Windows 7 e posterior)

    Funções diferentes estão disponíveis para uso em cenários em que nenhuma interface do usuário está sendo mostrada, ou onde a experiência padrão do Windows não está sendo usada (como o Media Center, aplicativos inseridos e o prompt de comando). Essa opção ignora a funcionalidade de experiência do usuário fornecida no assistente do NDF, que inclui a limitação dos resultados a causas raiz totalmente suportadas, bem como a heurística para apresentar os reparos para o usuário na ordem recomendada. Ao usar essas funções, você mesmo deve fornecer qualquer funcionalidade desse tipo. Você também deve se certificar de liberar a memória usada pelos resultados do diagnóstico.

    Para iniciar o diagnóstico, chame a função [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) . Todos os problemas encontrados serão retornados ao aplicativo como uma coleção de estruturas [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) descrevendo as causas raiz identificadas e os possíveis reparos.

    Depois de selecionar um reparo (ou pedir que o usuário selecione um reparo), [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) deve ser chamado para tentar o reparo e determinar se o problema foi resolvido.

    Em alguns casos, um reparo pode ser executado com êxito, mas não resolverá o problema. Nesses casos, é recomendável fechar o incidente existente e abrir um novo. Isso garantirá que todos os novos problemas desmascarados pelo reparo inicial sejam identificados. Por exemplo, suponha que nenhuma rede sem fio tenha sido visível. Depois de redefinir o adaptador, as redes sem fio ficam visíveis, mas nenhuma delas está na lista preferencial. Esse é um novo problema que exigiria que um novo diagnóstico fosse identificado. Se uma segunda tentativa de diagnóstico não identificar problemas adicionais, um reparo diferente poderá ser tentado para resolver o problema original ou o usuário poderá ser informado de que o problema não pôde ser resolvido.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) e [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) são APIs síncronas. Se você quiser cancelar a atividade iniciada por essas funções, chame [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) de outro thread. A função retornará no próximo ponto de interrupção disponível no processo de diagnóstico ou reparo.

    A qualquer momento, você pode, opcionalmente, chamar [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) para recuperar uma cópia do log NDF para a sessão de diagnóstico atual e incluí-la com os logs do aplicativo. O log é liberado após a recuperação, e as chamadas subsequentes só recuperarão os eventos que ocorreram após a última chamada para essa função.

## <a name="closing-an-incident"></a>Fechando um incidente

Quando você terminar de diagnosticar um incidente, chame [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) para liberar recursos do sistema associados à execução de diagnósticos nesse incidente. (Observe que isso não libera objetos criados pelo [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident).
