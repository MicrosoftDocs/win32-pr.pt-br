---
description: Nas informações resumidas de um pacote de instalação, a propriedade Resumo da Contagem de Palavras indica o tipo de imagem do arquivo de origem.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Propriedade Resumo da Contagem de Palavras
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0eb167c50db0894ea658bb93b97bfb9f49362d32cca8976a2ea3ec590b716450
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145229"
---
# <a name="word-count-summary-property"></a>Propriedade Resumo da Contagem de Palavras

Nas informações resumidas de um pacote de instalação, a propriedade Resumo da Contagem de **Palavras** indica o tipo de imagem do arquivo de origem. Se essa propriedade não estiver presente, o padrão será zero (0).

Essa propriedade é um campo de bits. Novos bits podem ser adicionados no futuro. No momento, os bits a seguir estão disponíveis.



| bit   | Valor          | Descrição                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Nomes de arquivo longos. Nomes de arquivo curtos.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | A origem está descompactada. A origem é compactada.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | A origem é a mídia original. Source é uma imagem administrativa criada por uma instalação administrativa.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Privilégios elevados podem ser necessários para instalar esse pacote. Privilégios elevados não são necessários para instalar esse pacote.<br/> Disponível a partir do Windows Installer versão 4.0 e Windows Vista ou Windows Server 2008.<br/> |



 

Eles são combinados para dar à **propriedade Resumo** da Contagem de Palavras um dos valores a seguir que indicam um tipo de imagem de arquivo de origem.



| Valor | Type                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Origem original usando nomes de arquivo longos. Corresponde à árvore na [Tabela de Diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar esse pacote.                                                                                                                                     |
| 1     | Origem original usando nomes de arquivo curtos. Corresponde à árvore na [Tabela de Diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar esse pacote.                                                                                                                                    |
| 2     | Arquivos de origem compactados usando nomes de arquivo longos. Corresponde a gabinetes e arquivos na Tabela [de Mídia](media-table.md). Privilégios elevados podem ser necessários para instalar esse pacote.                                                                                                                   |
| 3     | Arquivos de origem compactados usando nomes de arquivo curtos. Corresponde a gabinetes e arquivos na Tabela [de Mídia](media-table.md). Privilégios elevados podem ser necessários para instalar esse pacote.                                                                                                                  |
| 4     | Imagem administrativa usando nomes de arquivo longos. Corresponde à árvore na [Tabela de Diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar esse pacote.                                                                                                                                |
| 5     | Imagem administrativa usando nomes de arquivo curtos. Corresponde à árvore na [Tabela de Diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar esse pacote.                                                                                                                               |
| 8     | Privilégios elevados não são necessários para instalar esse pacote. Use esse valor ao [autorizar pacotes sem a caixa de diálogo UAC](authoring-packages-without-the-uac-dialog-box.md). Disponível a partir do Windows Installer versão 4.0 e Windows Vista ou Windows Server 2008.<br/> |



 

Observe que, se o pacote estiver marcado como compactado (Bit 1 está definido), o instalador do Windows instalará apenas arquivos localizados na raiz da origem. Nesse caso, até mesmo os arquivos [](file-table.md) marcados como descompactados na Tabela de Arquivos devem estar localizados na raiz a ser instalada. Para especificar uma imagem de origem que tenha um arquivo de gabinete (arquivos compactados) e arquivos descompactados que corresponderem à árvore na Tabela de [Diretórios](directory-table.md), marque o pacote como descompactado deixando o Bit 1 [](file-table.md) descompactado (value=0) na propriedade Resumo de Contagem de **Palavras** e de definir **msidbFileAttributesCompressed** (value=16384) na coluna Atributos da Tabela de Arquivos para cada arquivo no gabinete.

Em uma transformação, a **propriedade Resumo da Contagem de** Palavras deve ser Null.

No fluxo de informações resumidas  de um pacote de patch, a propriedade Resumo da Contagem de Palavras indica a versão mínima Windows do Instalador necessária para instalar o patch.



| Valor | Significado                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | O valor padrão, que indica que MSPATCH foi usado para criar o patch.                                                                                                        |
| 2     | Requer no mínimo Windows Installer 1.2 para que o patch seja aplicado. Um patch com uma Contagem de Palavras de "2" falhará imediatamente se for usado com uma versão do Windows Installer anterior à 1.2. |
| 3     | Requer no mínimo Windows Instalador 2.0 para que o patch seja aplicado. Um patch com uma Contagem de Palavras de "3" falhará imediatamente se for usado com uma versão do Windows Installer anterior à 2.0. |
| 4     | Requer no mínimo Windows Instalador 3.0 para que o patch seja aplicado. Um patch com uma Contagem de Palavras de "4" falhará se for usado com uma versão do Windows Installer anterior à 3.0.             |
| 5     | Requer no mínimo Windows Instalador 3.1 para que o patch seja aplicado.                                                                                                               |



 

Essa propriedade de resumo é REQUIRED.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições da propriedade Summary](summary-property-descriptions.md)
</dt> </dl>

 

 




