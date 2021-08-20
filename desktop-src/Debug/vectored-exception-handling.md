---
description: Os manipuladores de exceção em vetor são uma extensão da manipulação de exceção estruturada.
ms.assetid: e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef
title: Manipulação de exceção em vetor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926b0499e9399aa77e6835e90c6da016da3f2dc8195a4b4872f7f5119d04978a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405577"
---
# <a name="vectored-exception-handling"></a>Manipulação de exceção em vetor

Os manipuladores de exceção em vetor são uma extensão da manipulação de exceção estruturada. Um aplicativo pode registrar uma função para inspecionar ou manipular todas as exceções para o aplicativo. Os manipuladores vetoriais não são baseados em quadros, portanto, você pode adicionar um manipulador que será chamado independentemente de onde você estiver em um quadro de chamada. Os manipuladores vetoriais são chamados na ordem em que foram adicionados, depois que o depurador obtém uma notificação de primeira chance, mas antes de o sistema começar a desenrolar a pilha.

Para adicionar um manipulador de continuação em vetor, use a função [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler) . Para remover esse manipulador, use a função [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler) .

Para adicionar um manipulador de exceção em vetor, use a função [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler) . Para remover esse manipulador, use a função [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler) .

 

 
