---
description: No COM+, cada objeto COM é criado com um contexto associado.
ms.assetid: e5602af2-5852-4c34-a792-6742e90b7d41
title: Ativação de contexto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a652615d6c1288887085c857817e32e3a3b4081c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089371"
---
# <a name="context-activation"></a>Ativação de contexto

No COM+, cada objeto COM é criado com um contexto associado. Isso significa que um novo contexto deve ser criado e inicializado ou um contexto existente apropriado é usado. Esse processo é conhecido como *ativação*. No COM+, um objeto é ativado em seu próprio contexto ou no seu criador (um objeto que solicitou que o objeto fosse ativado — por exemplo, chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)).

Em algumas circunstâncias, como com o [pool de objetos](com--object-pooling.md), um objeto é ativado sem ser criado do zero. Nesse caso, uma instância em execução é ativada dentro de um contexto. Ao longo de seu tempo de vida, ele pode ser ativado repetidamente em diferentes contextos.

O mecanismo básico é o mesmo em ambos os casos — um objeto é associado a um contexto e esse contexto é inicializado corretamente para representar as necessidades de tempo de execução do objeto.

## <a name="flowing-of-context-properties"></a>Fluxo de propriedades de contexto

Quando um objeto está sendo ativado em resposta a uma solicitação de criação de outro objeto, o COM+ precisa se mediar entre eles para ativar corretamente o objeto downstream. O COM+ precisa comparar o contexto do chamador com a configuração do componente chamado e, em seguida, decidir onde ativar o componente downstream e como inicializar suas propriedades de contexto.

Para descobrir a configuração do componente, o COM+ o pesquisa no banco de dados de registro de classe COM+, que é otimizado para pesquisas extremamente rápidas em tempo de execução. (Isso é determinado pela maneira como você configurou um componente ao instalá-lo em um aplicativo COM+.) Em seguida, a configuração do componente é examinada em relação ao estado das propriedades de contexto do chamador.

Em alguns casos, a configuração é consistente com o contexto do chamador e o componente pode ser ativado dentro do contexto do chamador. Isso só poderá ocorrer se o contexto do chamador satisfizer todos os requisitos de tempo de execução do novo objeto.

Quando o componente downstream não pode ser ativado dentro do contexto do chamador, ele é ativado em seu próprio contexto em um apartamento apropriado. Quando isso ocorre, determinadas propriedades de contexto podem fluir do chamador para o receptor. Por exemplo, se o chamador estiver associado a uma transação e o receptor der suporte a transações, o novo objeto obtém seu próprio contexto (para votar na transação, ele precisa ter seu próprio sinalizador consistente) e herda a ID da transação e a ID da atividade do chamador (que residem na mesma transação e no mesmo domínio de sincronização).

## <a name="ignored-context-properties"></a>Propriedades de contexto ignoradas

Dependendo de como um componente é configurado, algumas propriedades de contexto podem não desempenhar nenhuma função para determinar se ele está ativado no contexto do criador ou em seu próprio contexto. Por exemplo, as configurações de transações desabilitadas e de sincronização desabilitadas, indicando a presença de uma transação ou de um domínio de sincronização, não desempenharão nenhuma função, seja na ativação do componente. Essas propriedades são basicamente ignoradas quando o contexto é transmitido. Ou, se um componente usar apenas a verificação de acesso no nível de processo, sua propriedade de contexto de segurança será ignorada — a configuração de segurança do componente nunca desempenhará uma função em sua ativação.

## <a name="forcing-activation-in-the-callers-context"></a>Forçando a ativação no contexto do chamador

Em algumas circunstâncias, talvez você queira que um objeto seja ativado somente no contexto do chamador, ou seja, nunca é ativado em seu próprio contexto. Por exemplo, talvez você queira controlar o comportamento do objeto quando ele é chamado em um limite de contexto.

Você pode garantir que um objeto não possa ser ativado em seu próprio contexto, selecionando a opção de **contexto deve ser ativado em chamadores** na guia **ativação** da página **Propriedades** do componente, usando a ferramenta administrativa serviços de componentes. (Consulte [impondo a ativação no contexto do chamador](enforcing-activation-in-the-caller-s-context.md) para obter instruções passo a passo.) Quando você seleciona essa opção, se o objeto não puder ser ativado no contexto do chamador, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) falhará, retornando co \_ E \_ tentar \_ \_ criar \_ fora do contexto do \_ cliente \_ .

## <a name="default-context"></a>Contexto padrão

Há contextos padrão para dar suporte a componentes não configurados, ou seja, componentes COM não instalados em aplicativos COM+ e não registrados no banco de dados de registro de classe COM+. Se os componentes não configurados tiverem um modelo de Threading compatível, eles serão ativados no contexto do chamador. Caso contrário, eles serão ativados em um contexto padrão no apartamento apropriado. Cada apartamento tem um contexto padrão para dar suporte a objetos COM que não usam serviços COM+.

## <a name="hooking-activation"></a>Conectando a ativação

Ao implementar [**controledeobjetoi:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**controledeobjetoi::D eactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), você pode conectar a ativação e desativação em conjunto para executar a inicialização especial no novo contexto. Esses métodos são chamados pelo COM+ em determinados pontos do ciclo de vida de um objeto, quando o objeto é configurado para usar a ativação JIT ou o pool de objetos. Consulte [ativação Just-in-time com+](com--just-in-time-activation.md) e [pool de objetos com+](com--object-pooling.md) para obter mais detalhes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interceptação de chamadas de contexto cruzado](interception-of-cross-context-calls.md)
</dt> </dl>

 

 
