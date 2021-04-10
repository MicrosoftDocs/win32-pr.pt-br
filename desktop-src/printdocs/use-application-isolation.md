---
description: Os aplicativos podem declarar o isolamento de driver de impressora em seu manifesto de aplicativo para isolar o aplicativo do driver de impressora e melhorar a confiabilidade dos aplicativos.
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 'Como: usar o isolamento de aplicativos'
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169453"
---
# <a name="how-to-use-application-isolation"></a>Como: usar o isolamento de aplicativos

Os aplicativos podem declarar o isolamento de driver de impressora em seu manifesto de aplicativo para isolar o aplicativo do driver de impressora e melhorar a confiabilidade do aplicativo. O serviço de impressão do Windows permite que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado. Usando esse recurso, seu aplicativo impede que ele falhe em caso de erro do driver de impressora.

O isolamento do driver de impressora é implementado no Windows 7 e no Windows Server 2008 R2.

### <a name="prerequisites"></a>Pré-requisitos

-   Um aplicativo de código gerenciado ou da Windows Store que usa a impressão do Windows.

## <a name="instructions"></a>Instruções

### <a name="update-the-app-manifest"></a>Atualizar o manifesto do aplicativo

Habilitar o isolamento de driver de impressora exige que você adicione o elemento **printerDriverIsolation** ao manifesto do aplicativo. Aqui está como:

1.  Edite o manifesto do aplicativo, adicionando o elemento **printerDriverIsolation** com um valor de **true** para o elemento **windowsSettings** do elemento **Application** , conforme mostrado neste exemplo.
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  Recompile seu aplicativo.

 

 



