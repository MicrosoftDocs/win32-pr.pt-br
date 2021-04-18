---
description: Por padrão, o sistema tem todas as exceções de FP desativadas.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Exceções de ponto flutuante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749658"
---
# <a name="floating-point-exceptions"></a>Exceções de ponto flutuante

Por padrão, o sistema tem todas as exceções de FP desativadas. Portanto, as computações resultam em NAN ou infinito, em vez de uma exceção. Antes de poder interceptar exceções de ponto flutuante (FP) usando manipulação de exceção estruturada, você deve chamar a função de biblioteca de tempo de execução [ \_ controlfp \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C para ativar todas as possíveis exceções de FP. Para interceptar apenas exceções específicas, use apenas os sinalizadores que correspondem às exceções a serem interceptadas. Observe que qualquer manipulador de erros FP deve chamar [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) como sua primeira instrução FP. Essa função limpa as exceções de ponto flutuante.

 

 
