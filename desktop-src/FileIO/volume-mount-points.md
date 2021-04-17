---
description: Usando pastas montadas, você pode unificar sistemas de arquivos diferentes, como o sistema de arquivos NTFS, um sistema de arquivos FAT de 16 bits e um sistema de arquivos ISO-9660 em uma unidade de CD-ROM em um sistema de arquivos lógico em um único volume NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Pastas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812955"
---
# <a name="mounted-folders"></a>Pastas montadas

O sistema de arquivos NTFS dá suporte a pastas montadas. Uma *pasta montada* é uma associação entre um volume e um diretório em outro volume. Quando uma pasta montada é criada, os usuários e os aplicativos podem acessar o volume de destino usando o caminho para a pasta montada ou usando a letra da unidade do volume. Por exemplo, um usuário pode criar uma pasta montada para associar a unidade D: com a \\ pasta c: mnt \\ DDrive na unidade C. Depois de criar a pasta montada, o usuário pode usar o caminho "C: \\ mnt \\ DDrive" para acessar a unidade D: como se fosse uma pasta na unidade C:.

Usando pastas montadas, você pode unificar sistemas de arquivos diferentes, como o sistema de arquivos NTFS, um sistema de arquivos FAT de 16 bits e um sistema de arquivos ISO-9660 em uma unidade de CD-ROM em um sistema de arquivos lógico em um único volume NTFS. Nem os usuários nem aplicativos precisam de informações sobre o volume de destino no qual um arquivo específico está localizado. Todas as informações necessárias para localizar um arquivo especificado são um caminho completo usando uma pasta montada no volume NTFS. Os volumes podem ser reorganizados, substituídos ou subdivididos em muitos volumes sem que os usuários ou aplicativos precisem alterar as configurações.

Para obter informações sobre pastas montadas, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                         | Descrição                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Criando pastas montadas](mounting-and-dismounting-a-volume.md)<br/>                                                  | A criação de uma pasta montada é um processo de duas etapas.<br/>                                                                                                                                                                 |
| [Enumerando pastas montadas](enumerating-volume-mount-points.md)<br/>                                                 | Funções a serem usadas para enumerar pastas montadas em um volume.<br/>                                                                                                                                                       |
| [Determinando se um diretório é uma pasta montada](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | Como determinar se um diretório especificado é uma pasta montada.<br/>                                                                                                                                              |
| [Atribuindo uma letra de unidade a um volume](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | Você pode atribuir uma letra de unidade (por exemplo, X: \) para um volume local usando a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , desde que não haja nenhum volume já atribuído a essa letra de unidade.<br/> |
| [Funções de pasta montadas](volume-mount-point-functions.md)<br/>                                                       | Funções usadas para gerenciar pastas montadas.<br/>                                                                                                                                                                        |



 

Para obter exemplos, consulte [exemplos de pastas montadas](volume-mount-point-examples.md).

 

 




