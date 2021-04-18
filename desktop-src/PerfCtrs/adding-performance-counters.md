---
description: Os contadores de desempenho específicos ao seu aplicativo podem ajudá-lo a ajustar o desempenho enquanto você desenvolve e depura o aplicativo.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Adicionando contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8660af9406de4dedec3ecbd76169a23b342aa7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758936"
---
# <a name="adding-performance-counters"></a>Adicionando contadores de desempenho

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e migrar contadores de desempenho existentes para usar esse método também.

Os contadores de desempenho específicos ao seu aplicativo podem ajudá-lo a ajustar o desempenho enquanto você desenvolve e depura o aplicativo. Depois que o aplicativo for concluído e instalado nos sistemas de destino, os contadores poderão ajudar os administradores do sistema a ajustar as configurações configuráveis para seu aplicativo.

## <a name="adding-a-performance-object-and-its-counters"></a>Adicionando um objeto de desempenho e seus contadores

1. Crie os tipos de objeto e contadores para o aplicativo. Para obter detalhes, consulte [design de objeto e contador](object-and-counter-design.md).
2. Crie um arquivo de inicialização (. ini) contendo os nomes e descrições dos objetos e contadores de desempenho que você fornecer. Para obter detalhes, consulte [adicionando nomes e descrições de contadores ao registro](adding-counter-names-and-descriptions-to-the-registry.md).
3. Crie um arquivo de cabeçalho (. h) contendo os deslocamentos relativos nos quais os objetos do contador e os contadores serão instalados no registro. Para obter detalhes, consulte [adicionando nomes e descrições de contadores ao registro](adding-counter-names-and-descriptions-to-the-registry.md).
4. Configure as entradas de monitoramento de desempenho necessárias no registro. Isso inclui as etapas a seguir.
    1. Crie uma chave do registro na chave de **Serviços** para o aplicativo. Se você não tiver esse nó, crie-o na seguinte chave do registro: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Para obter detalhes, consulte [criando a chave de desempenho do aplicativo](creating-the-applications-performance-key.md).
    2. Use o utilitário **lodctr** com os arquivos. ini e. h para instalar as informações no registro. Esse utilitário só terá sucesso se houver uma chave de desempenho na chave de **Serviços** para o aplicativo. Para obter detalhes, consulte [adicionando nomes e descrições de contadores ao registro](adding-counter-names-and-descriptions-to-the-registry.md).
5. Crie uma DLL de desempenho que contenha um conjunto de funções exportadas que forneçam os dados do contador consultado ao consumidor. Para obter detalhes, consulte [criando uma DLL de extensão de desempenho](creating-a-performance-extension-dll.md).
6. Modifique o arquivo de instalação do aplicativo para automatizar a adição de informações ao registro (conforme descrito na etapa 4) e copie a DLL de desempenho para o diretório do aplicativo na instalação.

Para obter informações sobre entradas de registro adicionais, consulte [criando outras entradas de registro](creating-other-registry-entries.md).
