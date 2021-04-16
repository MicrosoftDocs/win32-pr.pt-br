---
description: Nas informações resumidas de um pacote de instalação, a propriedade de resumo contagem de palavras indica o tipo de imagem de arquivo de origem.
ms.assetid: 1eeece25-4f24-4efe-879d-66ebbb6a9391
title: Propriedade de Resumo de contagem de palavras
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c4200cb946f6948770d0c900c2df651b8fbff11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747517"
---
# <a name="word-count-summary-property"></a>Propriedade de Resumo de contagem de palavras

Nas informações resumidas de um pacote de instalação, a propriedade de **Resumo contagem de palavras** indica o tipo de imagem de arquivo de origem. Se essa propriedade não estiver presente, o padrão será zero (0).

Essa propriedade é um campo de bits. Novos bits podem ser adicionados no futuro. No momento, os seguintes bits estão disponíveis.



| bit   | Valor          | Descrição                                                                                                                                                                                                                                      |
|-------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bit 0 | 0 1<br/> | Nomes de arquivo longos. Nomes de arquivo curtos.<br/>                                                                                                                                                                                                    |
| Bit 1 | 0 2<br/> | A origem é descompactada. A origem está compactada.<br/>                                                                                                                                                                                         |
| Bit 2 | 0 4<br/> | A origem é a mídia original. A origem é uma imagem administrativa criada por uma instalação administrativa.<br/>                                                                                                                                 |
| Bit 3 | 0 8<br/> | Privilégios elevados podem ser necessários para instalar este pacote. Privilégios elevados não são necessários para instalar este pacote.<br/> Disponível a partir do Windows Installer versão 4,0 e Windows Vista ou Windows Server 2008.<br/> |



 

Eles são combinados para dar à propriedade de **Resumo de contagem de palavras** um dos valores a seguir que indicam um tipo de imagem de arquivo de origem.



| Valor | Type                                                                                                                                                                                                                                                                                            |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Fonte original usando nomes de arquivo longos. Corresponde à árvore na [tabela de diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar este pacote.                                                                                                                                     |
| 1     | Fonte original usando nomes de arquivo curtos. Corresponde à árvore na [tabela de diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar este pacote.                                                                                                                                    |
| 2     | Arquivos de origem compactados usando nomes de arquivo longos. Corresponde a gabinetes e arquivos na [tabela de mídia](media-table.md). Privilégios elevados podem ser necessários para instalar este pacote.                                                                                                                   |
| 3     | Arquivos de origem compactados usando nomes de arquivo curtos. Corresponde a gabinetes e arquivos na [tabela de mídia](media-table.md). Privilégios elevados podem ser necessários para instalar este pacote.                                                                                                                  |
| 4     | Imagem administrativa usando nomes de arquivo longos. Corresponde à árvore na [tabela de diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar este pacote.                                                                                                                                |
| 5     | Imagem administrativa usando nomes de arquivo curtos. Corresponde à árvore na [tabela de diretórios](directory-table.md). Privilégios elevados podem ser necessários para instalar este pacote.                                                                                                                               |
| 8     | Privilégios elevados não são necessários para instalar este pacote. Use esse valor ao [criar pacotes sem a caixa de diálogo UAC](authoring-packages-without-the-uac-dialog-box.md). Disponível a partir do Windows Installer versão 4,0 e Windows Vista ou Windows Server 2008.<br/> |



 

Observe que, se o pacote for marcado como compactado (bit 1 é definido), o Windows Installer instalará apenas os arquivos localizados na raiz da origem. Nesse caso, até mesmo os arquivos marcados como não compactados na [tabela de arquivos](file-table.md) devem estar localizados na raiz a ser instalada. Para especificar uma imagem de origem que tenha um arquivo de gabinete (arquivos compactados) e arquivos descompactados que correspondam à árvore na [tabela de diretórios](directory-table.md), marque o pacote como descompactado deixando o bit 1 não definido (valor = 0) na propriedade de **Resumo contagem de palavras** e defina **msidbFileAttributesCompressed** (Value = 16384) na coluna atributos da [tabela de arquivos](file-table.md) para cada arquivo no gabinete.

Em uma transformação, a propriedade de **Resumo contagem de palavras** deve ser nula.

No fluxo de informações resumidas de um pacote de patch, a propriedade de **Resumo contagem de palavras** indica a versão de Windows Installer mínima necessária para instalar o patch.



| Valor | Significado                                                                                                                                                                              |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | O valor padrão, que indica que MSPATCH foi usado para criar o patch.                                                                                                        |
| 2     | Requer no mínimo Windows Installer 1,2 para que o patch seja aplicado. Um patch com uma contagem de palavras de "2" falhará imediatamente se for usado com uma versão Windows Installer anterior a 1,2. |
| 3     | Requer no mínimo Windows Installer 2,0 para que o patch seja aplicado. Um patch com uma contagem de palavras de "3" falhará imediatamente se for usado com uma versão Windows Installer anterior a 2,0. |
| 4     | Requer no mínimo Windows Installer 3,0 para que o patch seja aplicado. Um patch com uma contagem de palavras "4" falhará se for usado com uma versão Windows Installer anterior a 3,0.             |
| 5     | Requer no mínimo Windows Installer 3,1 para que o patch seja aplicado.                                                                                                               |



 

Essa propriedade de resumo é necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




