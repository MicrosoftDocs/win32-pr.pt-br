---
title: Recuperando informações de erro
description: Recuperando informações de erro
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e26844505b7c5de3e39c3199a6087c94f35bed9f64ef11a65d1c6df9a3dd4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309648"
---
# <a name="retrieving-error-information"></a>Recuperando informações de erro

Usando as interfaces e funções de tratamento de erros COM, você pode recuperar informações de erro da seguinte maneira:

1.  Verifique se o valor retornado representa um erro que o objeto está preparado para manipular.
2.  Chame [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter um ponteiro para a interface [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) . Em seguida, chame [**ISupportErrorInfo:: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) para verificar se o erro foi gerado pelo objeto que o retornou e se o objeto de erro pertence ao erro atual e não a uma chamada anterior.
3.  Para obter um ponteiro para o objeto Error, chame a função [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .
4.  Para recuperar informações do objeto de erro, use os métodos [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .

Se o objeto não estiver preparado para lidar com o erro, mas precisar propagar as informações de erro mais adiante na cadeia de chamadas, ele deverá simplesmente passar o valor de retorno para seu chamador. Como a função [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) limpa as informações de erro e passa a propriedade do objeto de erro para o chamador, a função deve ser chamada somente pelo objeto que manipula o erro.

 

 