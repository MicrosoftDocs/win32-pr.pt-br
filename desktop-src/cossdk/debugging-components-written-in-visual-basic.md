---
description: Componentes de depuração escritos em Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Componentes de depuração escritos em Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773027"
---
# <a name="debugging-components-written-in-visual-basic"></a>Componentes de depuração escritos em Visual Basic

Você pode usar o ambiente de desenvolvimento Microsoft Visual Basic 6,0 para depuração em determinados cenários. O uso de Visual Basic para depuração permite o acesso a ferramentas familiares para Visual Basic programadores. Por outro lado, como durante a depuração Visual Basic os componentes são executados dentro do processo do ambiente de Visual Basic, pode ser necessário depurar seu componente depois que ele tiver sido compilado usando o ambiente de desenvolvimento do Microsoft Visual C++.

Para obter mais informações sobre a depuração dentro do Visual Basic IDE (ambiente de desenvolvimento integrado), consulte [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md). Para saber mais sobre como depurar Visual Basic componentes depois que eles forem compilados usando o ambiente de desenvolvimento de Visual C++, consulte [Depurando componentes de Visual Basic compilados](debugging-compiled-visual-basic-components.md).

Além disso, várias limitações associadas ao uso do ambiente de Visual Basic para depurar componentes com o MTS foram resolvidas para COM+. Para obter mais informações, consulte [suporte à depuração de Visual Basic com+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

> [!Note]  
> Se você já tiver usado Visual Basic no mesmo computador que o COM+, talvez tenha notado o suplemento serviços de componentes disponível no ambiente de Visual Basic. Originalmente no MTS, esse recurso foi projetado para atualizar o registro cada vez que você recompilou um componente em um aplicativo COM+. No entanto, considerando a natureza da interação do registro do Microsoft Windows e do banco de dados de registro do COM+, algumas configurações podem não ser completamente atualizadas. Portanto, em vez de usar os comandos disponíveis com esse suplemento, você deve remover e reinstalar os componentes para atualizar as configurações após a recompilação.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Componentes de depuração escritos em Visual C++](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



