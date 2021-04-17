---
description: Este exemplo ilustra como uma transformação de personalização pode ser usada para desabilitar recursos e adicionar novos recursos.
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: Um exemplo de transformação de personalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748603"
---
# <a name="a-customization-transform-example"></a>Um exemplo de transformação de personalização

Este exemplo ilustra como uma transformação de personalização pode ser usada para desabilitar recursos e adicionar novos recursos.

Um administrador pode desabilitar permanentemente um recurso usando uma transformação de personalização para inserir um 0 na coluna nível da tabela de [recursos](feature-table.md). A aplicação da transformação de personalização impede a instalação e a exibição desse recurso, mesmo que o usuário selecione uma instalação completa usando a interface do usuário ou definindo a propriedade [**ADDLOCAL**](addlocal.md) como All na linha de comando. Para obter uma discussão sobre o nível de instalação, consulte [tabela de recursos](feature-table.md) e propriedade [**INSTALLLEVEL**](installlevel.md) .

Os recursos necessários para personalizar um aplicativo podem ser implantados usando uma transformação de personalização para adicionar um ou mais novos componentes. A transformação deve adicionar um ou mais novos recursos para conter esses novos componentes. Para as regras que devem ser seguidas durante a implantação de recursos, como arquivos, chaves do registro ou atalhos, consulte [usando transformações para adicionar recursos](using-transforms-to-add-resources.md).

Este exemplo ilustra como criar uma [transformação](transforms.md) para personalizar a instalação do aplicativo descrito em [um exemplo de instalação](an-installation-example.md). O pacote de instalação original instala todos os recursos do aplicativo de exemplo, incluindo a porta do recurso, que permite aos usuários exibir informações de admissão para a arena do Parque vermelho. Alguns grupos de usuários só precisam dos recursos do aplicativo que fornecem informações de agendamento de eventos e não precisam do recurso de portão. Esses grupos também precisam obter uma lista de telefones especial. Portanto, a transformação deve fazer duas coisas: 1) personalizar a instalação para que esse grupo receba apenas os recursos de aplicativo necessários e 2) forneça os recursos necessários para a nova lista de telefones.

Um exemplo de uma interface de usuário mínima para esse exemplo é fornecido nos [componentes SDK do Windows para Windows Installer desenvolvedores](platform-sdk-components-for-windows-installer-developers.md) como o arquivo Uisample.msi. Se você tiver o SDK, terá acesso a todas as ferramentas e dados necessários para reproduzir o pacote de instalação de exemplo, a interface do usuário e a transformação de personalização.

A transformação personalização tem as seguintes especificações:

-   A transformação personalização é inserida dentro do arquivo de MNP2000.msi para garantir que ele esteja sempre disponível com o banco de dados de instalação.
-   A instalação do MNP2000.msi com a transformação personalização não instala o recurso de portão, os recursos filho do recurso de portão ou qualquer um dos componentes do recurso de portão, mesmo que o usuário selecione o tipo completo de instalação.
-   Outros aplicativos podem compartilhar alguns ou todos os componentes do recurso de portão. Os pacotes de instalação desses aplicativos podem instalar todos os seus componentes no computador do usuário.
-   Remover MNP2000.msi com a transformação de personalização não remove nenhum dos componentes de porta que foram instalados por outros aplicativos.
-   A instalação do MNP2000.msi com a transformação personalização também instala um novo recurso de nível superior, lista de telefones \_ e um novo componente, telefone, que requer a instalação do recurso, Phone.txt. O usuário acessa o recurso de \_ lista telefônica usando um atalho no diretório de menus.

[Continuar](customizing-an-original-database.md)

 

 



