---
description: Habilitando a ativação JIT para um componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Habilitando a ativação JIT para um componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beac51cd4f97a451b372d8eeee8ef419ead3140a672ca85dcdc3740d8c52de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637696"
---
# <a name="enabling-jit-activation-for-a-component"></a>Habilitando a ativação JIT para um componente

Você deve configurar um componente para ser ativado por JIT somente quando ele for gravado corretamente para dar suporte ao serviço de ativação JIT (just-in-time) do COM+. Se um componente for desativado entre chamadas de método, ele perderá qualquer estado associado. Devido ao comportamento padrão da ativação JIT, é improvável que isso ocorra quando você não espera, mas deve estar ciente dos requisitos de um componente antes de alterar sua configuração e das expectativas dos clientes que chamarão o componente.

> [!Note]  
> Se um componente estiver configurado para exigir transações, o serviço de ativação JIT do COM+ será habilitado automaticamente. Você não pode desabilitá-lo nesse caso. Para obter mais detalhes, consulte [Configurando transações](configuring-transactions.md).

 

Quando você habilita a ativação JIT para um componente, seu atributo de sincronização é definido como obrigatório para esse componente. Nesse caso, você não pode alterar a configuração de sincronização. Para obter mais detalhes, consulte [dependências de sincronização](synchronization-dependencies.md).

**Para habilitar a ativação JIT**

1.  No painel de detalhes da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no componente que você deseja configurar e clique em **Propriedades**.

2.  Na caixa de diálogo Propriedades do componente, clique na guia **ativação** .

3.  Para habilitar a ativação JIT para o componente, marque a caixa de seleção **habilitar ativação Just in time** .

4.  Clique em **OK**.

Quando você tiver habilitado a ativação JIT para um componente, terá a opção de habilitar o recurso auto-pronto para qualquer método exposto por esse componente. Consulte [habilitando auto-pronto para um método](enabling-auto-done-for-a-method.md) para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Habilitando o auto-pronto para um método](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Definindo o bit concluído](setting-the-done-bit.md)
</dt> </dl>

 

 



