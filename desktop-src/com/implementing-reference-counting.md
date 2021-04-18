---
title: Implementando a contagem de referência
description: Implementando a contagem de referência
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d4dfe2b0faf2fc6557d1b089e33ae6ce4b98cb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105815440"
---
# <a name="implementing-reference-counting"></a>Implementando a contagem de referência

A contagem de referência requer trabalho na parte do implementador de uma classe e dos clientes que usam objetos dessa classe. Ao implementar uma classe, você deve implementar os métodos [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) como parte da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Esses dois métodos têm as seguintes implementações simples:

-   O [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa a contagem de referência interna do objeto.
-   A [**versão**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) diminuir primeiro decrementa a contagem de referência interna do objeto e verifica se a contagem de referência caiu para zero. Se tiver, isso significa que ninguém está usando o objeto por mais tempo, portanto, a função de **liberação** desalocará o objeto.

Uma abordagem de implementação comum para a maioria dos objetos é ter apenas uma implementação desses métodos (juntamente com [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))), que é compartilhada entre todas as interfaces e, portanto, uma contagem de referência que se aplica ao objeto inteiro. No entanto, do ponto de vista do cliente, a contagem de referência é estritamente e claramente uma noção de ponteiro por interface e, portanto, os objetos que aproveitam esse recurso criando dinamicamente, destruindo, carregando ou descarregando partes de sua funcionalidade com base nos ponteiros de interface existentes no momento podem ser implementados. Essas são coloquialmente chamadas *de interfaces de divisão*.

Sempre que um cliente chama um método (ou função de API), como [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), que retorna um novo ponteiro de interface, o método que está sendo chamado é responsável por incrementar a contagem de referência por meio do ponteiro retornado. Por exemplo, quando um cliente cria um objeto pela primeira vez, ele recebe um ponteiro de interface para um objeto que, do ponto de vista do cliente, tem uma contagem de referência de um. Se o cliente chamar [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) no ponteiro de interface, a contagem de referência se tornará duas. O cliente deve chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) duas vezes no ponteiro de interface para descartar todas as suas referências ao objeto.

Um exemplo de como as contagens de referência são estritamente por interface – o ponteiro ocorre quando um cliente chama [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) no primeiro ponteiro para uma nova interface ou para a mesma interface. Em qualquer um desses casos, o cliente precisa chamar [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) uma vez para cada ponteiro. COM não exige que um objeto retorne o mesmo ponteiro quando solicitado pela mesma interface várias vezes. (A única exceção a isso é uma consulta para [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que identifica um objeto para com.) Isso permite que a implementação do objeto gerencie recursos com eficiência.

A segurança de threads também é um problema importante na implementação de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para obter mais informações, consulte [processos, threads e Apartments](processes--threads--and-apartments.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciando tempos de vida de objeto por meio de contagem de referência](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 