---
title: Camada de compatibilidade de aplicativos
description: Para executar aplicativos herdados em um ambiente Serviços de Área de Trabalho Remota, você pode usar a camada de compatibilidade de aplicativos Serviços de Área de Trabalho Remota.
ms.assetid: 6e61ed45-4fcb-4aee-b8cc-638a9b87ce00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7bbc5867e42951783d3666aa770cdcc45406f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782882"
---
# <a name="application-compatibility-layer"></a>Camada de compatibilidade de aplicativos

Para executar aplicativos herdados em um ambiente Serviços de Área de Trabalho Remota, você pode usar a camada de compatibilidade de aplicativos Serviços de Área de Trabalho Remota. Quando o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) carrega um aplicativo que não está Serviços de Área de Trabalho Remota ciente, ele também carrega uma DLL que contém o código de compatibilidade. Para usar a camada de compatibilidade de aplicativos Serviços de Área de Trabalho Remota, você pode definir o sinalizador NOT TSAWARE ao compilar um aplicativo.

Se seu aplicativo estiver Serviços de Área de Trabalho Remota ciente, você poderá evitar a sobrecarga de carregar essa DLL extra e executar o código de compatibilidade.

Para indicar que seu aplicativo está Serviços de Área de Trabalho Remota ciente, defina o sinalizador de **reconhecimento de imagem \_ DLLCHARACTERISTICS \_ terminal \_ Server \_** no cabeçalho opcional. Se você estiver usando o vinculador fornecido com Microsoft Visual C++, poderá usar a opção vinculador **TSAWARE** para definir esse sinalizador. A ferramenta **DUMPBIN** fornecida com Microsoft Visual C++ fornece a opção */Headers* para determinar o estado do sinalizador **TSAWARE** . Para obter mais informações sobre como usar a ferramenta **DUMPBIN** , consulte [referência do DUMPBIN](/cpp/build/reference/dumpbin-reference?view=vs-2019).

Tenha cuidado ao usar o sinalizador **TSAWARE** porque ele permite que seu aplicativo ignore quaisquer serviços de área de trabalho remota otimizações de compatibilidade. O sinalizador **TSAWARE** só deverá ser usado se você tiver certeza de que seu aplicativo foi projetado para o ambiente de serviços de área de trabalho remota. Se seu aplicativo atender aos critérios a seguir, você poderá usar com segurança o sinalizador de **reconhecimento de imagem do \_ DLLCHARACTERISTICS \_ terminal \_ Server \_** .

-   O aplicativo não usa arquivos. ini.
-   O aplicativo não grava em **HKEY \_ Current \_ User** durante a instalação. Para obter mais informações, consulte [armazenando informações de User-Specific](storing-user-specific-information.md).
-   O aplicativo não é executado como um serviço de sistema (ou seja, LUID = System).
-   O aplicativo não espera acesso exclusivo ao Windows ou a outros diretórios do sistema. Isso significa que o aplicativo não armazena dados de configuração ou temporários por usuário no Windows ou em outros diretórios do sistema.
-   O aplicativo não grava no hive do registro do **computador local hKey** para configuração ou dados específicos do usuário.
-   O aplicativo segue outras diretrizes de compatibilidade Serviços de Área de Trabalho Remota mencionadas neste documento.

 

 