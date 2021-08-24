---
description: Contadores de desempenho específicos para seu aplicativo podem ajudá-lo a ajustar o desempenho durante o desenvolvimento e depuração do aplicativo.
ms.assetid: 016386f6-4675-409e-8446-599e4ff96109
title: Adicionando contadores de desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaf66d6a0e2f0c98ad0e9fe3cc66069509d4c2391ab74e4ecaa17d6780f4561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033996"
---
# <a name="adding-performance-counters"></a>Adicionando contadores de desempenho

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em Fornecendo dados de contador usando a versão [2.0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e que você migre contadores de desempenho existentes para usar esse método também.

Contadores de desempenho específicos para seu aplicativo podem ajudá-lo a ajustar o desempenho durante o desenvolvimento e depuração do aplicativo. Depois que o aplicativo for concluído e instalado em sistemas de destino, os contadores poderão ajudar os administradores do sistema a ajustar as configurações configuráveis para seu aplicativo.

## <a name="adding-a-performance-object-and-its-counters"></a>Adicionando um objeto de desempenho e seus contadores

1. Projete os tipos de objeto e contadores para o aplicativo. Para obter detalhes, consulte [Design de objeto e contador.](object-and-counter-design.md)
2. Crie um arquivo de inicialização (.ini) que contém os nomes e as descrições dos objetos de desempenho e contadores que você fornece. Para obter detalhes, consulte [Adicionando nomes de contadores e descrições ao Registro](adding-counter-names-and-descriptions-to-the-registry.md).
3. Crie um arquivo de header (.h) contendo os deslocamentos relativos nos quais os objetos e contadores do contador serão instalados no Registro. Para obter detalhes, consulte [Adicionando nomes de contadores e descrições ao Registro](adding-counter-names-and-descriptions-to-the-registry.md).
4. Configurar as entradas de monitoramento de desempenho necessárias no Registro. Isso inclui as etapas a seguir.
    1. Crie uma chave do Registro na **chave Serviços** para o aplicativo. Se você não tiver esse nó, crie-o na seguinte chave do Registro: `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` . Para obter detalhes, [consulte Criando a chave de desempenho do aplicativo.](creating-the-applications-performance-key.md)
    2. Use o **utilitário lodctr** com os arquivos .ini e .h para instalar as informações no Registro. Esse utilitário só terá êxito se houver uma chave de desempenho na **chave serviços** para o aplicativo. Para obter detalhes, consulte [Adicionando nomes de contadores e descrições ao Registro](adding-counter-names-and-descriptions-to-the-registry.md).
5. Crie uma DLL de desempenho que contém um conjunto de funções exportadas que fornecem os dados do contador consultado para o consumidor. Para obter detalhes, consulte [Criando uma DLL de extensão de desempenho](creating-a-performance-extension-dll.md).
6. Modifique o arquivo de instalação do aplicativo para automatizar a adição de informações ao Registro (conforme descrito na etapa 4) e copie sua DLL de desempenho para o diretório do aplicativo na instalação.

Para obter informações sobre entradas adicionais do Registro, consulte [Criando outras entradas do Registro](creating-other-registry-entries.md).
