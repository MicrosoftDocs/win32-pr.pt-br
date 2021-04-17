---
description: Um IME implementa um recurso chamado &\# 0034; reconversão&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Usando a reconversão com um IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768590"
---
# <a name="using-reconversion-with-an-ime"></a>Usando a reconversão com um IME

Um IME implementa um recurso chamado "reconversão". Normalmente, o IMM determina as listas de candidatos com base apenas nas entradas digitadas pelo usuário. A reconversão permite que o IMM determine um ou mais candidatos com base na frase que a contém (o contexto). Os tipos de reconversão definidos são simples, normais e aprimorados.

A reconversão é útil quando um usuário observa um erro de composição em um documento. O usuário pode selecionar o erro e escolher reconversão em um menu. O IME usa o contexto para determinar a melhor substituição. O aplicativo pode usar [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) para dar suporte à reconversão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Gerenciador de métodos de entrada](using-input-method-manager.md)
</dt> </dl>

 

 



