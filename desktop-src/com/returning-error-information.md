---
title: Retornando informações de erro
description: Retornando informações de erro
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 545c697be7da64362ecce0f5b4c45272832ad682d8b4dd0eb5234620b993e5f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309638"
---
# <a name="returning-error-information"></a>Retornando informações de erro

Usando as interfaces e funções de tratamento de erros COM, você pode retornar informações de erro executando as seguintes etapas:

1.  Implemente a interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .
2.  Para criar uma instância do objeto de erro genérico, chame a função [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .
3.  Para definir seu conteúdo, use os métodos [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .
4.  Para associar o objeto de erro ao thread lógico atual, chame a função [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .

As interfaces de tratamento de erros criam e gerenciam um objeto de erro, que fornece informações sobre o erro. O objeto de erro não é o mesmo que o objeto que encontrou o erro. É um objeto separado associado ao thread atual de execução.

 

 