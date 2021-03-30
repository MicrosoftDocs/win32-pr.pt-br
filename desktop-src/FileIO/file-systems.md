---
description: Gerenciar diretórios com tabela de entrada de diretório, identificadores de diretório, pontos de nova análise.
title: Sistemas de arquivos locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661796"
---
# <a name="local-file-systems"></a>Sistemas de arquivos locais

Um *sistema de arquivos* permite que os aplicativos armazenem e recuperem arquivos em dispositivos de armazenamento. Os arquivos são colocados em uma estrutura hierárquica. O sistema de arquivos especifica convenções de nomenclatura para arquivos e o formato para especificar o caminho para um arquivo na estrutura de árvore.

Cada sistema de arquivos consiste em um ou mais drivers e bibliotecas de vínculo dinâmico que definem os formatos de dados e os recursos do sistema de arquivos. Os sistemas de arquivos podem existir em vários tipos diferentes de dispositivos de armazenamento, incluindo discos rígidos, jukeboxes, discos ópticos removíveis, unidades de backup de fita e cartões de memória.

Todos os sistemas de arquivos com suporte do Windows têm os seguintes componentes de armazenamento:

-   Volumes. Um *volume* é uma coleção de diretórios e arquivos.
-   Listas. Um *diretório* é uma coleção hierárquica de diretórios e arquivos.
-   Arquivos. Um *arquivo* é um agrupamento lógico de dados relacionados.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                | Descrição                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Gerenciamento de diretórios](directory-management.md)<br/>          | Um *diretório* é uma coleção hierárquica de diretórios e arquivos. A única restrição no número de arquivos que podem estar contidos em um único diretório é o tamanho físico do disco no qual o diretório está localizado.<br/> |
| [Gerenciamento de disco](disk-management.md)<br/>                    | Um *disco rígido* é uma unidade rígida dentro de um computador que armazena e fornece acesso relativamente rápido a grandes quantidades de dados. É o tipo de armazenamento usado com mais frequência com o Windows. O sistema também dá suporte a mídia removível.<br/>    |
| [Gerenciamento de Arquivos](file-management.md)<br/>                    | Um *objeto File* fornece uma representação de um recurso (um dispositivo físico ou um recurso localizado em um dispositivo físico) que pode ser gerenciado pelo sistema de e/s.<br/>                                                            |
| [NTFS Transacional (TxF)](transactional-ntfs-portal.md)<br/> | O NTFS Transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação.<br/>                                                                                                                 |
| [Gerenciamento de volume](volume-management.md)<br/>                | O nível mais alto de organização no sistema de arquivos é o *volume*. Um sistema de arquivos reside em um volume.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência técnica de FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))
</dt> <dt>

[Tecnologias de sistemas de arquivos](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))
</dt> <dt>

[Referência técnica do NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

