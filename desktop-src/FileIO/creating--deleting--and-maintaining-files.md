---
description: Funções a serem usadas para criar, excluir e manter arquivos.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Criando, excluindo e mantendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787537"
---
# <a name="creating-deleting-and-maintaining-files"></a>Criando, excluindo e mantendo arquivos

Os tópicos a seguir descrevem como criar, excluir e manter arquivos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                   | Descrição                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Nomeando arquivos, caminhos e namespaces](naming-a-file.md)<br/>     | Regras, convenções e limitações de nomes para arquivos e diretórios, incluindo convenções de nomenclatura, nomes de arquivo curtos versus nomes de arquivo longos, caminhos totalmente qualificados versus caminhos relativos, limitação de comprimento de caminho máximo, nomes de arquivo 8,3 e namespaces.<br/>            |
| [Criando e abrindo arquivos](creating-and-opening-files.md)<br/> | Considerações para criar ou abrir um arquivo usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .<br/>                                                                                                                                                            |
| [Movendo e substituindo arquivos](moving-and-replacing-files.md)<br/> | Considerações para mover e substituir arquivos usando as funções CopyFileEx, CreateFile, ReplaceFile e MoveFileEx.<br/>                                                                                                                                        |
| [Fechando e excluindo arquivos](closing-and-deleting-files.md)<br/> | Para usar os recursos do sistema operacional com eficiência, um aplicativo deve fechar os arquivos quando eles não forem mais necessários usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.<br/> |
| [Desfragmentando arquivos](defragmenting-files.md)<br/>               | A *desfragmentação* é o processo de mover partes de arquivos em um disco para desfragmentar arquivos, ou seja, o processo de mover clusters de arquivos em um disco para torná-los contíguos.<br/>                                                                               |



 

 

