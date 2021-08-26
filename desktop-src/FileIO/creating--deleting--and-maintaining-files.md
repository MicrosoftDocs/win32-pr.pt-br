---
description: Funções a usar para criar, excluir e manter arquivos.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Criando, excluindo e mantendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff20362e2ff5f1d8b01b515c7cbbb9fae250d930b2610c49c5e8aaeeabe7b401
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982116"
---
# <a name="creating-deleting-and-maintaining-files"></a>Criando, excluindo e mantendo arquivos

Os tópicos a seguir descrevem como criar, excluir e manter arquivos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                   | Descrição                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nomeando arquivos, caminhos e namespaces](naming-a-file.md)<br/>     | Regras, convenções e limitações de nomes para arquivos e diretórios, incluindo convenções de nomengo, nomes de arquivo curtos versus nomes de arquivo longos, caminhos totalmente qualificados versus caminhos relativos, limitação de comprimento máximo do caminho, nomes de arquivo 8.3 e namespaces.<br/>            |
| [Criando e abrindo arquivos](creating-and-opening-files.md)<br/> | Considerações para criar ou abrir um arquivo usando a [**função CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)<br/>                                                                                                                                                            |
| [Movendo e substituindo arquivos](moving-and-replacing-files.md)<br/> | Considerações para mover e substituir arquivos usando as funções CopyFileEx, CreateFile, Replacefile e MoveFileEx.<br/>                                                                                                                                        |
| [Fechando e excluindo arquivos](closing-and-deleting-files.md)<br/> | Para usar recursos do sistema operacional com eficiência, um aplicativo deve fechar arquivos quando eles não são mais necessários usando a [**função CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.<br/> |
| [Desfragmentando arquivos](defragmenting-files.md)<br/>               | *A desfragmentação* é o processo de mover partes de arquivos em um disco para desfragmentar arquivos, ou seja, o processo de mover clusters de arquivos em um disco para torná-los contíguos.<br/>                                                                               |



 

 

