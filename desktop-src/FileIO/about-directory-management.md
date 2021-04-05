---
description: Um diretório que contém um ou mais diretórios é o pai do diretório ou dos diretórios contidos, e cada diretório contido é um filho do diretório pai. A estrutura hierárquica de diretórios é conhecida como árvore de diretórios.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Sobre o gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827159"
---
# <a name="about-directory-management"></a>Sobre o gerenciamento de diretório

Um diretório que contém um ou mais diretórios é o *pai* do diretório ou dos diretórios contidos, e cada diretório contido é um *filho* do diretório pai. A estrutura hierárquica de diretórios é conhecida como árvore de *diretórios*.

O sistema de arquivos NTFS implementa o link lógico entre um diretório e os arquivos que ele contém como uma *tabela de entrada de diretório*. Quando um arquivo é movido para um diretório, uma entrada é criada na tabela para o arquivo movido e o nome do arquivo é colocado na entrada. Quando um arquivo contido em um diretório é excluído, o nome e a entrada correspondentes ao arquivo excluído também são excluídos da tabela. Mais de uma entrada para um único arquivo pode existir em uma tabela de entrada de diretório. Se uma entrada adicional for criada na tabela para um arquivo, essa entrada será referida como um *link físico* para esse arquivo. Não há nenhum limite para o número de links físicos que podem ser criados para um único arquivo.

Os diretórios também podem conter junções e pontos de nova análise.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                 | Descrição                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Criando e excluindo diretórios](creating-and-deleting-directories.md)<br/> | Um aplicativo pode criar e excluir diretórios programaticamente.<br/>                          |
| [Identificadores de diretório](obtaining-a-handle-to-a-directory.md)<br/>                 | Sempre que um processo cria ou abre um objeto de diretório, ele recebe um identificador para o objeto.<br/> |
| [Pontos de reanálise](reparse-points.md)<br/>                                       | Descreve pontos de nova análise.<br/>                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de gerenciamento de diretório](directory-management-reference.md)
</dt> </dl>

 

 




