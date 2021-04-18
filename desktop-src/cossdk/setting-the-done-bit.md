---
description: Definindo o bit concluído
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: Definindo o bit concluído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a53368377016c88633d91d942cde1970d979563
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797624"
---
# <a name="setting-the-done-bit"></a>Definindo o bit concluído

O COM+ desativará um objeto ativado por JIT com base no status de uma propriedade de contexto, o bit feito, da seguinte maneira:

-   Quando o bit Done é definido como true, o COM+ desativa o objeto quando a chamada do método atual retorna.
-   Quando o bit Done é definido como false, o objeto permanece ativo quando a chamada do método atual retorna.

Por padrão, o bit Done é definido como false quando um objeto é criado e seu contexto é inicializado. (Qualquer objeto ativado por JIT é criado em seu próprio contexto para que ele tenha seu próprio bit feito para ser definido.) No entanto, você pode alterar essa configuração padrão de acordo com cada método usando a propriedade auto-done. Você pode definir o bit concluído das seguintes maneiras:

-   Usando [ **IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   Usando [ **IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   Usando a propriedade auto-Done

## <a name="using-icontextstate"></a>Usando IContextState

Você pode usar [**IContextState:: SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) para definir o bit Done como true ou false.

Você pode usar [**IContextState:: GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) para obter o status atual do bit realizado do contexto do objeto.

## <a name="using-iobjectcontext"></a>Usando IObjectContext

Você pode usar os seguintes métodos em [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) para definir o bit realizado enquanto define simultaneamente o bit consistente usado para votação em transações:

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) sinaliza que você concluiu e que votará para confirmar a transação atual. Ele define o bit Done e o bit consistente como true.
-   Os sinais [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) que você concluiu e Dooms a transação atual. Ele define o bit Done como true e o bit consistente como false.
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) sinaliza que você não está pronto, mas que você votará para confirmar a transação. Ele define o bit Done como false e o bit consistente como true.
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) sinaliza que você não está pronto e que vote em não confirmar a transação no momento, geralmente porque o estado é inconsistente. Ele define o bit Done e o bit consistente como false.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Pooling de objetos e ativação JIT do COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transações e ativação JIT do COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



