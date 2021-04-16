---
description: Informações sobre o gerenciamento de arquivos.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Sobre o gerenciamento de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fe8e5f53a0021d4a6fba90a31698d05971e7bea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757859"
---
# <a name="about-file-management"></a>Sobre o gerenciamento de arquivos

Os tópicos a seguir contêm mais informações sobre o gerenciamento de arquivos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comparação de funcionalidade do sistema de arquivos](filesystem-functionality-comparison.md)<br/>            | Tabelas que listam comparações de suporte a funcionalidades e recursos para os quatro principais sistemas de arquivos do Windows, NTFS, exFAT, UDF e FAT32.<br/>                                                                           |
| [Arquivos e clusters](files-and-clusters.md)<br/>                                               | Um *arquivo* é uma unidade de dados no sistema de arquivos que um usuário pode acessar e gerenciar.<br/>                                                                                                                              |
| [Criando, excluindo e mantendo arquivos](creating--deleting--and-maintaining-files.md)<br/> | Funções a serem usadas para criar, excluir e manter arquivos.<br/>                                                                                                                                                       |
| [Obtendo e configurando informações do arquivo](obtaining-and-setting-file-information.md)<br/>       | Funções a serem usadas para obter e definir informações de arquivo.<br/>                                                                                                                                                             |
| [Lendo e gravando em arquivos](reading-from-and-writing-to-files.md)<br/>                 | Um aplicativo lê e grava em um arquivo usando as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)e [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .<br/> |
| [Vinculação de arquivos e diretórios](file-and-directory-linking.md)<br/>                               | Há dois tipos de links com suporte no sistema de arquivos NTFS: [links físicos e junções](hard-links-and-junctions.md).<br/>                                                                                     |
| [Bloquear clonagem](block-cloning.md)<br/>                                                         | Uma operação de *clonagem de bloco* instrui o sistema de arquivos a copiar um intervalo de bytes de arquivo em nome de um aplicativo.<br/>                                                                                                |
| [Compactação e descompactação de arquivos](file-compression-and-decompression.md)<br/>               | O sistema de arquivos NTFS usa a compactação Lempel-Ziv, que é um algoritmo de compactação sem perdas.<br/>                                                                                                                  |
| [Criptografia de Arquivo](file-encryption.md)<br/>                                                     | O EFS (sistema de arquivos criptografados) fornece proteção criptográfica de arquivos individuais em volumes do sistema de arquivos NTFS usando um sistema de chave pública.<br/>                                                               |
| [Segurança de arquivo e direitos de acesso](file-security-and-access-rights.md)<br/>                     | Como os arquivos são [objetos protegíveis](/windows/desktop/SecAuthZ/securable-objects), o acesso a eles é regulamentado pelo modelo de controle de acesso que governa o acesso a todos os outros objetos protegíveis no Windows.<br/>                     |
| [Entrada e saída (e/s)](input-and-output--i-o-.md)<br/>                                       | O Windows fornece a capacidade de executar operações de e/s (entrada e saída) em componentes de armazenamento localizados em computadores locais e remotos.<br/>                                                                        |
| [Arquivos esparsos](sparse-files.md)<br/>                                                           | A compactação de arquivos que contêm principalmente zeros faz uso eficiente do espaço em disco.<br/>                                                                                                                        |
| [Links simbólicos](symbolic-links.md)<br/>                                                       | Um link simbólico é um objeto do sistema de arquivos que aponta para outro objeto do sistema de arquivos. O objeto que está sendo apontado é chamado de destino.<br/>                                                                          |



 

 

