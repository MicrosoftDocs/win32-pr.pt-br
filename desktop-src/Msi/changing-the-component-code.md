---
description: Ao especificar os componentes para uma instalação, os autores de pacote devem seguir as regras gerais da organização do componente descritas em Organizando aplicativos em componentes.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Alterando o código do componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96217dbcdbdc63d444f95d73dec657cf1a5ddef4ed80128c85b7752e1ec0f0d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520196"
---
# <a name="changing-the-component-code"></a>Alterando o código do componente

Ao especificar os [componentes para](windows-installer-components.md) uma instalação, os autores de pacote devem seguir as regras gerais da organização do componente descritas em Organizando aplicativos [em componentes](organizing-applications-into-components.md). Talvez os autores precisem introduzir novos componentes ou modificar componentes existentes. Se a adição, remoção ou modificação de recursos criar efetivamente um novo componente, o código do componente também deverá ser alterado.

## <a name="creating-a-new-component"></a>Criando um novo componente

Introduza um novo componente e atribua a ele um código de componente exclusivo ao fazer qualquer uma das seguintes alterações:

-   Qualquer alteração que não tenha sido mostrada pelo teste para ser compatível com versões anteriores do componente. Nesse caso, você também deve alterar o nome ou o local de destino de cada recurso no componente.
-   Uma alteração no nome ou local de destino de qualquer arquivo, chave do Registro, atalho ou outro recurso no componente. Nesse caso, você também deve alterar o nome ou o local de destino de cada recurso no componente.
-   A adição ou remoção de qualquer arquivo, chave do Registro, atalho ou outro recurso do componente. Nesse caso, você também deve alterar o nome ou o local de destino de cada recurso no componente.
-   Recompilar um componente de 32 bits em um componente de 64 bits.

Ao introduzir um novo componente, os autores precisam fazer um dos seguintes para garantir que o componente não entre em conflito com nenhum componente existente:

-   Altere o nome ou o local de destino de qualquer recurso que possa ser instalado sob o mesmo nome e local de destino por outro componente.
-   Caso contrário, garanta que o novo componente nunca seja instalado na mesma pasta que outro componente que tenha um recurso em um nome e local comuns. Isso inclui versões localizadas de arquivos com o mesmo nome de arquivo. Para obter mais informações, consulte [O que acontece se as regras de componente são interrompidas?](what-happens-if-the-component-rules-are-broken.md).
-   Ao alterar o código do componente de um componente existente, também altere o nome ou o local de destino de cada arquivo, chave do Registro, atalho e outros recursos no componente.

### <a name="creating-a-new-version-of-a-component"></a>Criando uma nova versão de um componente

Uma nova versão de um componente recebe o mesmo código de componente que outro componente existente. Modificar um componente sem alterar o código do componente só é opcional nos seguintes casos:

-   As alterações no componente foram comprovadas pelo teste como compatíveis com versões anteriores com todas as versões anteriores do componente.
-   O autor pode garantir que a nova versão do componente nunca será instalada em um sistema em que ele entra em conflito com versões anteriores do componente ou aplicativos que exigem uma versão anterior. Para obter mais informações, consulte [O que acontece se as regras de componente são interrompidas?](what-happens-if-the-component-rules-are-broken.md).

O código do componente de uma nova versão de um componente não deve ser alterado quando isso resultaria em dois componentes compartilhando recursos, como valores do Registro, arquivos ou atalhos.

 

 



