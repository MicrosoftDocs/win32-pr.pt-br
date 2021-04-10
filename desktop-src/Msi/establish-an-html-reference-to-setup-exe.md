---
description: A etapa final é fazer uma referência para o Setup.exe na página da Web hipotética MySetup (MySetup.html) descrita em um exemplo de instalação com base em URL Windows Installer.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Estabelecer uma referência HTML para Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169857"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="b2eed-103">Estabelecer uma referência HTML para Setup.exe</span><span class="sxs-lookup"><span data-stu-id="b2eed-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="b2eed-104">A etapa final é fazer uma referência para o Setup.exe na página da Web hipotética MySetup (MySetup.html) descrita em [um exemplo de instalação com base em URL Windows Installer](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="b2eed-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="b2eed-105">Use o seguinte script HTML:</span><span class="sxs-lookup"><span data-stu-id="b2eed-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="b2eed-106">Clicar no link "MySetup Installation" apresenta aos usuários a opção de salvar ou executar a partir desse local.</span><span class="sxs-lookup"><span data-stu-id="b2eed-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="b2eed-107">Se o usuário selecionar executar nesse local, o Setup.exe atualizará a versão do Windows Installer no computador, se necessário, verificará a assinatura digital no pacote do instalador e instalará o pacote em seu computador.</span><span class="sxs-lookup"><span data-stu-id="b2eed-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="b2eed-108">Isso conclui o exemplo.</span><span class="sxs-lookup"><span data-stu-id="b2eed-108">This completes the example.</span></span>

 

 



