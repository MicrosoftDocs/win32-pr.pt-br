---
title: Definindo a interface
description: Uma definição de interface é uma especificação formal de como um aplicativo cliente e um aplicativo de servidor se comunicam entre si.
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- Chamada de procedimento remoto RPC, tarefas, definindo a interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005201"
---
# <a name="defining-the-interface"></a>Definindo a interface

Uma definição de interface é uma especificação formal de como um aplicativo cliente e um aplicativo de servidor se comunicam entre si. A interface define como o cliente e o servidor reconhecem um ao outro, os procedimentos remotos que o aplicativo cliente pode chamar e os tipos de dados dos parâmetros e valores de retorno dos procedimentos. Ele também especifica como os dados são transmitidos entre o cliente e o servidor.

Você define essa interface no linguagem IDL da Microsoft (MIDL), que consiste em definições de linguagem C aumentadas com palavras-chave, denominadas atributos, que descrevem como os dados são transmitidos pela rede.

O arquivo de definição de interface (IDL) contém definições de tipo, atributos e protótipos de função que descrevem como os dados são transmitidos na rede. O arquivo de configuração de aplicativo (ACF) contém atributos que configuram seu aplicativo para um determinado ambiente operacional sem afetar suas características de rede.

 

 




