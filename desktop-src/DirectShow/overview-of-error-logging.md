---
description: Visão geral do log de erros
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Visão geral do log de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087555"
---
# <a name="overview-of-error-logging"></a>Visão geral do log de erros

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Para dar aos aplicativos flexibilidade máxima no tratamento de erros, os [serviços de edição do DirectShow](directshow-editing-services.md) usam um mecanismo de retorno de chamada. Seu aplicativo implementa um método para registrar um erro. Em tempo de execução, se ocorrer um erro, o DES chamará o método que você forneceu. O método usa parâmetros que descrevem o erro. O que o método faz com essas informações cabe a você. (No entanto, ele deve retornar o mais rápido possível, ou pode interferir na execução do programa.)

O método de retorno de chamada de log de erros está contido em uma interface COM, [**IAMErrorLog**](iamerrorlog.md). Seu aplicativo deve implementar essa interface. Como todas as interfaces COM, **IAMErrorLog** herda a interface **IUnknown** , de modo que seu aplicativo também deve implementá-la.

Você tem várias opções para implementar essas interfaces COM. Você pode usar o Active Template Library (ATL), que fornece implementações de estoque dos métodos **IUnknown** . O DirectShow também fornece uma classe base do C++, [**CUnknown**](cunknown.md), que facilita a implementação de uma interface com. Para obter informações sobre como usar o **CUnknown**, consulte [como implementar IUnknown](how-to-implement-iunknown.md).

O código de exemplo neste artigo define uma classe C++ independente, que implementa **IUnknown** e **IAMErrorLog**. O resultado não é um objeto COM verdadeiro, porque ele não dá suporte a **CoCreateInstance**. No entanto, essa abordagem é adequada para a finalidade do exemplo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Erros de log](logging-errors.md)
</dt> </dl>

 

 



