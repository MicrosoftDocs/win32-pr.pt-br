---
description: Um arquivo é uma unidade de dados no sistema de arquivos que um usuário pode acessar e gerenciar.
ms.assetid: 271bad79-c23b-45ee-938c-d17dae89db1a
title: Arquivos e clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75384900d5d487ab02bd19c13cc2c25e9a310b3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165255"
---
# <a name="files-and-clusters"></a>Arquivos e clusters

Um *arquivo* é uma unidade de dados no sistema de arquivos que um usuário pode acessar e gerenciar. Um arquivo deve ter um nome exclusivo em seu diretório. Ele consiste em um ou mais fluxos de bytes que contêm um conjunto de dados relacionados, além de um conjunto de atributos (também chamados de propriedades) que descrevem o arquivo ou os dados dentro do arquivo. A hora de criação de um arquivo é um exemplo de um atributo de arquivo.

Quando um arquivo é criado, um fluxo padrão não nomeado é criado para armazenar todos os dados gravados no arquivo enquanto ele está aberto. Você também pode criar fluxos adicionais dentro do arquivo. Esses fluxos adicionais são chamados de fluxos alternativos. A figura a seguir descreve um arquivo com o fluxo padrão e dois fluxos alternativos.

![arquivo com um fluxo padrão e dois fluxos alternativos](images/fig1.png)

Os atributos de arquivo não são armazenados nos fluxos de dados com os dados do arquivo, mas são armazenados em outro lugar e gerenciados pelo sistema operacional.

Todos os dados do sistema de arquivos, incluindo os diretórios e o código de inicialização do sistema, são armazenados pelo sistema de arquivos NTFS em arquivos. Outros sistemas de arquivos armazenam essas informações em regiões de disco externas ao sistema de arquivos. Uma vantagem de armazenar essas informações em arquivos é que o Windows pode localizar, acessar e manter as informações facilmente. Outras vantagens são que cada um desses arquivos pode ser protegido por um descritor de segurança e, no caso de corrupção parcial do disco, eles podem ser rapidamente realocados para uma parte mais segura do disco.

A unidade de armazenamento fundamental de todos os sistemas de arquivos com suporte é um *cluster*, que é um grupo de setores. Isso permite que o sistema de arquivos Otimize a administração de dados de disco independentemente do tamanho de setor de disco definido pelo controlador de disco de hardware. Se o disco a ser administrado for grande e grandes quantidades de dados forem movidos e organizados em uma única operação, o administrador poderá ajustar o tamanho do cluster para acomodar isso.

O Windows gerencia arquivos por meio de [objetos de arquivo](file-objects.md), [identificadores de arquivo](file-handles.md)e [ponteiros de arquivo](file-pointers.md).

Para obter mais informações sobre fluxos de arquivos, consulte [fluxos de arquivos](file-streams.md). Para obter mais informações sobre clusters, consulte [clusters e extensões](clusters-and-extents.md). Para obter mais informações sobre como acessar e gerenciar arquivos, consulte [Gerenciamento de arquivos](file-management.md) e [referência de gerenciamento de arquivos](file-management-reference.md).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                       | Descrição                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Fluxos de arquivos](file-streams.md)<br/>                 | No sistema de arquivos NTFS, os fluxos contêm os dados gravados em um arquivo, e isso fornece mais informações sobre um arquivo do que atributos e propriedades.<br/>                                                                                         |
| [Objetos de arquivo](file-objects.md)<br/>                 | Os *objetos de arquivo* funcionam como a interface lógica entre os processos de kernel e de modo de usuário e os dados de arquivo que residem no disco físico.<br/>                                                                                                      |
| [Identificadores de arquivo](file-handles.md)<br/>                 | Quando um arquivo é aberto por um processo usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , um *identificador de arquivo* é associado a ele até que o processo seja encerrado ou o identificador seja fechado usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .<br/> |
| [Ponteiros de arquivo](file-pointers.md)<br/>               | Um ponteiro de arquivo é um valor de deslocamento de 64 bits que especifica o próximo byte a ser lido ou o local para receber o próximo byte gravado.<br/>                                                                                                                 |
| [Clusters e extensões](clusters-and-extents.md)<br/> | Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume.<br/>                                                                                                                                                   |



 

 

