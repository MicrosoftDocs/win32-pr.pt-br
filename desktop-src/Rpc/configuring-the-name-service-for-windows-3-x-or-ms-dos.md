---
title: Configurando o serviço de nome para Windows 3. x ou MS-DOS
description: RPC (chamada de procedimento remoto) e configuração do serviço de nome para Windows 3. x ou MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005674"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configurando o serviço de nome para Windows 3. x ou MS-DOS

Quando você executa Setup.exe para instalar a biblioteca de tempo de execução RPC de 16 bits, ele solicita que você selecione um provedor de serviços de nome:

-   Se você escolher **instalar provedor de serviço de nome padrão**, o NSP padrão, Microsoft Locator, será instalado.
-   Se você escolher **instalar provedor de serviço de nome personalizado**, conclua a caixa de diálogo **Definir endereço de rede** para instalar o serviço de diretório de célula do DCE como seu NSP. O serviço de diretório de célula do DCE é o NSP usado com servidores DCE.

O endereço de rede é o nome do computador host que executa o daemon de NSI (nsid). Esse computador atua como um gateway para o serviço de diretório de célula do DCE, passando chamadas de função de NSI entre computadores que executam sistemas operacionais Microsoft e computadores DCE. O endereço de rede pode ter de 80 caracteres ou menos — por exemplo, 11.1.9.169 é um endereço válido.

 

 




