---
description: Códigos de controle usados com compactação e descompactação de arquivos e com pontos de reparse.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Códigos de controle de gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1354d1a4ce72f2867ece1f15218d9c7cb3f364a12ea3eb0d3b16f66b0954e89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755186"
---
# <a name="directory-management-control-codes"></a>Códigos de controle de gerenciamento de diretório

Os códigos de controle a seguir são usados com [compactação de arquivo e descompactação](file-compression-and-decompression.md).



| Código de controle                                             | Significado                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ GET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | Recupera o estado de compactação atual de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por fluxo.<br/>    |
| [**FSCTL \_ SET \_ COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | Define o estado de compactação de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por arquivo e por diretório.<br/> |



 

Os códigos de controle a seguir são usados com [pontos de reparse](reparse-points.md).

## <a name="in-this-section"></a>Nesta seção



| Código de controle                                                                   | Descrição                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**FSCTL \_ DELETE \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | Exclui um ponto de nova esparsa do arquivo ou diretório especificado.<br/>                                              |
| [**FSCTL \_ GET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | Recupera os dados de ponto de reparse associados ao arquivo ou diretório identificado pelo identificador especificado.<br/> |
| [**FSCTL \_ SET \_ REPARSE \_ POINT**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | Define um ponto de nova esparsa em um arquivo ou diretório.<br/>                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Códigos de controle de gerenciamento de arquivos](file-management-control-codes.md)
</dt> <dt>

[Códigos de controle de gerenciamento de volume](volume-management-control-codes.md)
</dt> </dl>

 

