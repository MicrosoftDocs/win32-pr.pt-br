---
title: Camada de compatibilidade do aplicativo
description: Para executar aplicativos herdado em um ambiente Serviços de Área de Trabalho Remota, você pode usar a camada Serviços de Área de Trabalho Remota Compatibilidade do Aplicativo.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c3630346578801e4d2578db6f528048914412dc9ad1a8544e2c2d303188814b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099606"
---
# <a name="application-compatibility-layer"></a>Camada de compatibilidade do aplicativo

Para executar aplicativos herdado em um ambiente Serviços de Área de Trabalho Remota, você pode usar a camada Serviços de Área de Trabalho Remota Compatibilidade do Aplicativo. Quando o Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) carrega um aplicativo que não Serviços de Área de Trabalho Remota ciente, ele também carrega uma DLL que contém código de compatibilidade. Para usar a camada Serviços de Área de Trabalho Remota Compatibilidade do Aplicativo, você pode definir o sinalizador NOT TSAWARE ao compilar um aplicativo.

Se o aplicativo estiver Serviços de Área de Trabalho Remota, você poderá evitar a sobrecarga de carregar essa DLL extra e executar o código de compatibilidade.

Para indicar que seu aplicativo está Serviços de Área de Trabalho Remota, defina o sinalizador **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE** no header opcional. Se você estiver usando o linker que acompanha Microsoft Visual C++, poderá usar a opção de vinculador **TSAWARE** para definir esse sinalizador. A **ferramenta DUMPBIN** que acompanha Microsoft Visual C++ fornece a *opção /HEADERS* para determinar o estado do **sinalizador TSAWARE.** Para obter mais informações sobre como usar a **ferramenta DUMPBIN,** consulte [Referência de DUMPBIN](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Tenha cuidado ao usar o sinalizador **TSAWARE,** pois ele permite que seu aplicativo ignore todas as otimizações de Serviços de Área de Trabalho Remota compatibilidade. O **sinalizador TSAWARE** só deverá ser usado se você tiver certeza de que seu aplicativo foi projetado para o Serviços de Área de Trabalho Remota ambiente. Se o aplicativo atender aos critérios a seguir, você poderá usar com segurança o sinalizador **IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL SERVER \_ \_ AWARE.**

-   O aplicativo não usa arquivos .ini dados.
-   O aplicativo não escreve no **HKEY \_ CURRENT USER \_ durante** a instalação. Para obter mais informações, [consulte Armazenamento de User-Specific Informações](storing-user-specific-information.md).
-   O aplicativo não é executado como um serviço do sistema (ou seja, LUID=System).
-   O aplicativo não espera acesso exclusivo ao Windows ou a outros diretórios do sistema. Isso significa que o aplicativo não armazena dados temporários ou de configuração por usuário no Windows ou em outros diretórios do sistema.
-   O aplicativo não escreve no hive de **registro do computador local HKEY** para dados ou configuração específicos do usuário.
-   O aplicativo segue outras Serviços de Área de Trabalho Remota de compatibilidade mencionadas neste documento.

 

 