---
description: Este conjunto de tópicos discute como implementar os manipuladores de extensão que permitem modificar uma variedade de ações do Shell.
ms.assetid: 794b6369-665f-49a9-a263-7c736c5ce8ac
title: Trabalhando com extensões do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 804b121ccf633b44574ae956b367143eebdaf7a2a3a8a9cc8400995522b4cbef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452833"
---
# <a name="working-with-shell-extensions"></a>Trabalhando com extensões do Shell

Os recursos do Shell podem ser estendidos com entradas do Registro e .ini arquivos. Embora essa abordagem para estender o Shell seja simples e adequada para muitas finalidades, ela é limitada. Por exemplo, se você usar o Registro para especificar um ícone personalizado para um tipo de arquivo, o mesmo ícone será exibido para cada arquivo desse tipo. Estender o Shell com o Registro não permite que você varie o ícone para membros diferentes do tipo de arquivo. Outros aspectos do Shell, como a folha de propriedades **Propriedades** que podem ser exibidos quando um arquivo é clicado com o botão direito do mouse, não podem ser modificados com o Registro.

Uma abordagem mais eficiente e flexível para estender o Shell é implementar manipuladores *de extensão de shell*. Esses manipuladores podem ser implementados para uma variedade de ações que o Shell pode tomar. Antes de tomar a ação, o Shell consulta o manipulador de extensão, dando a ele a oportunidade de modificar a ação. Um exemplo comum é um manipulador de extensão de menu de atalho. Se um for implementado para um tipo de arquivo, ele será consultado sempre que um dos arquivos for clicado com o botão direito do mouse. O manipulador pode especificar itens de menu adicionais em uma base de arquivo por arquivo, em vez de ter o mesmo conjunto para todos os arquivos desse tipo de arquivo.

Este conjunto de tópicos discute como implementar os manipuladores de extensão que permitem modificar uma variedade de ações do Shell. Os manipuladores a seguir são associados a um tipo de arquivo específico e permitem que você especifique em uma base de arquivo por arquivo.



| Manipulador                                               | Descrição                                                                                                                                                                |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulador de menu de atalho](context-menu-handlers.md)    | Chamado antes que o menu de atalho de um arquivo seja exibido. Ele permite que você adicione itens ao menu de atalho em uma base de arquivo por arquivo.                                               |
| [Manipulador de dados](how-to-create-data-handlers.md)       | Chamado quando uma operação do tipo "arrastar e soltar" é executada em objetos shell. Ele permite que você forneça formatos de área de transferência adicionais para o destino de soltar.                            |
| [Manipulador de soltar](how-to-create-drop-handlers.md)       | Chamado quando um objeto de dados é arrastado ou descartado em um arquivo. Ele permite que você faça um arquivo em um destino de soltar.                                                          |
| [Manipulador de ícones](how-to-create-icon-handlers.md)       | Chamado antes que o ícone de um arquivo seja exibido. Ele permite que você substitua o ícone padrão do arquivo por um ícone personalizado em uma base de arquivo por arquivo.                                    |
| [Manipulador de folha de propriedades](propsheet-handlers.md)      | Chamado antes que a folha de propriedades **Propriedades** de um objeto seja exibida. Ele permite que você adicione ou substitua páginas.                                                              |
| [**Manipulador de imagem em miniatura**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) | Fornece uma imagem para representar o item.                                                                                                                                   |
| [**Manipulador de infodicas**](/windows/win32/api/shlobj_core/nn-shlobj_core-iqueryinfo)                 | Fornece texto pop-up quando o usuário passar o ponteiro do mouse sobre o objeto.                                                                                               |
| [**Manipulador de metadados**](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)       | Fornece acesso de leitura e gravação a metadados (propriedades) armazenados em um arquivo. Isso pode ser usado para estender a exibição Detalhes, as infotips, a página de propriedades e os recursos de grupo. |



 

Outros não estão associados a um tipo de arquivo específico, mas são chamados antes de algumas operações do Shell.



| Manipulador                                                            | Descrição                                                                                                                                  |
|--------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Manipulador de coluna](../lwef/column-handlers.md)                             | Chamado pelo Windows Explorer antes de exibir a exibição Detalhes de uma pasta. Ele permite que você adicione colunas personalizadas à exibição Detalhes.        |
| [Manipulador de gancho de cópia](how-to-create-copy-hook-handlers.md)          | Chamado quando um objeto de pasta ou impressora está prestes a ser movido, copiado, excluído ou renomeado. Ele permite que você aprove ou veta a operação.   |
| [Manipulador do tipo "arrastar e soltar"](context-menu-handlers.md)                 | Chamado quando um arquivo é arrastado com o botão direito do mouse. Ele permite que você modifique o menu de atalho exibido.                     |
| [Manipulador de sobreposição de ícone](how-to-implement-icon-overlay-handlers.md) | Chamado antes que o ícone de um arquivo seja exibido. Ele permite que você especifique uma sobreposição para o ícone do arquivo.                                          |
| [Manipulador de pesquisa](../lwef/search-handlers.md)                             | Chamado para iniciar um mecanismo de pesquisa. Ele permite que você implemente um mecanismo de pesquisa personalizado acessível no menu **Iniciar** ou Windows Explorer. |



 

Os detalhes de como implementar manipuladores de extensão específicos são abordados nas seções listadas acima. Para discussões sobre problemas de implementação comuns a todos os manipuladores de extensão do Shell, consulte estes tópicos:

-   [Inicializando manipuladores de extensão do Shell](int-shell-exts.md)
-   [Registrando manipuladores de extensão do Shell](reg-shell-exts.md)

 

 
