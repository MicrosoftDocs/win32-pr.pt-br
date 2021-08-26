---
description: Visão geral do log de erros
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Visão geral do log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcde3e0366ffca12dfcb5674259273ba1bbf25c1feed9be3ead57fa64cc42dc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904626"
---
# <a name="overview-of-error-logging"></a>Visão geral do log de erros

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Para dar aos aplicativos máxima flexibilidade no tratamento de erros, [DirectShow Serviços de](directshow-editing-services.md) Edição usa um mecanismo de retorno de chamada. Seu aplicativo implementa um método para registrar um erro em log. Em tempo de operação, se ocorrer um erro, o DES chamará o método que você forneceu. O método aceita parâmetros que descrevem o erro. O que o método faz com essas informações é de sua responsabilidade. (No entanto, ele deve retornar o mais rápido possível ou pode interferir na execução do programa.)

O método de retorno de chamada de log de erros está contido em uma interface COM, [**IAMErrorLog.**](iamerrorlog.md) Seu aplicativo deve implementar essa interface. Como todas as interfaces COM, **IAMErrorLog** herda a interface **IUnknown,** portanto, seu aplicativo também deve implementá-lo.

Você tem várias opções para implementar essas interfaces COM. Você pode usar o Active Template Library (ATL), que fornece implementações de estoque dos **métodos IUnknown.** DirectShow também fornece uma classe base C++, [**CUnknown**](cunknown.md), que facilita a implementação de uma interface COM. Para obter informações sobre **como usar CUnknown**, [consulte How to Implement IUnknown](how-to-implement-iunknown.md).

O código de exemplo neste artigo define uma classe C++ independente, que implementa **IUnknown** e **IAMErrorLog**. O resultado não é um objeto COM verdadeiro, porque não dá suporte a **CoCreateInstance**. No entanto, essa abordagem é adequada para a finalidade do exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de registro em log](logging-errors.md)
</dt> </dl>

 

 



