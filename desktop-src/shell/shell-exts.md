---
description: Este conjunto de tópicos discute como implementar os manipuladores de extensão que permitem modificar uma variedade de ações de Shell.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Trabalhando com extensões de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbb696f4536cdb0fb6869be073771d431bd8d2de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968175"
---
# <a name="working-with-shell-extensions"></a>Trabalhando com extensões de Shell

Os recursos do Shell podem ser estendidos com entradas de registro e arquivos. ini. Embora essa abordagem para estender o shell seja simples e adequada para muitas finalidades, ela é limitada. Por exemplo, se você usar o registro para especificar um ícone personalizado para um tipo de arquivo, o mesmo ícone será exibido para cada arquivo desse tipo. Estender o shell com o registro não permite que você varie o ícone para diferentes membros do tipo de arquivo. Outros aspectos do Shell, como a folha de propriedades **Propriedades** que podem ser exibidas quando um arquivo é clicado com o botão direito do mouse, não podem ser modificados com o registro.

Uma abordagem mais poderosa e flexível para estender o Shell é implementar *manipuladores de extensão de shell*. Esses manipuladores podem ser implementados para uma variedade de ações que o Shell pode executar. Antes de executar a ação, o Shell consulta o manipulador de extensão, dando a ele a oportunidade de modificar a ação. Um exemplo comum é um manipulador de extensão de menu de atalho. Se um for implementado para um tipo de arquivo, ele será consultado toda vez que um dos arquivos for clicado com o botão direito do mouse. O manipulador pode, então, especificar itens de menu adicionais de acordo com o arquivo, em vez de ter o mesmo conjunto para todos os arquivos desse tipo de arquivo.

Este conjunto de tópicos discute como implementar os manipuladores de extensão que permitem modificar uma variedade de ações de Shell. Os manipuladores a seguir estão associados a um tipo de arquivo específico e permitem que você especifique em uma base arquivo por arquivo.



| Manipulador                                               | Descrição                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulador de menu de atalho](context-menu-handlers.md)    | Chamado antes de o menu de atalho de um arquivo ser exibido. Ele permite que você adicione itens ao menu de atalho de acordo com o arquivo.                                               |
| [Manipulador de dados](how-to-create-data-handlers.md)       | Chamado quando uma operação de arrastar e soltar é executada em objetos do Shell. Ele permite que você forneça formatos de área de transferência adicionais para o destino de soltar.                            |
| [Descartar manipulador](how-to-create-drop-handlers.md)       | Chamado quando um objeto de dados é arrastado ou solto em um arquivo. Ele permite que você faça um arquivo em um destino de soltura.                                                          |
| [Manipulador de ícone](how-to-create-icon-handlers.md)       | Chamado antes do ícone de um arquivo ser exibido. Ele permite que você substitua o ícone padrão do arquivo por um ícone personalizado em cada arquivo.                                    |
| [Manipulador de folha de propriedades](propsheet-handlers.md)      | Chamado antes da exibição da folha de propriedades de **Propriedades** de um objeto. Ele permite que você adicione ou substitua páginas.                                                              |
| [**Manipulador de imagem em miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornece uma imagem para representar o item.                                                                                                                                   |
| [**Manipulador de infodicas**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornece texto pop-up quando o usuário passa o ponteiro do mouse sobre o objeto.                                                                                               |
| [**Manipulador de metadados**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Fornece acesso de leitura e gravação a metadados (Propriedades) armazenados em um arquivo. Isso pode ser usado para estender a exibição de detalhes, infotips, a página de propriedades e agrupar recursos. |



 

Outros não estão associados a um tipo de arquivo específico, mas são chamados antes de algumas operações de Shell.



| Manipulador                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulador de coluna](../lwef/column-handlers.md)                             | Chamado pelo Windows Explorer antes de exibir a exibição de detalhes de uma pasta. Ele permite que você adicione colunas personalizadas à exibição de detalhes.        |
| [Copiar manipulador de gancho](how-to-create-copy-hook-handlers.md)          | Chamado quando um objeto de pasta ou de impressora está prestes a ser movido, copiado, excluído ou renomeado. Ele permite que você aprove ou veta a operação.   |
| [Manipulador do tipo "arrastar e soltar"](context-menu-handlers.md)                 | Chamado quando um arquivo é arrastado com o botão direito do mouse. Ele permite que você modifique o menu de atalho que é exibido.                     |
| [Manipulador de sobreposição de ícone](how-to-implement-icon-overlay-handlers.md) | Chamado antes do ícone de um arquivo ser exibido. Ele permite que você especifique uma sobreposição para o ícone do arquivo.                                          |
| [Manipulador de pesquisa](../lwef/search-handlers.md)                             | Chamado para iniciar um mecanismo de pesquisa. Ele permite que você implemente um mecanismo de pesquisa personalizado acessível no menu **Iniciar** ou no Windows Explorer. |



 

Os detalhes de como implementar manipuladores de extensão específicos são abordados nas seções listadas acima. Para discussões sobre problemas de implementação que são comuns a todos os manipuladores de extensão do Shell, consulte estes tópicos:

-   [Inicializando manipuladores de extensão do Shell](int-shell-exts.md)
-   [Registrando manipuladores de extensão do Shell](reg-shell-exts.md)

 

 
