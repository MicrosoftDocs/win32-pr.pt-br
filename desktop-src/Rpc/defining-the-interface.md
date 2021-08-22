---
title: Definindo a interface
description: Uma definição de interface é uma especificação formal de como um aplicativo cliente e um aplicativo de servidor se comunicam entre si.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Chamada de procedimento remoto RPC, tarefas, definindo a interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 654c6690e6980e659df8a68652aec59b296b7d88543eca02605f489a2c3a909c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930800"
---
# <a name="defining-the-interface"></a>Definindo a interface

Uma definição de interface é uma especificação formal de como um aplicativo cliente e um aplicativo de servidor se comunicam entre si. A interface define como o cliente e o servidor reconhecem um ao outro, os procedimentos remotos que o aplicativo cliente pode chamar e os tipos de dados dos parâmetros e valores de retorno dos procedimentos. Ele também especifica como os dados são transmitidos entre o cliente e o servidor.

Você define essa interface no linguagem IDL da Microsoft (MIDL), que consiste em definições de linguagem C aumentadas com palavras-chave, denominadas atributos, que descrevem como os dados são transmitidos pela rede.

O arquivo de definição de interface (IDL) contém definições de tipo, atributos e protótipos de função que descrevem como os dados são transmitidos na rede. O arquivo de configuração de aplicativo (ACF) contém atributos que configuram seu aplicativo para um determinado ambiente operacional sem afetar suas características de rede.

 

 




