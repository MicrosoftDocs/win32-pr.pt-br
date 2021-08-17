---
title: Novos recursos no TSF
description: Com o lançamento do Microsoft WindowsXP Service Pack1, Estrutura de Serviços de Texto (TSF) tem vários novos recursos.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Estrutura de Serviços de Texto (TSF), novos recursos
- TSF (Estrutura de Serviços de Texto), novos recursos
- serviços de texto, novos recursos
- Aplicativos habilitados para TSF, novos recursos
- Estrutura de Serviços de Texto (TSF), suporte avançado
- TSF (Estrutura de Serviços de Texto), suporte avançado
- serviços de texto, suporte avançado
- Aplicativos habilitados para TSF, suporte avançado
- Estrutura de Serviços de Texto (TSF),Rich Edit
- TSF (Estrutura de Serviços de Texto),Rich Edit
- serviços de texto, Edição rica
- Aplicativos habilitados para TSF, Edição Rica
- Edição rica
- Estrutura de Serviços de Texto (TSF), segurança
- TSF (Estrutura de Serviços de Texto), segurança
- serviços de texto, segurança
- Aplicativos habilitados para TSF, segurança
- segurança para TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73494d4538b25dfa0b004c8691391fb1c572c7ce6d82247cacae4fb9e0a838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952013"
---
# <a name="new-features-in-tsf"></a>Novos recursos no TSF

Com o lançamento do Microsoft WindowsXP Service Pack1, Estrutura de Serviços de Texto (TSF) tem vários novos recursos.

## <a name="extended-support-of-advanced-text-services"></a>Suporte estendido dos Serviços de Texto Avançados

Foi adicionado suporte ao TSF e Windows para fornecer uma interface do usuário consistente para todos os aplicativos na área de trabalho. Esse novo suporte permite que aplicativos herdado ou controles que não estão cientes do TSF aproveitem alguns serviços de texto avançados gratuitamente. Por exemplo, o ditado de fala e o manuscrito agora podem ser usados para inserir texto em um documento em qualquer aplicativo.

Esse novo recurso está disponível somente para WindowsXP Service Pack1 ou posterior. Ele é desligado por padrão. Para habilita-lo, clique  na caixa  de seleção na nova guia Avançado na parte Serviços de Texto e Idiomas de Entrada do painel de controle **Opções** Regionais e de Idioma.

![suporte ao aplicativo sem conhecimento no painel de controle tsf](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Suporte a Edição Rich

[Edição ® Microsoft](../controls/rich-edit-controls.md) A versão 4.1, usada por aplicativos para exibir e editar texto com formatação especial de caractere e parágrafo, agora expõe a funcionalidade TSF. Por padrão, esse suporte é desligado. Para habilitar o TSF no Rich Edit, um aplicativo de hospedagem envia uma mensagem de janela especial para o controle Rich Edit.

## <a name="security-improvements"></a>Aprimoramentos de segurança

A segurança e a robustez do TSF foram substancialmente aprimoradas, para reduzir a probabilidade de um programa invasor poder acessar a pilha, o heap ou outros locais de memória segura. A segurança de aplicativos de exemplo do SDK (Software Development Kit) e dos serviços de texto também foi aprimorada.

 

 