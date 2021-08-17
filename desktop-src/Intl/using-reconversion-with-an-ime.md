---
description: Um IME implementa um recurso chamado &\# 0034;reconversion&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Usando o Reconversion com um IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5a0453b6ac94da805e00639d2a7a56fd79deca4027d23d47e33aab93e4009b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146839"
---
# <a name="using-reconversion-with-an-ime"></a>Usando o Reconversion com um IME

Um IME implementa um recurso chamado "reconversion". Normalmente, o IMM determina as listas de candidatos com base apenas em entradas digitadas pelo usuário. A reconversão permite que o IMM determine um ou mais candidatos com base na frase que o contém (o contexto). Os tipos de reconversão definidos são simples, normais e aprimorados.

A reconversão é útil quando um usuário percebe um erro de composição em um documento. O usuário pode selecionar o erro e escolher a reconversão em um menu. O IME usa o contexto para determinar a melhor substituição. O aplicativo pode usar [**ImmSetCompositionString para dar**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) suporte à reconversão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Gerenciador de Métodos de Entrada](using-input-method-manager.md)
</dt> </dl>

 

 



