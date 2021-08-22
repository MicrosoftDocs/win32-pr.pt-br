---
title: Tratamento de erros de objeto de serviço
description: Quando ocorre um erro em um objeto de serviço, o valor de retorno para a chamada IDispatch Invoke deve ser DISP \_ e \_ Exception, e o ponteiro do parâmetro pExceptInfo para uma estrutura EXCEPTINFO no deve ser preenchido.
ms.assetid: 1b08c404-69f2-4b0d-9231-c2bd242e124d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c98db4ffdb3c4625ec4c0dfbe3d497ab1cbe4b5152b172c34422c1630ce581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999516"
---
# <a name="service-object-error-handling"></a>Tratamento de erros de objeto de serviço

Quando ocorre um erro em um objeto de serviço, o valor de retorno para a chamada [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) deve ser DISP \_ e \_ Exception, e o ponteiro do parâmetro *pExceptInfo* para uma estrutura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) no deve ser preenchido.

Especificamente, os membros **bstrname** e **BstrDescription** da estrutura [**EXCEPTINFO**](/windows/win32/api/oaidl/ns-oaidl-excepinfo) são usados pelo host do dispositivo com tecnologia UPnP para criar uma resposta de falha de UPnP; **bstrname** é o código de erro e **bstrDescription** é a descrição do erro.

 

 