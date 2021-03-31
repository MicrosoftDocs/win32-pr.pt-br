---
description: Você pode aplicar a atualização pequena a uma imagem de origem administrativa do MNP2000.msi instalando o patch de exemplo MNP2000. msp criado na geração de um pacote de patch.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Aplicando um pacote de patch a uma instalação administrativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921517"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Aplicando um pacote de patch a uma instalação administrativa

Você pode aplicar a atualização pequena a uma imagem de origem administrativa do MNP2000.msi instalando o patch de exemplo MNP2000. msp criado na [geração de um pacote de patch](generating-a-patch-package.md). A atualização pode ser propagada para os usuários solicitando que eles reinstalem o aplicativo da nova imagem de origem administrativa.

Um administrador pode usar a seguinte linha de comando para atualizar a imagem de origem administrativa localizada em//Server/MNP2000.msi para uma nova imagem de origem que seja a mesma produzida por uma instalação administrativa de um CD-ROM totalmente atualizado.

**msiexec/a//Server/MNP2000.msi/p MNP2000. msp**

Os membros do grupo de trabalho usando MNP2000, em seguida, devem reinstalar o aplicativo da nova imagem de origem administrativa para receber a atualização.

Para reinstalar completamente os aplicativos e armazenar em cache o arquivo. msi atualizado no computador do usuário, os usuários podem inserir um dos comandos a seguir.

**msiexec/fvomus//Server/MNP2000.msi**

**msiexec/I//Server/MNP2000.msi reinstalar = todas as reinstalaçãomode = vomus**

Para reinstalar apenas o recurso de concerto atualizado e armazenar em cache o arquivo. msi atualizado no computador do usuário, os usuários podem digitar o comando a seguir.

**msiexec/I//Server/MNP2000.msi reinstalar = Concert REINSTALLMODE = vomus**

## <a name="next-example"></a>Próximo exemplo

[Um exemplo de localização](a-localization-example.md)

 

 



