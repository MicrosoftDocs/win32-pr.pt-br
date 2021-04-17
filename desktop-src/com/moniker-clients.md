---
title: Clientes de moniker
description: Os clientes do moniker devem começar obtendo um moniker e há várias maneiras para um cliente moniker obter um moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761841"
---
# <a name="moniker-clients"></a>Clientes de moniker

Os clientes do moniker devem começar obtendo um moniker e há várias maneiras para um cliente moniker obter um moniker. Por exemplo, em documentos compostos OLE, quando o usuário final cria um item vinculado (usando a caixa de diálogo **Inserir objeto** , a área de transferência ou arrasta e solta), um moniker é inserido como parte do item vinculado. Nesse caso, o programador tem um mínimo de contato com os monikers. Programaticamente, se você tiver um ponteiro de interface para um objeto que implementa a interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , poderá usá-lo para obter um moniker, e existem métodos em outras interfaces que são definidas para retornar moniker.

Há diferentes tipos de monikers, que são usados para identificar diferentes tipos de objetos, mas para um cliente moniker, todos os monikeres têm a mesma aparência. Um cliente moniker simplesmente chama [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) em um moniker e Obtém um ponteiro de interface para o objeto que o moniker identifica. Se o moniker identificar um objeto tão grande quanto uma planilha inteira ou tão pequeno quanto uma única célula dentro de uma planilha, chamar **BindToObject** retornará um ponteiro para esse objeto. Se o objeto já estiver em execução, o **BindToObject** irá encontrá-lo na memória. Se o objeto for armazenado de forma passiva no disco, o **BindToObject** localizará um servidor para esse objeto, executará o servidor e fará com que o servidor Coloque o objeto no estado de execução. Todos os detalhes do processo de associação estão ocultos do cliente moniker. Portanto, para um cliente moniker, o uso do moniker é muito simples.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Provedores de moniker](moniker-providers.md)
</dt> <dt>

[Implementações de moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




