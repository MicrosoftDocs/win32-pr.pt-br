---
title: Novos recursos no TSF
description: Com o lançamento do Microsoft WindowsXP Service Pack1, a TSF (estrutura de serviços de texto) tem vários recursos novos.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- TSF (estrutura de serviços de texto), novos recursos
- TSF (estrutura de serviços de texto), novos recursos
- serviços de texto, novos recursos
- Aplicativos habilitados para TSF, novos recursos
- TSF (estrutura de serviços de texto), suporte avançado
- TSF (estrutura de serviços de texto), suporte avançado
- serviços de texto, suporte avançado
- Aplicativos habilitados para TSF, suporte avançado
- TSF (estrutura de serviços de texto), edição avançada
- TSF (estrutura de serviços de texto), edição avançada
- serviços de texto, edição avançada
- Aplicativos habilitados para TSF, edição avançada
- Edição avançada
- TSF (estrutura de serviços de texto), segurança
- TSF (estrutura de serviços de texto), segurança
- serviços de texto, segurança
- Aplicativos habilitados para TSF, segurança
- segurança para TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366106"
---
# <a name="new-features-in-tsf"></a>Novos recursos no TSF

Com o lançamento do Microsoft WindowsXP Service Pack1, a TSF (estrutura de serviços de texto) tem vários recursos novos.

## <a name="extended-support-of-advanced-text-services"></a>Suporte estendido de serviços de texto avançados

O suporte foi adicionado ao TSF e ao Windows para fornecer uma interface de usuário consistente para todos os aplicativos na área de trabalho. Esse novo suporte permite que os aplicativos herdados ou controles que não reconheçam o TSF aproveitem alguns serviços de texto avançados gratuitamente. Por exemplo, o ditado de fala e o manuscrito agora podem ser usados para inserir texto em um documento em qualquer aplicativo.

Esse novo recurso está disponível apenas para o WindowsXP Service Pack1 ou posterior. Ela é desativada por padrão. Para habilitá-lo, clique na caixa de seleção na nova guia **avançado** na parte de **serviços de texto e idiomas de entrada** do painel de controle **Opções regionais e de idiomas** .

![suporte a aplicativos sem reconhecimento no painel de controle do TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Suporte para edição avançada

[Edição avançada do Microsoft®](../controls/rich-edit-controls.md) A versão 4,1, usada por aplicativos para exibir e editar texto com caracteres especiais e formatação de parágrafo, agora expõe a funcionalidade TSF. Por padrão, esse suporte é desativado. Para habilitar o TSF no Rich Edit, um aplicativo de hospedagem envia uma mensagem de janela especial para o controle de edição rico.

## <a name="security-improvements"></a>Aprimoramentos de segurança

A segurança e a robustez do TSF foram substancialmente aperfeiçoadas, para reduzir a probabilidade de um programa hostil ser capaz de acessar a pilha, heap ou outros locais de memória segura. A segurança dos aplicativos de exemplo do SDK (Software Development Kit) e dos serviços de texto também foi aprimorada.

 

 