---
description: Uma CRC (verificação de redundância cíclica) de arquivos está disponível com Windows Installer.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Verificação de CRC durante uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170666"
---
# <a name="crc-checking-during-an-installation"></a>Verificação de CRC durante uma instalação

Uma CRC (verificação de redundância cíclica) de arquivos está disponível com Windows Installer. A verificação de CRC é um mecanismo de verificação de erros semelhante a uma checksum, que permite que um aplicativo determine se as informações em um arquivo foram modificadas. Depois que o Windows Installer terminar de copiar um arquivo, ele obtém um valor de CRC dos arquivos de origem e de destino. O instalador verifica a CRC original carimbada no arquivo e a compara com a CRC calculada a partir da cópia. A verificação de CRC falhará se o valor de CRC original for não nulo e for diferente do CRC calculado na cópia. Se o CRC original for nulo, nenhuma verificação ocorrerá.

O Windows Installer faz uma verificação de CRC em um arquivo nos seguintes casos:

-   Se a [Propriedade MSICHECKCRCS](msicheckcrcs.md) for definida e **msidbFileAttributesChecksum** estiver incluído no campo atributos do registro do arquivo na [tabela de arquivos](file-table.md). O instalador faz a verificação de CRC uma vez após a instalação, duplicação ou movimentação do arquivo.
-   Se a [Propriedade MSICHECKCRCS](msicheckcrcs.md) for definida e **msidbFileAttributesChecksum** estiver incluído no campo atributos do registro do arquivo na [tabela de arquivos](file-table.md), o instalador fará uma verificação de CRC depois de aplicar o patch no arquivo.
-   Se o **msidbFileAttributesChecksum** for incluído no campo atributos do registro do arquivo na [tabela de arquivos](file-table.md), o instalador fará uma verificação de CRC antes de vincular as imagens.

Se a verificação falhar antes de associar uma imagem, o instalador relatará os dois erros a seguir no arquivo de log e continuará a instalação sem associar o arquivo.



| Código | Mensagem                                               |
|------|-------------------------------------------------------|
| 2941 | Não é possível computar o CRC para o arquivo \[ 2 \] .             |
| 2942 | A ação de BindImage não foi executada em \[ 2 \] arquivos. |



 

Se a verificação falhar depois que um arquivo descompactado tiver sido copiado, duplicado ou corrigido, o instalador relatará o erro a seguir. Esse erro também será relatado se a verificação falhar depois que um arquivo compactado for copiado. Se o arquivo tiver o atributo **msidbFileAttributesVital** , o arquivo será considerado vital para a instalação e o usuário obterá a opção de tentar novamente ou cancelar a instalação. Se o arquivo for marcado como não vital na coluna atributos da tabela de [arquivos](file-table.md), o usuário poderá ignorar o erro e continuar, repetir ou cancelar a instalação.



| Código | Mensagem                                         |
|------|-------------------------------------------------|
| 1331 | Falha ao copiar corretamente \[ o \] arquivo 2: erro de CRC. |



 

Observe que somente arquivos descompactados são movidos. Se a verificação falhar depois que um arquivo descompactado for movido, o instalador exibirá o erro a seguir. Se o arquivo tiver o atributo **msidbFileAttributesVital** , o arquivo será considerado vital para a instalação e a instalação falhará. Se o arquivo for marcado como não vital na coluna atributos da tabela de [arquivos](file-table.md), o usuário obterá a opção de cancelar ou ignorar o erro e continuar a instalação.



| Código | Mensagem                                         |
|------|-------------------------------------------------|
| 1332 | Falha ao mover corretamente \[ 2 \] arquivos: erro de CRC. |



 

Se a verificação falhar depois que um arquivo descompactado for corrigido, o instalador exibirá o erro a seguir. Se o arquivo tiver o atributo **msidbFileAttributesVital** , o arquivo será considerado vital para a instalação e a instalação falhará. Se o arquivo for marcado como não vital na coluna atributos da tabela de [arquivos](file-table.md), o usuário obterá a opção de cancelar ou ignorar o erro e continuar a instalação.



| Código | Mensagem                                          |
|------|--------------------------------------------------|
| 1333 | Falha ao corrigir corretamente \[ o \] arquivo 2: erro de CRC. |



 

 

 



