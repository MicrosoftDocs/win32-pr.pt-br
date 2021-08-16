---
description: A etapa final é colocar uma referência ao Setup.exe na página da Web do MySetup hipotética (MySetup.html) descrita em Um Exemplo de instalação do instalador baseado em URL Windows.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Estabelecer uma referência HTML para Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22be693c4e2e411fa724a70f90da4af4af4cf17ad6bb316bd3a483dd55bfd5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378066"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Estabelecer uma referência HTML para Setup.exe

A etapa final é colocar uma referência ao Setup.exe na página da Web do MySetup hipotética (MySetup.html) descrita em Exemplo de instalação do instalador baseado em [URL Windows](a-url-based-windows-installer-installation-example.md). Use o seguinte script HTML:

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Clicar no link "Instalação do MySetup" apresenta aos usuários a opção de salvar ou executar nesse local. Se o usuário selecionar executar nesse local, o Setup.exe atualizará a versão do Instalador do Windows no computador, se necessário, verificará a assinatura digital no pacote do instalador e instalará o pacote em seu computador.

Isso conclui o exemplo.

 

 



