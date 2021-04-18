---
description: Você pode habilitar o recurso auto-pronto para qualquer método exposto por um componente para o qual a ativação JIT do COM+ esteja habilitada. Se a ativação JIT estiver desabilitada, o auto-pronto não estará disponível.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Habilitando o auto-pronto para um método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771645"
---
# <a name="enabling-auto-done-for-a-method"></a>Habilitando o auto-pronto para um método

Você pode habilitar o recurso auto-pronto para qualquer método exposto por um componente para o qual a ativação JIT do COM+ esteja habilitada. Se a ativação JIT estiver desabilitada, o auto-pronto não estará disponível.

Você deve habilitar o auto-pronto apenas para um método que foi escrito intencionalmente para tirar proveito dele, pois esse recurso pode potencialmente alterar o comportamento esperado do método.

Quando você habilita o auto-pronto, você está alterando o comportamento padrão da ativação JIT e das transações automáticas para esse método. Talvez você queira usar esse recurso porque ele pode remover a necessidade de declarar explicitamente a consistência e a conclusão. Em vez disso, isso pode ser feito simplesmente retornando um HRESULT quando a conclusão automática está habilitada. Essencialmente, ao habilitar o auto-pronto, você está instruindo o COM+ a fazer o seguinte:

-   Defina o bit Done como true por padrão no contexto no qual o objeto é executado sempre que esse método for chamado.
-   Inspecione o HRESULT retornado pelo método; Se ele indicar êxito ou falha, defina o bit de consistência de acordo. Isso pode resultar em uma chamada automática para [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) ou [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), dependendo também do que o método faz internamente.

**Para habilitar o auto-pronto para um método**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no método que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do método, clique na guia **geral** .

3.  Para habilitar o auto-pronto, marque a caixa de seleção **desativar automaticamente este objeto quando este método for retornado** . Se a caixa de seleção não estiver disponível, você deverá primeiro habilitar a ativação JIT para o componente. (Consulte[habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md) para obter instruções detalhadas.)

4.  Clique em **OK**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de ativação Just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitando a ativação JIT para um componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Definindo o bit concluído](setting-the-done-bit.md)
</dt> </dl>

 

 



