---
description: A figura a seguir mostra a relação entre os aplicativos de especialista e analisador e outros componentes da arquitetura de Monitor de Rede.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Arquitetura de expert e parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089977"
---
# <a name="expert-and-parser-architecture"></a>Arquitetura de expert e parser

A figura a seguir mostra a relação entre os aplicativos de [especialista](experts.md) e [analisador](parsers.md) e outros componentes da arquitetura de monitor de rede.

![a relação entre aplicativos de especialista e analisador](images/nm-arch1.png)

O tráfego de rede é coletado, como quadros individuais, do driver NDIS. O driver de Monitor de Rede (Nmnt.sys), em seguida, roteia os quadros para um NPP (provedor de pacotes de rede), que captura os dados e os coloca em um ou mais arquivos de captura. O NPP é uma coleção de interfaces COM usadas para capturar dados. Nesse caso, a interface [**IDelaydC**](idelaydc.md) é usada para executar uma captura atrasada.

> [!Note]  
> O NPP é usado para capturas atrasadas e em tempo real. Para capturas em tempo real, a interface [**IRTC**](irtc.md) é usada.

 

Quando os quadros de rede são armazenados no arquivo de captura e o arquivo é acessível, os especialistas e analisadores podem usar a interface do usuário do Monitor de Rede e as funções Monitor de Rede fornecidas no Nmapi.dll para analisar os dados. Os arquivos de captura não estarão acessíveis até que a captura seja concluída.

 

 



