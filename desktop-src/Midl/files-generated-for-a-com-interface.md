---
title: Arquivos gerados para uma interface COM
description: Para interfaces COM, o compilador MIDL combina todos os dados e rotinas auxiliares do servidor de objetos e do cliente em um único arquivo de proxy de interface.
ms.assetid: 13063ee8-cb41-48a7-b90b-ea08c19c5230
keywords:
- MIDL do compilador MIDL, MIDL e COM
- MIDL COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ea38ef85baa03890e323b4ba9d5eae4f295429
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917228"
---
# <a name="files-generated-for-a-com-interface"></a>Arquivos gerados para uma interface COM

Para interfaces COM, o compilador MIDL combina todos os dados e rotinas auxiliares do servidor de objetos e do cliente em um único arquivo de proxy de interface. Esse arquivo inclui os pontos de entrada substitutos para clientes e servidores. Além disso, o compilador MIDL gera um arquivo de cabeçalho de interface, um arquivo UUID de interface e um arquivo de registro de interface. Você usará todos esses arquivos ao criar uma DLL de proxy que contém o código para dar suporte ao uso da interface por aplicativos cliente e servidores de objetos. Você também usará o arquivo de cabeçalho da interface e o arquivo UUID da interface ao criar o arquivo executável para um aplicativo cliente que usa a interface.

Os tópicos a seguir descrevem cada um dos arquivos gerados para uma interface COM personalizada, que você identifica, incluindo o **\[** [](object.md) **\]** atributo Object na lista atributo de interface do arquivo IDL:

-   [O arquivo de proxy da interface](the-interface-proxy-file.md)
-   [Os arquivos de cabeçalho](the-header-files.md)
-   [O arquivo UUID de interface](the-interface-uuid-file.md)
-   [O arquivo de registro da interface](the-interface-registration-file.md)

Para obter mais informações, consulte [arquivo de configuração de aplicativo (ACF)](application-configuration-file-acf-.md), [**\_ configuração de/App**](-app-config.md), arquivo de definição de [interface (IDL)](interface-definition-idl-file.md)e [compilando e registrando uma DLL de proxy](../com/building-and-registering-a-proxy-dll.md).

 

 