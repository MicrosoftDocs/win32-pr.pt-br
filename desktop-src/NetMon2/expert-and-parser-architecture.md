---
description: A figura a seguir mostra a relação entre aplicativos especialistas e analisador e outros componentes da Monitor de Rede arquitetura.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Arquitetura de especialista e analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261343005f0cb9fc7de5b7025f9ffe59f11515614ab43609c1b8da9f396e9f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795833"
---
# <a name="expert-and-parser-architecture"></a>Arquitetura de especialista e analisador

A figura a seguir mostra a relação entre aplicativos [especialistas](experts.md) e analisador e outros [componentes](parsers.md) da Monitor de Rede arquitetura.

![a relação entre aplicativos especialistas e analisador](images/nm-arch1.png)

O tráfego de rede é coletado, como quadros individuais, do driver NDIS. O Monitor de Rede driver (Nmnt.sys) encaminha os quadros para um NPP (provedor de pacotes de rede), que captura os dados e os coloca em um ou mais arquivos de captura. O NPP é uma coleção de interfaces COM usadas para capturar dados. Nesse caso, a interface [**IDelaydC**](idelaydc.md) é usada para executar uma captura atrasada.

> [!Note]  
> O NPP é usado para capturas atrasadas e em tempo real. Para capturas em tempo real, a interface [**IRTC**](irtc.md) é usada.

 

Quando os quadros de rede são armazenados no arquivo de captura e o arquivo está acessível, especialistas e analisadores podem usar a interface do usuário do Monitor de Rede e as funções Monitor de Rede fornecidas no Nmapi.dll para analisar os dados. Os arquivos de captura não ficam acessíveis até que a captura seja concluída.

 

 



