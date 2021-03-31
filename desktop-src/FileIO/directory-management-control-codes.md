---
description: Códigos de controle usados com compactação e descompactação de arquivo e com pontos de nova análise.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Códigos de controle de gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829677"
---
# <a name="directory-management-control-codes"></a>Códigos de controle de gerenciamento de diretório

Os códigos de controle a seguir são usados com [compactação e descompactação de arquivo](file-compression-and-decompression.md).



| Código de controle                                             | Significado                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ obter \_ compactação**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Recupera o estado de compactação atual de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por fluxo.<br/>    |
| [**\_compactação do conjunto de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Define o estado de compactação de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por arquivo e por diretório.<br/> |



 

Os códigos de controle a seguir são usados com [pontos de nova análise](reparse-points.md).

## <a name="in-this-section"></a>Nesta seção



| Código de controle                                                                   | Descrição                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ excluir \_ ponto de nova análise \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Exclui um ponto de nova análise do arquivo ou diretório especificado.<br/>                                              |
| [**FSCTL \_ obter \_ ponto de nova análise \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Recupera os dados do ponto de nova análise associados ao arquivo ou diretório identificado pelo identificador especificado.<br/> |
| [**FSCTL \_ definir \_ ponto de nova análise \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Define um ponto de nova análise em um arquivo ou diretório.<br/>                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de controle de gerenciamento de arquivos](file-management-control-codes.md)
</dt> <dt>

[Códigos de controle de gerenciamento de volume](volume-management-control-codes.md)
</dt> </dl>

 

