---
description: Informações sobre o gerenciamento de arquivos.
ms.assetid: cf4e69b9-86dd-43a4-9011-6209fc65f550
title: Sobre o Gerenciamento de Arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2544d31ecb95029053987a3d64e80f4cdf8c0f3170b3a679b542e145ca262947
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766366"
---
# <a name="about-file-management"></a>Sobre o Gerenciamento de Arquivos

Os tópicos a seguir contêm mais informações sobre o gerenciamento de arquivos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                 | Descrição                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comparação de funcionalidades do sistema de arquivos](filesystem-functionality-comparison.md)<br/>            | Tabelas que listam as comparações de funcionalidade e recurso para os quatro sistemas de arquivos Windows principais, NTFS, exFAT, UDF e FAT32.<br/>                                                                           |
| [Arquivos e clusters](files-and-clusters.md)<br/>                                               | Um *arquivo* é uma unidade de dados no sistema de arquivos que um usuário pode acessar e gerenciar.<br/>                                                                                                                              |
| [Criando, excluindo e mantendo arquivos](creating--deleting--and-maintaining-files.md)<br/> | Funções a usar para criar, excluir e manter arquivos.<br/>                                                                                                                                                       |
| [Obtendo e configurando informações de arquivo](obtaining-and-setting-file-information.md)<br/>       | Funções a usar para obter e definir informações de arquivo.<br/>                                                                                                                                                             |
| [Lendo de e escrevendo em arquivos](reading-from-and-writing-to-files.md)<br/>                 | Um aplicativo lê e grava em um arquivo usando as funções [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx,**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) [**e WriteFileEx.**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)<br/> |
| [Vinculação de arquivo e diretório](file-and-directory-linking.md)<br/>                               | Há dois tipos de links com suporte no sistema de arquivos NTFS: [links rígidos e junções](hard-links-and-junctions.md).<br/>                                                                                     |
| [Bloquear clonagem](block-cloning.md)<br/>                                                         | Uma *operação de clonagem* de bloco instrui o sistema de arquivos a copiar um intervalo de bytes de arquivo em nome de um aplicativo.<br/>                                                                                                |
| [Compactação e descompactação de arquivos](file-compression-and-decompression.md)<br/>               | O sistema de arquivos NTFS usa Lempel-Ziv compactação, que é um algoritmo de compactação sem perda.<br/>                                                                                                                  |
| [Criptografia de Arquivo](file-encryption.md)<br/>                                                     | O EFS (Sistema de Arquivos Criptografado) fornece proteção criptográfica de arquivos individuais em volumes do sistema de arquivos NTFS usando um sistema de chave pública.<br/>                                                               |
| [Segurança de arquivos e direitos de acesso](file-security-and-access-rights.md)<br/>                     | Como os arquivos [são objetos](/windows/desktop/SecAuthZ/securable-objects)de segurança , o acesso a eles é regulamentado pelo modelo de controle de acesso que rege o acesso a todos os outros objetos que podem ser Windows.<br/>                     |
| [Entrada e saída (E/S)](input-and-output--i-o-.md)<br/>                                       | Windows fornece a capacidade de executar operações de E/S (entrada e saída) em componentes de armazenamento localizados em computadores locais e remotos.<br/>                                                                        |
| [Arquivos esparsos](sparse-files.md)<br/>                                                           | A compactação de arquivos que contêm principalmente zeros faz uso eficiente do espaço em disco.<br/>                                                                                                                        |
| [Links simbólicos](symbolic-links.md)<br/>                                                       | Um link simbólico é um objeto do sistema de arquivos que aponta para outro objeto do sistema de arquivos. O objeto que está sendo apontado é chamado de destino.<br/>                                                                          |



 

 

