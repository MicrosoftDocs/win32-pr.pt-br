---
title: Portando a função bbox2
description: Não há nenhum equivalente de OpenGL para a função IRIS GL bbox2.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Portação IRIS GL, função bbox2
- portando da função IRIS GL,bbox2
- portando para OpenGL da função IRIS GL,bbox2
- Portação openGL da função IRIS GL,bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012004"
---
# <a name="porting-the-bbox2-function"></a>Portando a função bbox2

Não há nenhum equivalente de OpenGL para a função IRIS GL **bbox2.**

**Para portar o código que contém funções bbox2**

1.  Crie uma nova lista de exibição (OpenGL) que contém tudo na lista de exibição iris GL equivalente, exceto a chamada para **bbox2**.
2.  Use o Windows código apropriado para desenhar um retângulo do mesmo tamanho que o IRIS GL **bbox**.

 

 




