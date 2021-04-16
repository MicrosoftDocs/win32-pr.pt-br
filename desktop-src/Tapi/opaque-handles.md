---
description: Alguns tipos definidos por TSPI são identificadores opacos.
ms.assetid: e52ed691-0479-48da-9e06-c6a0d7a20e10
title: Identificadores opacos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df2e0b0f608b9cefc8f0f4f538bffd452a8aab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502004"
---
# <a name="opaque-handles"></a>Identificadores opacos

Alguns tipos definidos por TSPI são identificadores opacos. Eles são usados em TSPI como referências públicas para estruturas de dados privadas. Isso permite a verificação de tipos de parâmetros fornecidos aos procedimentos de interface enquanto ainda oferece uma medida de proteção de tipo. Somente o proprietário da estrutura de dados privada sabe como interpretar o tipo opaco como uma referência à sua representação de estrutura de dados. Como um exemplo de como as alças opacas são usadas, considere um dispositivo de telefone. A TAPI e o provedor de serviços normalmente mantêm estruturas de dados que representam suas respectivas exibições do dispositivo.

Em estruturas de dados de telefone típicas mantidas pela TAPI e por um provedor de serviços, cada uma contém um identificador opaco para a outra estrutura de dados. Elas eram trocadas em uma etapa de inicialização antecipada. Quando a TAPI chama uma função TSPI, ela passa o identificador opaco para se referir ao dispositivo. O provedor de serviços sabe como resolver isso como uma referência (seta) para sua estrutura de dados. Um processo semelhante ocorre quando o provedor de serviços chama uma função de retorno de chamada na TAPI.

 

 



