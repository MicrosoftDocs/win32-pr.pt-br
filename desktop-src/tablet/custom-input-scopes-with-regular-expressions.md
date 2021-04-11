---
description: Você pode definir escopos de entrada personalizados usando modelos de linguagem compostos por expressões regulares para manuscrito e atribuindo-os a campos. Por exemplo, se você estiver criando um aplicativo de banco de dados para partes de depósito e quiser que os usuários possam inserir números de peça usando o painel de escrita do Tablet PC. Se a sintaxe do número da peça consistir em três letras seguidas por quatro números seguidos por outra letra (por exemplo, ABC1234D), o reconhecedor de manuscrito teria um tempo difícil de reconhecer essa entrada porque não está definido no modelo de linguagem. Não há nenhum factor predefinido que corresponda a tal sintaxe, nem a Microsoft pode incluir a sintaxe de todos os campos possíveis que um aplicativo possa precisar. As expressões regulares de manuscrito fornecem uma maneira fácil para que os aplicativos definam seu próprio modelo de linguagem para um campo de uso especial específico. Observação ao trabalhar em um aplicativo habilitado para tinta que usa a propriedade facto do objeto RecognizerContext, você não pode usar as da versão 1 em uma expressão regular.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Escopos de entrada personalizados com expressões regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010298"
---
# <a name="custom-input-scopes-with-regular-expressions"></a>Escopos de entrada personalizados com expressões regulares

Você pode definir escopos de entrada personalizados usando modelos de linguagem compostos por expressões regulares para manuscrito e atribuindo-os a campos.

Por exemplo, se você estiver criando um aplicativo de banco de dados para partes de depósito e quiser que os usuários possam inserir números de peça usando o painel de escrita do Tablet PC. Se a sintaxe do número da peça consistir em três letras seguidas por quatro números seguidos por outra letra (por exemplo, ABC1234D), o reconhecedor de manuscrito teria um tempo difícil de reconhecer essa entrada porque não está definido no modelo de linguagem. Não há nenhum factor predefinido que corresponda a tal sintaxe, nem a Microsoft pode incluir a sintaxe de todos os campos possíveis que um aplicativo possa precisar. As expressões regulares de manuscrito fornecem uma maneira fácil para que os aplicativos definam seu próprio modelo de linguagem para um campo de uso especial específico.

> [!Note]  
> Ao trabalhar em um aplicativo habilitado para tinta que usa a propriedade [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) , você não pode usar o factos de versão 1 em uma expressão regular.

 

 

 



