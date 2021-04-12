---
title: Incluindo atributos no catálogo global
description: O catálogo global de uma floresta inclui uma réplica parcial de cada objeto na floresta.
ms.assetid: 185467ed-7bcf-41e9-9862-02412009c437
ms.tgt_platform: multiple
keywords:
- Atributos incluídos no AD do catálogo global
- Atributos de anúncio, incluídos no catálogo global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffbffd39e92456e6de7eccc6127f8a1351a4466
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453961"
---
# <a name="including-attributes-in-the-global-catalog"></a>Incluindo atributos no catálogo global

O catálogo global de uma floresta inclui uma réplica parcial de cada objeto na floresta. Para cada objeto, o catálogo global inclui apenas um subconjunto dos atributos de cada objeto. O atributo [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) de um objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) será definido como **true** se o atributo for replicado para o catálogo global.

Os atributos com as seguintes características são apropriados para o armazenamento no catálogo global:

-   O atributo é globalmente interessante, seja porque o atributo é necessário para localizar objetos que podem ocorrer em qualquer lugar na floresta ou porque o acesso de leitura ao atributo é valioso mesmo quando o objeto completo não está acessível. Um exemplo do primeiro tipo é o atributo [**Location**](/windows/desktop/ADSchema/a-location) , que pode ser usado para localizar um objeto [**PrintQueue**](/windows/desktop/ADSchema/c-printqueue) . Um exemplo do segundo tipo é [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber), pois você pode chamar alguém mesmo que não possa acessar uma réplica completa de seu objeto de [**usuário**](/windows/desktop/ADSchema/c-user) .
-   O volatilidade do atributo é muito baixo. Isso é importante, porque se uma classe de atributo estiver incluída no catálogo global, as alterações a cada valor dessa classe de atributo em toda a floresta da empresa serão replicadas para todos os servidores de catálogo global na empresa.
-   O tamanho do valor do atributo é pequeno. "Pequeno" é altamente subjetivo: ao colocar um atributo no catálogo global, considere o impacto de replicar o atributo para todos os servidores de catálogo global na empresa. Quanto menor o atributo, menor o impacto. Como a replicação ocorre somente quando o atributo é alterado, o impacto da replicação também é menor, pois o volatilidade diminui, de modo que um atributo grande com volatilidade muito baixo pode ter um impacto geral menor do que um atributo pequeno com alto volatilidade.

Ao decidir se deve ou não posicionar um atributo no catálogo global, lembre-se de que você está negociando a replicação e o armazenamento em disco maiores em servidores de catálogo global para um desempenho de consulta potencialmente mais rápido. Normalmente, você usaria o catálogo global para pesquisar um objeto de interesse para que possa ler os atributos selecionados do objeto. Se os atributos nos quais você está interessado forem replicados para o catálogo global, você poderá lê-los diretamente do catálogo global. Como alternativa, para ler atributos que não são replicados para o catálogo global, você deve executar etapas adicionais para recuperá-los. Nesse caso, depois de Pesquisar o catálogo global para localizar o objeto de interesse, você deve ler o nome distinto do objeto do catálogo global, usar o DN para associar diretamente a uma réplica completa do objeto, que pode estar em um servidor diferente e, por fim, ler os atributos não globais do catálogo da réplica completa do objeto.

Os atributos consultados e referenciados com frequência, como nome do funcionário e número de telefone, são bons para serem incluídos no catálogo global. Um atributo referenciado com pouca frequência, como "driverVersion" para impressoras, é o mais bem deixado do catálogo global.

 

 