---
description: Os aplicativos podem declarar o isolamento do driver de impressora no manifesto do aplicativo para isolar o aplicativo do driver de impressora e melhorar a confiabilidade dos aplicativos.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: Como usar o isolamento do aplicativo
ms.date: 05/31/2018
ms.openlocfilehash: 818ba30e7b294c695b2f67bb9bccc485959db43818bb95aedaa67cafc26d3559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233826"
---
# <a name="how-to-use-application-isolation"></a>Como usar o isolamento do aplicativo

Os aplicativos podem declarar o isolamento do driver de impressora no manifesto do aplicativo para isolar o aplicativo do driver de impressora e melhorar a confiabilidade do aplicativo. O Windows de impressão permite que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado. O uso desse recurso impede que o aplicativo falha caso o driver de impressora tenha um erro.

O isolamento do driver de impressora é implementado no Windows 7 e Windows Server 2008 R2.

### <a name="prerequisites"></a>Pré-requisitos

-   Um código gerenciado ou um Windows Store que usa Windows impressão.

## <a name="instructions"></a>Instruções

### <a name="update-the-app-manifest"></a>Atualizar o manifesto do aplicativo

A habilitação do isolamento do driver de impressora exige que você adicione o **elemento printerDriverIsolation** ao manifesto do aplicativo. Aqui está como:

1.  Edite o manifesto do aplicativo, adicionando o elemento  **printerDriverIsolation** com um valor true ao elemento **windowsSettings** do elemento **application,** conforme mostrado neste exemplo.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Recomar seu aplicativo.

 

 



