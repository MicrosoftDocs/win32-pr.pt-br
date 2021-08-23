---
description: A propriedade Resumo de Palavras-chave em bancos de dados de instalação ou em transformaçãos contém uma lista de palavras-chave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propriedade Resumo de Palavras-chave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a572161e440b440010d43f598e2baa453dbca514d71aa6f0f672deb7c726fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680306"
---
# <a name="keywords-summary-property"></a>Propriedade Resumo de Palavras-chave

A **propriedade Resumo de Palavras-chave** em bancos de dados de instalação ou em transformaçãos contém uma lista de palavras-chave. As palavras-chave podem ser usadas por navegadores de arquivos para fazer pesquisas de palavra-chave para um arquivo. Essa propriedade contém uma lista de fontes do patch em um pacote de patch.

É responsabilidade do autor de um pacote de banco de dados de instalação, transformação ou patch fornecer o valor dessa propriedade nas informações resumidas. Os autores devem fazer o seguinte para determinar o valor correto.

-   Em um pacote de instalação, de definido o valor dessa propriedade como uma lista de palavras-chave. A palavra-chave deve incluir "Instalador", bem como palavras-chave específicas do produto, e pode ser localizada.
-   Em uma transformação, de definido o valor dessa propriedade como uma lista de palavras-chave. A palavra-chave deve incluir "Instalador", bem como palavras-chave específicas do produto, e pode ser localizada.
-   Em um pacote de patch, defina o valor dessa propriedade como uma lista delimitada por ponto e vírgula de locais de rede ou URL para as fontes do patch. Quando o patch é instalado, o instalador os adiciona à lista de origem do pacote de patch. Se o patch armazenado em cache ficar ausente, o instalador poderá pesquisar uma origem no local original, um local adicionado à lista de origem pela propriedade **Resumo** de Palavras-chave ou um local adicionado à lista de origem usando as funções [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) ou [**MsiSourceListAddSourceEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições da propriedade Summary](summary-property-descriptions.md)
</dt> </dl>

 

 




