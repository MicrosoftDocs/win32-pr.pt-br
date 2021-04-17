---
description: Os volumes são implementados por um driver de dispositivo chamado Gerenciador de volumes.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Sobre o gerenciamento de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759421"
---
# <a name="about-volume-management"></a>Sobre o gerenciamento de volume

Os volumes são implementados por um driver de dispositivo chamado Gerenciador de volumes. Os exemplos incluem o Gerenciador de FtDisk, o Gerenciador de discos lógicos (LDM) e o Gerenciador de volumes lógicos (LVM) da VERITAS. Os gerenciadores de volumes fornecem uma camada de abstração física, proteção de dados (usando alguma forma de RAID) e desempenho.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                       | Descrição                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Reconhecimento do sistema de arquivos](file-system-recognition.md)<br/>           | A meta do reconhecimento do sistema de arquivos é permitir que o sistema operacional Windows tenha uma opção adicional para um sistema de arquivos válido, mas não reconhecido, diferente de "RAW".<br/>                                                                                                         |
| [Nomeando um volume](naming-a-volume.md)<br/>                           | Um rótulo é um nome amigável que é atribuído a um volume, geralmente por um usuário final, para facilitar o reconhecimento. Um volume pode ter um rótulo, uma letra da unidade, ambos ou nenhum. Para definir o rótulo de um volume, use a função [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .<br/> |
| [Enumerando volumes](enumerating-volumes.md)<br/>                   | Para fazer uma lista completa dos volumes em um computador ou manipular cada volume por vez, você pode enumerar volumes.<br/>                                                                                                                                                       |
| [Obtendo informações de volume](obtaining-volume-information.md)<br/> | Antes de acessar arquivos e diretórios em um determinado volume, você deve determinar os recursos do sistema de arquivos usando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .<br/>                                                                              |
| [Diários de alterações](change-journals.md)<br/>                           | Quando qualquer alteração é feita em um arquivo ou diretório em um volume, o diário de alterações do USN desse volume é atualizado com uma descrição da alteração e o nome do arquivo ou diretório.<br/>                                                                                        |
| [Pastas montadas](volume-mount-points.md)<br/>                       | Usando pastas montadas, você pode unificar sistemas de arquivos diferentes, como o sistema de arquivos NTFS, um sistema de arquivos FAT de 16 bits e um sistema de arquivos ISO-9660 em uma unidade de CD-ROM em um sistema de arquivos lógico em um único volume NTFS.<br/>                                                      |
| [Tabela de arquivos mestre](master-file-table.md)<br/>                       | Todas as informações sobre um arquivo, incluindo seu tamanho, carimbos de data e hora, permissões e conteúdo de dados, são armazenadas em entradas de MFT (tabela de arquivos mestre) ou em espaço fora do MFT que é descrito pelas entradas de MFT.<br/>                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência técnica de volumes e discos básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))
</dt> <dt>

[Referência técnica de volumes e discos dinâmicos](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))
</dt> <dt>

[Referência de gerenciamento de volume](volume-management-reference.md)
</dt> </dl>

 

