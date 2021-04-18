---
description: A propriedade Resumo de palavras-chave em bancos de dados de instalação ou transformações contém uma lista de palavras-chave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propriedade de Resumo de palavras-chave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759218"
---
# <a name="keywords-summary-property"></a>Propriedade de Resumo de palavras-chave

A propriedade **Resumo de palavras-chave** em bancos de dados de instalação ou transformações contém uma lista de palavras-chave. As palavras-chave podem ser usadas por navegadores de arquivos para realizar pesquisas de palavra-chaves para um arquivo. Essa propriedade contém uma lista de fontes do patch em um pacote de patch.

Cabe ao autor de um banco de dados de instalação, transformação ou pacote de patch para fornecer o valor dessa propriedade nas informações de resumo. Os autores devem fazer o seguinte para determinar o valor correto.

-   Em um pacote de instalação, defina o valor dessa propriedade como uma lista de palavras-chave. A palavra-chave deve incluir "instalador", bem como palavras-chave específicas do produto, e pode ser localizada.
-   Em uma transformação, defina o valor dessa propriedade como uma lista de palavras-chave. A palavra-chave deve incluir "instalador", bem como palavras-chave específicas do produto, e pode ser localizada.
-   Em um pacote de patch, defina o valor dessa propriedade como uma lista delimitada por ponto-e-vírgula de locais de rede ou URL para as fontes do patch. Quando o patch é instalado, o instalador o adiciona à lista de origem do pacote de patch. Se o patch armazenado em cache se tornar ausente, o instalador poderá pesquisar uma origem no local original, um local adicionado à lista de origem pela propriedade **Resumo de palavras-chave** ou um local adicionado à lista de origem usando as funções [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) ou [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




