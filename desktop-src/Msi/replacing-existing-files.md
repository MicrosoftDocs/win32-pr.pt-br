---
description: Como a cópia de arquivo desnecessária reduz a instalação, o Windows Installer determina se o arquivo de chave do componente já está instalado antes de tentar instalar os arquivos de qualquer componente.
ms.assetid: 8be734c7-4f16-4f54-93db-bb8efb1ea6da
title: Substituindo arquivos existentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b3908749e5496e4be9bf0ff68c7038a9ea6573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828866"
---
# <a name="replacing-existing-files"></a>Substituindo arquivos existentes

Como a cópia de arquivo desnecessária reduz a instalação, o Windows Installer determina se o arquivo de chave do componente já está instalado antes de tentar instalar os arquivos de qualquer componente. Se o instalador encontrar um arquivo com o mesmo nome que o arquivo de chave do componente instalado no local de destino, ele compara a versão, a data e o idioma dos dois arquivos de chave e usa regras de controle de versão de arquivo para determinar se deseja instalar o componente fornecido pelo pacote. Se o instalador determinar que precisa substituir a base do componente no arquivo de chave, ele usará as regras de controle de versão de arquivo em cada arquivo instalado para determinar se deseja substituir o arquivo.

Observe que, ao criar um pacote de instalação com arquivos com versão, a cadeia de caracteres da versão na coluna versão da [tabela de arquivos](file-table.md) deve ser sempre idêntica à versão do arquivo incluído no pacote.

As regras de controle de versão de arquivo padrão podem ser substituídas ou modificadas usando a propriedade [**REinstallmode**](reinstallmode.md) . O instalador usa as regras de controle de versão de arquivo especificadas pela propriedade **REinstallmode** ao instalar, reinstalar ou reparar um arquivo. O exemplo a seguir mostra como o instalador aplica as [regras de controle de versão de arquivo](file-versioning-rules.md)padrão. O valor padrão da propriedade **REinstallmode** é "omus".

Os seguintes arquivos de chave de componente são instalados no sistema antes de o componente ser reinstalado.



| Arquivo                                    | Versão  | Data de criação | Data de modificação | Idioma    |
|-----------------------------------------|----------|-------------|---------------|-------------|
| FileA                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB                                   | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Arquiva                                   | 1.0.0000 | 1/1/99      | 1/2/99        | ENG         |
| Arquivo                                   | nenhum     | 1/1/99      | 1/1/99        | nenhum        |
| FileF (modificado > criado)<br/> | nenhum     | 1/1/99      | 1/2/99        | nenhum        |
| FileG                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileH                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| Arquivo                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN     |
| FileJ                                   | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, WINDOWS, EM |



 

Os seguintes arquivos de chave de componente estão incluídos no pacote do instalador.



| Arquivo                               | Versão  | Data de criação | Data de modificação | Idioma    |
|------------------------------------|----------|-------------|---------------|-------------|
| FileA (marcado mesmo)<br/>     | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB (versão anterior)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC (versão posterior)<br/>   | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Arquivado (versão posterior)<br/>   | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| Arquivo (marcado mesmo)<br/>     | nenhum     | 1/1/99      | 1/1/99        | nenhum        |
| FileF (novo arquivo)<br/>        | nenhum     | 1/3/99      | 1/3/99        | nenhum        |
| FileG (nova linguagem)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (nova linguagem)<br/>    | 1.0.0000 | 1/1/99      | 1/1/99        | EM, ENG, WINDOWS |
| Arquivo (mais idiomas)<br/>  | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (menos idiomas)<br/> | 1.0.0000 | 1/1/99      | 1/1/99        | Windows         |



 

Os arquivos de chave de componente a seguir permanecem no sistema depois que o componente é reinstalado. O estado do arquivo de chave determina o estado de quaisquer outros arquivos no componente.



| Arquivo                | Versão  | Data de criação | Data de modificação | Idioma    |
|---------------------|----------|-------------|---------------|-------------|
| Arquivo (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileB (original)    | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| FileC (substituição) | 2.0.0000 | 1/1/99      | 1/1/99        | ENG         |
| Arquivado (substituição) | 2.0.0000 | 12/31/98    | 1/10/99       | FRN         |
| Arquivo (substituição) | nenhum     | 1/1/99      | 1/1/99        | nenhum        |
| FileF (original)    | nenhum     | 1/1/99      | 1/2/99        | nenhum        |
| FileG (substituição) | 1.0.0000 | 1/1/99      | 1/1/99        | FRN         |
| FileH (substituição) | 1.0.0000 | 1/1/99      | 1/1/99        | EM, ENG, WINDOWS |
| Arquivoi (substituição) | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, FRN, SPN |
| FileJ (original)    | 1.0.0000 | 1/1/99      | 1/1/99        | ENG, WINDOWS, EM |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Verificação de CRC durante uma instalação](crc-checking-during-an-installation.md)
</dt> </dl>

 

 




