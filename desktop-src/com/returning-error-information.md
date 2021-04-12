---
title: Retornando informações de erro
description: Retornando informações de erro
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366739"
---
# <a name="returning-error-information"></a>Retornando informações de erro

Usando as interfaces e funções de tratamento de erros COM, você pode retornar informações de erro executando as seguintes etapas:

1.  Implemente a interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .
2.  Para criar uma instância do objeto de erro genérico, chame a função [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .
3.  Para definir seu conteúdo, use os métodos [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .
4.  Para associar o objeto de erro ao thread lógico atual, chame a função [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .

As interfaces de tratamento de erros criam e gerenciam um objeto de erro, que fornece informações sobre o erro. O objeto de erro não é o mesmo que o objeto que encontrou o erro. É um objeto separado associado ao thread atual de execução.

 

 