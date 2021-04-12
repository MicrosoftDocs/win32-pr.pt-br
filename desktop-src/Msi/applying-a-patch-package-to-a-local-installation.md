---
description: Você pode aplicar a atualização pequena a uma instalação local do MNP2000 com o patch de exemplo MNPpatch. msp criado na geração de um pacote de patch.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Aplicando um pacote de patch a uma instalação local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169209"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a>Aplicando um pacote de patch a uma instalação local

Você pode aplicar a atualização pequena a uma instalação local do MNP2000 com o patch de exemplo MNPpatch. msp criado na [geração de um pacote de patch](generating-a-patch-package.md). O procedimento geral é abordado na seção [aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md).

Instale o produto MNP2000 original localmente no seu computador. Verifique se isso tem o erro Concert.txt que a pequena atualização deve ser corrigida. Em seguida, inicie a instalação inserindo a seguinte linha de comando.

**msiexec/p MNP2000. msp reinstalar = todos os REINSTALLMODE = omus**

Examine novamente as Concert.txt pertencentes a MNP2000 para verificar se o instalador aplicou a pequena atualização para corrigir esse arquivo.

Para aplicar a pequena atualização a uma imagem administrativa, consulte [aplicando um pacote de patch a uma instalação administrativa](applying-a-patch-package-to-an-administrative-installation.md).

[Continuar](applying-a-patch-package-to-an-administrative-installation.md)

 

 



