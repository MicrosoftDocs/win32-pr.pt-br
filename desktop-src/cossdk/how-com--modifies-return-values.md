---
description: Como o COM+ modifica valores de retorno
ms.assetid: a6997f02-8456-45b5-9f40-4b9094ee4626
title: Como o COM+ modifica valores de retorno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa8270e41f1a1a96df0c17ccc1b98530fba4347
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089313"
---
# <a name="how-com-modifies-return-values"></a>Como o COM+ modifica valores de retorno

COM+ nunca altera o valor de retorno de um **HRESULT** que indica falha, como e \_ inesperado ou \_ falha. No entanto, quando um objeto que usa a funcionalidade COM+ retorna um valor **HRESULT** que indica êxito (como s \_ OK, s \_ false ou NOERROR), o com+ às vezes converte o **HRESULT** em um código de erro com+ antes que ele retorne ao chamador.

Por exemplo, quando um aplicativo retorna S \_ OK após chamar [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), se o objeto for a raiz de uma transação que não é confirmada, o **HRESULT** será convertido em Context \_ E \_ abortado.

Quando o COM+ converte um valor **HRESULT** , ele limpa todos os parâmetros de saída do método. As referências retornadas são liberadas e os valores dos ponteiros de objeto retornados são definidos como **NULL**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Política de FailFast e isolamento de falhas](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Localizando a origem de um erro](finding-the-source-of-an-error.md)
</dt> <dt>

[Interpretando códigos de erro](interpreting-error-codes.md)
</dt> <dt>

[Estratégias para lidar com erros no COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solução de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



