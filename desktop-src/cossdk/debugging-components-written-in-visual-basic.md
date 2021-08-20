---
description: Componentes de depuração escritos em Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Componentes de depuração escritos em Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0dc8e4d98a41f0059de8e3eb44deeb9dcd8e4fbfdc6dba0510bd227a189c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991173"
---
# <a name="debugging-components-written-in-visual-basic"></a>Componentes de depuração escritos em Visual Basic

você pode usar o ambiente de desenvolvimento Microsoft Visual Basic 6,0 para depuração em determinados cenários. o uso de Visual Basic para depuração permite o acesso a ferramentas familiares para Visual Basic programadores. por outro lado, como durante a depuração Visual Basic os componentes são executados dentro do processo do ambiente de Visual Basic, pode ser necessário depurar seu componente depois que ele tiver sido compilado usando o ambiente de desenvolvimento do Microsoft Visual C++.

para obter mais informações sobre a depuração dentro do Visual Basic ide (ambiente de desenvolvimento integrado), consulte [debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md). para saber mais sobre como depurar Visual Basic componentes depois que eles forem compilados usando o ambiente de desenvolvimento de Visual C++, consulte [depurando componentes de Visual Basic compilados](debugging-compiled-visual-basic-components.md).

além disso, várias limitações associadas ao uso do ambiente de Visual Basic para depurar componentes com o MTS foram resolvidas para COM+. para obter mais informações, consulte [suporte à depuração de Visual Basic COM+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> se você já tiver usado Visual Basic no mesmo computador que o COM+, talvez tenha notado o suplemento serviços de componentes disponível no ambiente de Visual Basic. Originalmente no MTS, esse recurso foi projetado para atualizar o registro cada vez que você recompilou um componente em um aplicativo COM+. no entanto, considerando a natureza da interação do registro do Microsoft Windows e do banco de dados de registro do COM+, algumas configurações podem não ser completamente atualizadas. Portanto, em vez de usar os comandos disponíveis com esse suplemento, você deve remover e reinstalar os componentes para atualizar as configurações após a recompilação.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes de depuração escritos em Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



