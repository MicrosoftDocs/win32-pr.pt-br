---
description: Uma DRT (tabela de roteamento distribuído) existe como uma malha de nós de cooperação, onde cada nó é uma instância de um aplicativo usando a API DRT.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: Sobre tabelas de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8e82b25fee0bb6733bb21db82193d14e6cc8d621148b6d5c671fb04a3b2d85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011834"
---
# <a name="about-distributed-routing-tables"></a>Sobre tabelas de roteamento distribuído

Uma DRT (tabela de roteamento distribuído) existe como uma malha de nós de cooperação, onde cada nó é uma instância de um aplicativo usando a API DRT. Nós que publicam chaves são responsáveis por auxiliar outros nós a publicar e resolver chaves. Os nós também podem participar de uma maneira "resolver somente", o que não exige que eles ajudem os colegas. O protocolo DRT é executado em um transporte UDP/IPv6.

Um nó que publica uma chave compila e mantém uma tabela de roteamento local de outros nós na malha. Essa tabela de roteamento é otimizada para que o nó possa localizar rapidamente uma chave específica na malha localizando a chave diretamente na tabela de roteamento local ou perguntando outros nós publicando chaves numericamente perto do destino. Essa ação é repetida até que a chave necessária seja encontrada ou o nó determine que não existe tal chave.

As chaves DRT são inteiros sem sinal de 256 bits. A proximidade entre as chaves é definida pela diferença numérica entre elas. O keyspace de DRT é considerado circular. Por exemplo, o primeiro valor de chave possível e o último valor de chave possível são considerados vizinhos.

Em um DRT seguro, os nós são necessários para autenticar as chaves que eles publicam. O mecanismo pelo qual os nós autenticam chaves deve ser definido usando a API DRT quando o DRT é inicializado. Isso é feito escolhendo um provedor de segurança para o DRT. Um provedor de segurança é um módulo que pode produzir tokens usados para autenticar chaves e verificar tokens produzidos por outros nós. Ele deve implementar a interface do provedor de segurança que está definida nesta documentação. a DRT Windows 7 é fornecida com dois provedores de segurança totalmente implementados que podem ser usados para criar Windows aplicativos.

Durante a inicialização, um aplicativo também deve fornecer o DRT com um provedor de inicialização. O provedor de inicialização é um módulo que pode recuperar os pontos de extremidade de rede dos nós já presentes na malha DRT e é chamado pelo DRT quando um novo nó é estabelecido. Assim como o módulo do provedor de segurança, o provedor Bootstrap deve implementar uma interface bem definida. a DRT Windows 7 é fornecida com dois provedores de inicialização totalmente implementados.

A DRT considera os vizinhos imediatos de uma chave especial. As cinco chaves mais próximas numericamente menores e as cinco chaves mais próximas numericamente maiores que um formulário de chave publicado, o que é chamado de um conjunto de folha. Os relatórios de DRT são alterados para o conjunto de folha de uma chave por meio da API DRT.

## <a name="drt-life-cycle-and-state-transitions"></a>Ciclo de vida de DRT e transições de estado

Um aplicativo pode inicializar uma instância DRT local usando a função [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen) . Essa função dispara o processo de inicialização, em que a API DRT chama o provedor Bootstrap para aprender as chaves e os pontos de extremidade de rede de outros nós já participando do DRT. Se o provedor de inicialização localizar com êxito pelo menos um outro nó, o DRT entrará no \_ estado de DRT ativo. Nesse estado, o aplicativo pode pesquisar chaves publicadas por outros nós e pode publicar chaves que podem ser resolvidas. Se o provedor de inicialização não conseguir localizar outros nós com êxito, o DRT entrará no estado de DRT \_ sozinho. O DRT permanecerá no estado de DRT \_ sozinho e tentará realizar a inicialização periodicamente para localizar os pares e passar para o \_ estado ativo DRT.

Um nó pode fazer a transição para esses Estados de DRT \_ ativa.

| Estado do ciclo de vida | Condições                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_somente DRT       | O nó local não descobriu outros nós no DRT. Enquanto estiver nesse estado, o nó continuará a escutar outros nós dentro do DRT.<br/> Se outro nó ingressar no DRT, o nó local passará para o \_ estado ativo DRT. Se a rede estiver inoperante, ela fará a transição para DRT \_ sem \_ rede. No caso de um erro sério com o DRT, o nó passará para o \_ estado de falha DRT.<br/> |
| DRT \_ sem \_ rede | Quando um nó perde a conectividade de rede, ele faz a transição para o \_ estado DRT sem \_ rede. Neste ponto, o aplicativo pode aguardar a restauração da conectividade de rede e pode fechar o DRT.<br/>                                                                                                                                                                                                                    |
| DRT \_ com falha     | Ocorreu um erro sério no nó local. Por exemplo, se o computador local ficar sem memória física.<br/> Enquanto um nó entra nesse estado, o aplicativo deve chamar a API [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) , corrigir o problema e reinicializar o DRT com [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).<br/>                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o API de Tabela de roteamento distribuído](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Referência de API de Tabela de roteamento distribuído](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




