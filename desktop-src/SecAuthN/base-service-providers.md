---
description: Esses provedores de serviços fornecem os recursos básicos do cartão inteligente.
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: Provedores de serviço base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07fab7f7406b4932ed5c08ab2c8743f8ebde57893aed4564f8fdf40758b5af4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883566"
---
# <a name="base-service-providers"></a>Provedores de serviço base

Esses [*provedores de serviços*](/windows/desktop/SecGloss/c-gly) fornecem os recursos básicos do [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) . Eles podem ser usados para acessar um único recurso de cartão inteligente, ou suas interfaces COM podem ser combinadas para fornecer vários recursos dentro de um único provedor de serviços. Esses provedores de serviços são os blocos de construção para o desenvolvimento de funcionalidades adicionais para outros provedores de serviços.

As seguintes tarefas podem ser executadas por interfaces de provedor de serviço base fornecidas pelo SDK do cartão inteligente.



| Tarefa                                                                                                                   | Interfaces de provedor de serviço base         | DLL      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| Conexão a um cartão inteligente, implemente transações, feche as conexões e assim por diante.                                         | [**Iscard**](iscard.md)                 | SCardSSP |
| Mantenha um comando APDU e [*responda APDU*](/windows/desktop/SecGloss/r-gly).          | [**ISCardCmd**](iscardcmd.md)           | SCardSSP |
| Consulte o [*banco de dados do cartão inteligente*](/windows/desktop/SecGloss/s-gly). | [**ISCardDatabase**](iscarddatabase.md) | SCardSSP |
| Localize um cartão inteligente ou leitor.                                                                                         | [**ISCardLocate**](iscardlocate.md)     | SCardSSP |
| Crie um APDU de comando ISO7816-4.                                                                                       | [**ISCardISO7816**](iscardiso7816.md)   | SCardSSP |
| encapsular um buffer de Istream usando tipos compatíveis com Visual Basic.                                                         | [**IByteBuffer**](ibytebuffer.md)       | SCardSSP |



 

O procedimento a seguir mostra um uso típico dessas interfaces de provedor de serviço base. Neste exemplo, as interfaces [**iscard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md) são usadas para executar uma transação.

**Para executar uma transação**

1.  Crie uma instância para todas as interfaces de provedor de serviço base necessárias (por exemplo, [**iscard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md)e [**ISCardCmd**](iscardcmd.md)).
2.  Conexão a um cartão inteligente específico usando os métodos na interface [**iscard**](iscard.md) .
3.  Usando [**ISCardISO7816**](iscardiso7816.md) e um objeto [**ISCardCmd**](iscardcmd.md) , crie um comando ISO 7816-4 chamando o método **ISCardISO7816** . O comando está contido em **ISCardCmd** como o comando APDU.
4.  Faça uma transação com o cartão chamando o método [**iscard**](iscard.md) transação e passando o objeto [**ISCardCmd**](iscardcmd.md) criado. Quando a transação for concluída, os resultados serão armazenados no APDU de resposta **ISCardCmd** .
5.  Interprete o APDU de resposta [**ISCardCmd**](iscardcmd.md) e repita.
6.  Libere todas as interfaces quando as operações forem concluídas.

Para obter informações sobre o comando APDU criado dentro das DLLs, consulte [criando um comando ISO7816-4 APDU](building-an-iso7816-4-apdu-command.md).

 

 
