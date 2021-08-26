---
description: A arquitetura da DLL do analisador deve fornecer os recursos mostrados na ilustração a seguir.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitetura de DLL do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b2c3ead77d5172bc57fa3bc1c8b6001b9c690cd254dc436ac93f504ddb732
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962856"
---
# <a name="parser-dll-architecture"></a>Arquitetura de DLL do analisador

A arquitetura da DLL do analisador deve fornecer os recursos mostrados na ilustração a seguir. Esteja ciente de que alguns recursos exigem a implementação de apenas um ponto de entrada. No entanto, se a DLL do analisador for compatível com vários protocolos, o recurso exigirá a implementação de vários pontos de entrada.

![recursos de dll do analisador](images/parserarchitecture1.png)



| Para obter informações sobre                                                  | Consulte                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Como implementar funções de exportação de DLL do analisador.                          | [Escrevendo um analisador de protocolo](writing-a-protocol-parser.md)             |
| Funções e estruturas específicas que os analisadores usam – tópicos de referência. | [Funções e estruturas do analisador](parser-functions-and-structures.md) |



 

 

 



