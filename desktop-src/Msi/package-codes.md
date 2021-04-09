---
description: O código do pacote é um GUID que identifica um determinado pacote de Windows Installer.
ms.assetid: dcb6a0d4-e28d-453d-9bda-bfe74f74579b
title: Códigos de pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aa77dbc6c11a1b420572293669a4177f7845ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091532"
---
# <a name="package-codes"></a>Códigos de pacote

O código do pacote é um GUID que identifica um determinado [*pacote*](p-gly.md)de Windows Installer. O código do pacote associa um arquivo. msi a um aplicativo ou produto e também pode ser usado para a verificação de fontes. Os códigos do produto e do pacote não são intercambiáveis. Para obter detalhes, consulte [códigos de produto](product-codes.md).

Arquivos. msi não idênticos não devem ter o mesmo código de pacote. É importante alterar o código do pacote porque ele é o identificador principal usado pelo instalador para pesquisar e validar o pacote correto para uma determinada instalação. Se um pacote for alterado sem alterar o código do pacote, o instalador não poderá usar o pacote mais recente se ambos ainda estiverem acessíveis ao instalador.

O código do pacote é armazenado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do fluxo de informações de [Resumo](summary-information-stream.md). Observe que as letras no código do produto e nos GUIDs de código do pacote devem estar em letras maiúsculas. Utilitários como o GUIDGEN geram GUIDs contendo letras minúsculas. As letras minúsculas nesses GUIDs devem ser alteradas para letras maiúsculas para serem usadas como código do produto ou código do pacote.

Embora seja comum enviar um aplicativo que tenha o mesmo código de pacote e código do produto, os dois valores podem divergir à medida que o aplicativo é atualizado. Por exemplo, a inclusão de um novo arquivo com o aplicativo exigiria a atualização do banco de dados de instalação para instalar o arquivo. Se as alterações forem secundárias, um desenvolvedor poderá optar por não alterar o código do produto, no entanto, um arquivo. msi diferente será necessário para instalar o novo arquivo e, portanto, o código do pacote deverá ser incrementado. Por outro lado, um único pacote pode ser usado para instalar mais de um produto. Por exemplo, a instalação de um pacote sem uma transformação de linguagem pode instalar a versão em inglês do aplicativo e a instalação do mesmo pacote com uma transformação de linguagem pode instalar a versão em francês. A transformação é distinta do arquivo. msi que determina o código do pacote. As versões em inglês e francês podem ter códigos de produto diferentes e o mesmo código de pacote porque ambos estão instalados com o mesmo arquivo. msi.

 

 



