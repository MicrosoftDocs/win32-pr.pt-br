---
description: Ao especificar os componentes para uma instalação, os autores de pacote devem seguir as regras gerais para a organização de componentes descrita em organizando aplicativos em componentes.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Alterando o código do componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753453"
---
# <a name="changing-the-component-code"></a>Alterando o código do componente

Ao especificar os [componentes](windows-installer-components.md) para uma instalação, os autores de pacote devem seguir as regras gerais para a organização de componentes descrita em [organizando aplicativos em componentes](organizing-applications-into-components.md). Os autores podem precisar introduzir novos componentes ou modificar componentes existentes. Se a adição, remoção ou modificação de recursos efetivamente criar um novo componente, o código do componente também deverá ser alterado.

## <a name="creating-a-new-component"></a>Criando um novo componente

Introduza um novo componente e atribua um código de componente exclusivo ao fazer qualquer uma das seguintes alterações:

-   Qualquer alteração que não tenha sido mostrada pelo teste para ser compatível com as versões anteriores do componente. Nesse caso, você também deve alterar o nome ou o local de destino de cada recurso no componente.
-   Uma alteração no nome ou no local de destino de qualquer arquivo, chave do registro, atalho ou outro recurso no componente. Nesse caso, você também deve alterar o nome ou o local de destino de cada recurso no componente.
-   A adição ou remoção de qualquer arquivo, chave do registro, atalho ou outro recurso do componente. Nesse caso, você também deve alterar o nome ou o local de destino de cada recurso no componente.
-   Recompilando um componente de 32 bits em um componente de 64 bits.

Ao introduzir um novo componente, os autores precisam realizar uma das ações a seguir para garantir que o componente não entre em conflito com os componentes existentes:

-   Altere o nome ou o local de destino de qualquer recurso que possa ser instalado com o mesmo nome e local de destino por outro componente.
-   Caso contrário, garanta que o novo componente nunca seja instalado na mesma pasta que outro componente que tenha um recurso em um nome e local comuns. Isso inclui versões localizadas de arquivos com o mesmo nome de arquivo. Para obter mais informações, consulte [o que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md).
-   Ao alterar o código do componente de um componente existente, altere também o nome ou o local de destino de cada arquivo, chave do registro, atalho e outro recurso no componente.

### <a name="creating-a-new-version-of-a-component"></a>Criando uma nova versão de um componente

Uma nova versão de um componente recebe o mesmo código de componente que outro componente existente. Modificar um componente sem alterar o código do componente só é opcional nos seguintes casos:

-   As alterações no componente foram comprovadas pelo teste para serem compatíveis com versões anteriores do componente.
-   O autor pode garantir que a nova versão do componente nunca seja instalada em um sistema em que estaria em conflito com versões anteriores do componente ou aplicativos que exigem uma versão anterior. Para obter mais informações, consulte [o que acontece se as regras de componente forem interrompidas?](what-happens-if-the-component-rules-are-broken.md).

O código de componente de uma nova versão de um componente não deve ser alterado quando resultaria em dois componentes compartilhando recursos, como valores de registro, arquivos ou atalhos.

 

 



