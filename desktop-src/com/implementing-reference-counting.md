---
title: Implementando a contagem de referência
description: Implementando a contagem de referência
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa2a3e9827d35d07fa88b62c6f1097fcb3ad3ae3b5b75764deeac1c9c271050
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048154"
---
# <a name="implementing-reference-counting"></a>Implementando a contagem de referência

A contagem de referência requer trabalho por parte do implementador de uma classe e dos clientes que usam objetos dessa classe. Ao implementar uma classe, você deve implementar os métodos [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) como parte da interface [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Esses dois métodos têm as seguintes implementações simples:

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa a contagem de referência interna do objeto.
-   [**A**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) versão primeiro diminui a contagem de referência interna do objeto e, em seguida, verifica se a contagem de referência diminuiu para zero. Se tiver, isso significa que ninguém está mais usando o objeto, portanto, a **função Release** desaloca o objeto.

Uma abordagem de implementação comum para a maioria dos objetos é ter apenas uma implementação desses métodos (juntamente com [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), que é compartilhada entre todas as interfaces e, portanto, uma contagem de referência que se aplica a todo o objeto. No entanto, da perspectiva de um cliente, a contagem de referência é estritamente e claramente uma noção por ponteiro por interface e, portanto, objetos que aproveitam essa funcionalidade construindo, destrói, carregando ou descarregando partes de sua funcionalidade com base nos ponteiros de interface existentes no momento podem ser implementados. Elas são chamadas de *interfaces de replicação.*

Sempre que um cliente chama um método (ou função de API), como [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), que retorna um novo ponteiro de interface, o método que está sendo chamado é responsável por incrementar a contagem de referência por meio do ponteiro retornado. Por exemplo, quando um cliente cria um objeto pela primeira vez, ele recebe um ponteiro de interface para um objeto que, do ponto de vista do cliente, tem uma contagem de referência de um. Se o cliente chamar [**AddRef no**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ponteiro de interface, a contagem de referência se tornará duas. O cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) duas vezes no ponteiro de interface para soltar todas as suas referências ao objeto .

Um exemplo de como as contagens de referência são estritamente por ponteiro de interface ocorre quando um cliente chama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) no primeiro ponteiro para uma nova interface ou a mesma interface. Em qualquer um desses casos, o cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) uma vez para cada ponteiro. O COM não exige que um objeto retorne o mesmo ponteiro quando solicitado a usar a mesma interface várias vezes. (A única exceção a isso é uma consulta a [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que identifica um objeto para COM.) Isso permite que a implementação do objeto gerencie recursos com eficiência.

O thread-safety também é um problema importante na implementação de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para obter mais informações, [consulte Processos, threads e apartments.](processes--threads--and-apartments.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando os tempos de vida do objeto por meio da contagem de referência](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 