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
# <a name="defining-the-interface"></a><span data-ttu-id="bdd75-104">Definindo a interface</span><span class="sxs-lookup"><span data-stu-id="bdd75-104">Defining the Interface</span></span>

<span data-ttu-id="bdd75-105">Uma definição de interface é uma especificação formal de como um aplicativo cliente e um aplicativo de servidor se comunicam entre si.</span><span class="sxs-lookup"><span data-stu-id="bdd75-105">An interface definition is a formal specification for how a client application and a server application communicate with each other.</span></span> <span data-ttu-id="bdd75-106">A interface define como o cliente e o servidor reconhecem um ao outro, os procedimentos remotos que o aplicativo cliente pode chamar e os tipos de dados dos parâmetros e valores de retorno dos procedimentos.</span><span class="sxs-lookup"><span data-stu-id="bdd75-106">The interface defines how the client and server recognize each other, the remote procedures that the client application can call, and the data types for those procedures' parameters and return values.</span></span> <span data-ttu-id="bdd75-107">Ele também especifica como os dados são transmitidos entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="bdd75-107">It also specifies how the data is transmitted between client and server.</span></span>

<span data-ttu-id="bdd75-108">Você define essa interface no linguagem IDL da Microsoft (MIDL), que consiste em definições de linguagem C aumentadas com palavras-chave, denominadas atributos, que descrevem como os dados são transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="bdd75-108">You define this interface in the Microsoft Interface Definition Language (MIDL) which consists of C-language definitions augmented with keywords, called attributes, which describe how the data is transmitted over the network.</span></span>

<span data-ttu-id="bdd75-109">O arquivo de definição de interface (IDL) contém definições de tipo, atributos e protótipos de função que descrevem como os dados são transmitidos na rede.</span><span class="sxs-lookup"><span data-stu-id="bdd75-109">The interface definition (IDL) file contains type definitions, attributes and function prototypes that describe how data is transmitted on the network.</span></span> <span data-ttu-id="bdd75-110">O arquivo de configuração de aplicativo (ACF) contém atributos que configuram seu aplicativo para um determinado ambiente operacional sem afetar suas características de rede.</span><span class="sxs-lookup"><span data-stu-id="bdd75-110">The application configuration (ACF) file contains attributes that configure your application for a particular operating environment without affecting its network characteristics.</span></span>

 

 




