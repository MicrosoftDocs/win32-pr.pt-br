---
description: Implantando para comunicação mais rápida
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Implantando para comunicação mais rápida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787020"
---
# <a name="deploying-for-faster-communication"></a>Implantando para comunicação mais rápida

O desempenho é uma consideração importante ao implantar um aplicativo COM+, e o local do componente é a chave para obter o melhor desempenho de um aplicativo bem projetado.

Uma vez amplamente ocupou isso com arquiteturas escalonáveis de aplicativos, o desempenho poderia ser resolvido simplesmente movendo os componentes primários do aplicativo para um hardware mais rápido. Isso provou não ser verdadeiro. Os problemas de desempenho não surgem do desempenho de componentes individuais, mas dos links Conectando componentes.

O fator primário para o sucesso é o local. A proximidade ou o local físico, o tempo, a capacidade e a finalidade são aspectos distintos do local que se aplicam à implantação de um aplicativo do COM+, todos os quais afetam o desempenho.

O melhor desempenho é quando os componentes e os recursos do aplicativo são projetados e implantados para corresponder às demandas colocadas sobre eles pela carga de trabalho do aplicativo.

Em geral, você deve implantar componentes para minimizar a comunicação entre processos e, especialmente entre computadores, entre componentes. Se o design do seu aplicativo for eficiente, as classes dentro de um componente serão agrupadas por uso e função para maximizar a comunicação nos componentes. Na implantação de componentes, você precisa garantir que os componentes estejam localizados logicamente para usar as relações entre os componentes e para reduzir a quantidade de mensagens entre os componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Projetando para implantação](designing-for-deployment.md)
</dt> </dl>

 

 



