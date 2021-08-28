---
description: Você pode aplicar a pequena atualização a uma imagem de origem administrativa do MNP2000.msi instalando o patch de exemplo MNP2000.msp criado em Gerando um Pacote de Patch.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Aplicando um pacote de patch a uma instalação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c29cbec604ae18745348a62f147d13d2ccbf06c0620b3a5dcca7c6c009045b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105436"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Aplicando um pacote de patch a uma instalação administrativa

Você pode aplicar a pequena atualização a uma imagem de origem administrativa do MNP2000.msi instalando o patch de exemplo MNP2000.msp criado em [Gerando](generating-a-patch-package.md)um pacote de patch . A atualização pode então ser propagada para os usuários solicitando que eles reinstalem o aplicativo da nova imagem de origem administrativa.

Um administrador pode usar a linha de comando a seguir para atualizar a imagem de origem administrativa localizada em //server/MNP2000.msi para uma nova imagem de origem que é a mesma que seria produzida por uma instalação administrativa de um CD-ROM totalmente atualizado.

**msiexec /a //server/MNP2000.msi /p MNP2000.msp**

Os membros do grupo de trabalho que usam MNP2000 devem reinstalar o aplicativo da nova imagem de origem administrativa para receber a atualização.

Para reinstalar completamente os aplicativos e armazenar em cache o arquivo .msi no computador do usuário, os usuários podem inserir qualquer um dos comandos a seguir.

**msiexec /fvomus //server/MNP2000.msi**

**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**

Para reinstalar apenas o recurso Concert atualizado e armazenar em cache o arquivo .msi no computador do usuário, os usuários podem inserir o comando a seguir.

**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**

## <a name="next-example"></a>Próximo exemplo

[Um exemplo de localização](a-localization-example.md)

 

 



