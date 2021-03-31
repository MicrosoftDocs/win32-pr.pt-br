---
title: Atributos de função
description: Os atributos \ callback \ e \ local \ podem ser aplicados como atributos de função.
ms.assetid: 05e19164-072c-4a5a-878d-845273975854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ef199b937d5a3e9a8444be9ed65749da007ced
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641685"
---
# <a name="function-attributes"></a>Atributos de função

O **\[** [**retorno de chamada**](/windows/desktop/Midl/callback) **\]** e os **\[** atributos [**locais**](/windows/desktop/Midl/local) **\]** podem ser aplicados como atributos de função.

Um callback é uma chamada remota do servidor para o cliente que é executado como parte de um thread de execução única conceitual. Um retorno de chamada é sempre emitido no contexto de uma chamada remota (ou callback) e é executado pelo thread que emitiu a chamada remota original (ou retorno de chamada).

Geralmente, é desejável posicionar uma declaração de procedimento local no arquivo IDL, já que esse é o local lógico para descrever as interfaces para um pacote. O **\[** [](/windows/desktop/Midl/local) **\]** atributo local indica que uma declaração de procedimento não é, na verdade, uma função remota, mas um procedimento local. O compilador MIDL não gera stubs para funções com o atributo **\[ local \]** .

É importante observar que o uso de retorno de **\[** [**chamada**](/windows/desktop/Midl/callback) **\]** não é recomendado na programação de vários threads. Como uma função de programação de thread único, ele não está equipado para dar suporte às demandas de segurança que um ambiente de vários threads fornece.

 

 