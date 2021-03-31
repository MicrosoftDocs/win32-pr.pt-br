---
description: Cada arquivo e diretório em um volume que dá suporte à compactação para arquivos e diretórios individuais tem um estado de compactação.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Estado de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169739"
---
# <a name="compression-state"></a>Estado de compactação

Cada arquivo e diretório em um volume que dá suporte à compactação para arquivos e diretórios individuais tem um *estado de compactação*.

Enquanto o atributo de compactação de um arquivo ou diretório indica simplesmente se o arquivo ou diretório está compactado ou não compactado, o estado de compactação também especifica o formato de todos os dados compactados.

Use o código de controle [**\_ obter \_ compactação fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) para determinar o estado de compactação de um arquivo ou diretório.

O estado de compactação é codificado como um valor de 16 bits. Um valor de estado de compactação de formato de COMPACTação \_ \_ None indica que um arquivo não está compactado. Um valor padrão de formato de COMPACTação \_ \_ indica que um arquivo está compactado, usando o formato de compactação padrão. Qualquer outro valor indica que um arquivo está compactado, usando o formato de compactação especificado pelo valor de estado de compactação.

Use o código de controle [**fsctl \_ set \_ Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) para definir o estado de compactação de um arquivo ou diretório. Essa operação também define o atributo de compactação do arquivo ou diretório.

Definir o estado de compactação de um arquivo para um valor diferente de zero compacta o arquivo, usando o formato de compactação codificado pelo valor do estado de compactação. Definir o estado de compactação de um arquivo como zero descompacta o arquivo. Essas são operações síncronas. O arquivo é compactado ou descompactado imediatamente quando você define seu estado de compactação.

Definir o estado de compactação de um diretório não causa nenhuma compactação ou descompactação imediata. Em vez disso, definir o estado de compactação de um diretório define um estado de compactação padrão que será fornecido a todos os arquivos e subdiretórios recém-criados.

 

 
