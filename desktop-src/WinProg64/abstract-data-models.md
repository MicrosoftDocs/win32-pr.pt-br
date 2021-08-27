---
title: Modelos de dados abstratos
description: Cada aplicativo e cada sistema operacional tem um modelo de dados abstrato.
ms.assetid: c670d92b-e64d-4d4c-a30c-cd4fb4f2d0b9
keywords:
- abstract data models 64-bit Windows Programming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ad383e52c49997e43aa90301e7e417ef8cfeb089c9f6da151542b193b25071
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121856"
---
# <a name="abstract-data-models"></a>Modelos de dados abstratos

Cada aplicativo e cada sistema operacional tem um modelo de dados abstrato. Muitos aplicativos não expõem explicitamente esse modelo de dados, mas o modelo orienta a maneira como o código do aplicativo é escrito. No modelo de programação de 32 bits (conhecido como modelo ILP32), os tipos de dados integer, long e pointer têm 32 bits de comprimento. A maioria dos desenvolvedores usou esse modelo sem perceber. Para o histórico da API do Win32, essa foi uma suposição válida (embora não necessariamente segura) a ser assumida.

Em 64 bitsWindows, essa suposição de paridade em tamanhos de tipo de dados é inválida. Fazer com que todos os tipos de dados de 64 bits de comprimento percam espaço, pois a maioria dos aplicativos não precisa do tamanho maior. No entanto, os aplicativos precisam de ponteiros para dados de 64 bits e precisam da capacidade de ter tipos de dados de 64 bits em casos selecionados. Essas considerações levaram à seleção de um modelo de dados abstrato chamado LLP64 (ou P64). No modelo de dados LLP64, somente os ponteiros se expandem para 64 bits; todos os outros tipos de dados básicos (inteiro e longo) permanecem com 32 bits de comprimento.

Inicialmente, a maioria dos aplicativos executados em Windows de 64 bits terá sido portada de 32 bits Windows. É uma meta que a mesma origem, cuidadosamente escrita, deve ser executado em 32 e 64 bits Windows. Definir o modelo de dados não facilita essa tarefa. No entanto, garantir que o modelo de dados afete apenas os tipos de dados de ponteiro é a primeira etapa. A segunda etapa é definir um conjunto de novos tipos de dados que permitem aos desenvolvedores tamanho automático de seus dados relacionados a ponteiros. Isso permite que os dados associados aos ponteiros alterem o tamanho à medida que o tamanho do ponteiro muda de 32 bits para 64 bits. Os tipos de dados básicos permanecem com 32 bits de comprimento, portanto, não há nenhuma alteração no tamanho dos dados no disco, dados compartilhados por uma rede ou dados compartilhados por meio de arquivos mapeados em memória. Isso alivia os desenvolvedores de grande parte do esforço envolvido na portação de código de 32 bits para 64 bits Windows.

Esses novos tipos de dados foram adicionados aos arquivos de Windows de API. Portanto, você pode começar a usar os novos tipos agora. Para obter mais informações, consulte [The New Data Types](the-new-data-types.md).

 

 




