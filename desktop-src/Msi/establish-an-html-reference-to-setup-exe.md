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
# <a name="establish-an-html-reference-to-setupexe"></a>Estabelecer uma referência HTML para Setup.exe

A etapa final é fazer uma referência para o Setup.exe na página da Web hipotética MySetup (MySetup.html) descrita em [um exemplo de instalação com base em URL Windows Installer](a-url-based-windows-installer-installation-example.md). Use o seguinte script HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Clicar no link "MySetup Installation" apresenta aos usuários a opção de salvar ou executar a partir desse local. Se o usuário selecionar executar nesse local, o Setup.exe atualizará a versão do Windows Installer no computador, se necessário, verificará a assinatura digital no pacote do instalador e instalará o pacote em seu computador.

Isso conclui o exemplo.

 

 



