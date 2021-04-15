---
description: A arquitetura da DLL do analisador deve fornecer os recursos mostrados na ilustração a seguir.
ms.assetid: 2da5d4bc-a219-47b5-8522-1237f7bcac16
title: Arquitetura de DLL do analisador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7852029a892d8b74c954cbc2d7341fcaf29032fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461343"
---
# <a name="parser-dll-architecture"></a>Arquitetura de DLL do analisador

A arquitetura da DLL do analisador deve fornecer os recursos mostrados na ilustração a seguir. Lembre-se de que alguns recursos exigem a implementação de apenas um ponto de entrada. No entanto, se a DLL do analisador der suporte a vários protocolos, o recurso exigirá a implementação de vários pontos de entrada.

![recursos de DLL do analisador](images/parserarchitecture1.png)



| Para obter informações sobre                                                  | Consulte                                                                    |
|------------------------------------------------------------------------|------------------------------------------------------------------------|
| Como implementar funções de exportação de DLL do parser.                          | [Gravando um analisador de protocolo](writing-a-protocol-parser.md)             |
| Funções específicas e estruturas que os analisadores usam — tópicos de referência. | [Funções e estruturas do analisador](parser-functions-and-structures.md) |



 

 

 



