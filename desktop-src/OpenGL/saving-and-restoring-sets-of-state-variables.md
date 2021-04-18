---
title: Salvando e restaurando conjuntos de variáveis de estado
description: Você pode salvar e restaurar os valores de uma coleção de variáveis de estado em uma pilha de atributos com as funções glPushAttrib e glPopAttrib.
ms.assetid: 339de633-4158-4907-b985-2d75b465fb2a
keywords:
- Variáveis de estado OpenGL
- Salvando variáveis de estado OpenGL
- restaurando variáveis de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b3192c228ea35005c5755802d3cd1b873f7b7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750458"
---
# <a name="saving-and-restoring-sets-of-state-variables"></a>Salvando e restaurando conjuntos de variáveis de estado

Você pode salvar e restaurar os valores de uma coleção de variáveis de estado em uma pilha de atributos com as funções [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) . A pilha de atributos tem uma profundidade de pelo menos 16. Para obter a profundidade real, use a \_ profundidade máxima de \_ \_ pilha de Atrib GL \_ com [**glGetIntegerv**](glgetintegerv.md). Enviar por push uma pilha completa ou limpar uma vazia gera um erro.

Em geral, é mais rápido usar **glPushAttrib** e **glPopAttrib** do que obter e restaurar os valores por conta própria. Alguns valores podem ser enviados e retirados no hardware, e salvar e restaurá-los pode ter uso intensivo de recursos. Além disso, se você estiver operando em um cliente remoto, todos os dados de atributo deverão ser transferidos pela conexão de rede e de volta conforme são salvos e restaurados. No entanto, a implementação do OpenGL mantém a pilha de atributos no servidor, evitando atrasos de rede desnecessários.

O protótipo de **glPushAttrib** é:

**void** **glPushAttrib**( *máscara* de GLbitfield);

O uso de [**glPushAttrib**](glpushattrib.md) salva todos os atributos indicados por bits na *máscara* , enviando-os por push para a pilha de atributos. Para obter uma lista dos bits de máscara possíveis que você pode logicamente ou juntos para salvar qualquer combinação de atributos, consulte [grupos de atributos](attribute-groups.md). Cada bit corresponde a uma coleção de variáveis de estado individuais. Por exemplo, \_ o bit de iluminação GL \_ refere-se a todas as variáveis de estado relacionadas à iluminação, que incluem a cor do material atual; o ambiente, a difusão, a especulação e a luz emitida; uma lista das luzes que estão habilitadas; e as direções dos destaques. Quando você chama [**glPopAttrib**](glpopattrib.md), todas essas variáveis são restauradas. Para descobrir exatamente quais atributos são salvos para valores de máscara específicos, consulte [variáveis de estado OpenGL](opengl-state-variables.md).

 

 




