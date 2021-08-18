---
description: Vsdiagview e Vssagent são ferramentas que você pode usar para solucionar problemas de aplicativos VSS. observe que essas ferramentas estão incluídas no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Usando diagnósticos do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7742bf706da0bb8fdd377960a597a61b6592b772df98982cec500434f66c7579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590799"
---
# <a name="using-vss-diagnostics"></a>Usando diagnósticos do VSS

Vsdiagview e Vssagent são ferramentas que você pode usar para solucionar problemas de aplicativos VSS.

> [!Note]  
> essas ferramentas estão incluídas no SDK (Software Development Kit) do Microsoft Windows para Windows Vista e posterior. você pode baixar o SDK do Windows do [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

na instalação do SDK do Windows, essas ferramentas podem ser encontradas em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para a Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para Windows de 32 bits).

## <a name="gathering-data"></a>Coletando dados

Você pode coletar dados usando o comando Vssagent.

**Para coletar dados usando o Vssagent**

1.  Para coletar dados da linha de comando, use o comando Vssagent da seguinte maneira:

    **vssagent-coletar** *xmlFileName * * * .xml**

2.  Para exibir o arquivo de saída, consulte a seção exibindo dados a seguir.

## <a name="viewing-data"></a>Exibindo dados

O aplicativo Vsdiagview pode ser usado para exibir dados que foram coletados usando o comando Vssagent. Vsdiagview exibe as seguintes informações sobre o computador:

-   Informações sobre o computador, como a versão do sistema operacional, a memória total disponível e a velocidade da CPU
-   Os nomes e os números de versão dos binários do VSS
-   Os nomes e as propriedades dos dispositivos de disco e volume
-   Os nomes e as propriedades de qualquer aplicativo COM+
-   Os nomes dos logs de eventos que podem ser usados para diagnosticar problemas de VSS
-   Os nomes de qualquer gravador VSS e os eventos que eles manipulam
-   Informações sobre outros arquivos do sistema operacional

**Para exibir dados usando o Vsdiagview**

1.  No menu arquivo, escolha **abrir** para procurar um arquivo. (O local padrão é C: \\ vssdiag.)
2.  Clique em **abrir** para exibir os dados.

 

 



