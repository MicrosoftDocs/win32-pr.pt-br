---
description: Uma CRC (Verificação de Redundância Cíclica) de arquivos está disponível com Windows Instalador.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Verificação de CRC durante uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b80a9b1900abf6c294911803df155a4c75025f5ad5ef01609af7345b0431e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379911"
---
# <a name="crc-checking-during-an-installation"></a>Verificação de CRC durante uma instalação

Uma CRC (Verificação de Redundância Cíclica) de arquivos está disponível com Windows Instalador. A verificação de CRC é um mecanismo de verificação de erro, semelhante a uma verificação de verificação, que permite que um aplicativo determine se as informações em um arquivo foram modificadas. Depois que Windows instalador terminar de copiar um arquivo, ele obtém um valor CRC dos arquivos de origem e de destino. O instalador verifica o CRC original carimbado no arquivo e compara isso com o CRC calculado da cópia. A verificação de CRC falhará se o valor CRC original não for nulo e for diferente do CRC calculado na cópia. Se o CRC original for nulo, nenhuma verificação ocorrerá.

O Windows instalador faz uma verificação de CRC em um arquivo nos seguintes casos:

-   Se a propriedade [MSICHECKCRCS](msicheckcrcs.md) estiver definida e **msidbFileAttributesChecksum** estiver incluído no campo Atributos do registro do arquivo na [tabela Arquivo](file-table.md). O instalador faz a verificação de CRC uma vez depois de instalar, duplicar ou mover o arquivo.
-   Se a propriedade [MSICHECKCRCS](msicheckcrcs.md) estiver definida e **msidbFileAttributesChecksum** estiver incluído no campo Atributos do registro do arquivo na tabela Arquivo [,](file-table.md)o instalador faz uma verificação de CRC depois de corrigir o arquivo.
-   Se **o msidbFileAttributesChecksum** estiver incluído no campo Atributos do registro do arquivo na tabela Arquivo [,](file-table.md)o instalador faz uma verificação de CRC antes de vincular imagens.

Se a verificação falhar antes de vincular uma imagem, o instalador relata os dois erros a seguir no arquivo de log e continua a instalação sem vincular o arquivo.



| Código | Mensagem                                               |
|------|-------------------------------------------------------|
| 2941 | Não é possível calcular o CRC para o \[ arquivo \] 2.             |
| 2942 | A ação BindImage não foi executada em \[ dois \] arquivos. |



 

Se a verificação falhar depois que um arquivo descompactado tiver sido copiado, duplicado ou a patch, o instalador relata o erro a seguir. Esse erro também será relatado se a verificação falhar depois que um arquivo compactado for copiado. Se o arquivo tiver o atributo **msidbFileAttributesVital,** o arquivo será considerado vital para a instalação e o usuário terá a opção de repetir ou cancelar a instalação. Se o arquivo for marcado como nãovital na coluna Atributos da tabela Arquivo [,](file-table.md)o usuário poderá ignorar o erro e continuar, tentar novamente ou cancelar a instalação.



| Código | Mensagem                                         |
|------|-------------------------------------------------|
| 1331 | Falha ao copiar corretamente \[ o arquivo \] 2: erro CRC. |



 

Observe que apenas arquivos descompactados são movidos. Se a verificação falhar depois que um arquivo descompactado for movido, o instalador exibirá o erro a seguir. Se o arquivo tiver o **atributo msidbFileAttributesVital,** o arquivo será considerado vital para a instalação e a instalação falhará. Se o arquivo for marcado como nãovital na coluna Atributos da tabela Arquivo [,](file-table.md)o usuário poderá cancelar ou ignorar o erro e continuar a instalação.



| Código | Mensagem                                         |
|------|-------------------------------------------------|
| 1332 | Falha ao mover \[ corretamente 2 \] arquivo: erro CRC. |



 

Se a verificação falhar depois que um arquivo descompactado for corrigida, o instalador exibirá o erro a seguir. Se o arquivo tiver o **atributo msidbFileAttributesVital,** o arquivo será considerado vital para a instalação e a instalação falhará. Se o arquivo for marcado como nãovital na coluna Atributos da tabela Arquivo [,](file-table.md)o usuário poderá cancelar ou ignorar o erro e continuar a instalação.



| Código | Mensagem                                          |
|------|--------------------------------------------------|
| 1333 | Falha ao corrigir corretamente \[ o arquivo \] 2: erro CRC. |



 

 

 



