---
title: Configurando o Serviço de Nome para Windows 3.x ou MS-DOS
description: RPC (Chamada de Procedimento Remoto) e configurando o serviço de nome para Windows 3.x ou MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24884c782913c47806c702ff129594c6524fe7c0e731561de405f3b6a360c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022426"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>Configurando o Serviço de Nome para Windows 3.x ou MS-DOS

Quando você executar Setup.exe para instalar a biblioteca em tempo de executar RPC de 16 bits, ele solicitará que você selecione um provedor de serviços de nome:

-   Se você escolher **Instalar Provedor de Serviços de Nome Padrão**, o NSP padrão, Microsoft Locator, será instalado.
-   Se você escolher **Instalar Provedor de Serviços de** Nome Personalizado , conclua a caixa de diálogo Definir Endereço de Rede para instalar o Serviço de Diretório de Célula do DCE como seu NSP.  O Serviço de Diretório de Célula do DCE é o NSP usado com servidores DCE.

O endereço de rede é o nome do computador host que executa o daemon NSI (nsid). Esse computador atua como um gateway para o Serviço de Diretório de Célula do DCE, passando chamadas de função NSI entre computadores que executem sistemas operacionais Da Microsoft e computadores DCE. O endereço de rede pode ter 80 caracteres ou menos, por exemplo, 11.1.9.169 é um endereço válido.

 

 




