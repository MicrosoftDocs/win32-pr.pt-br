---
description: 'Saiba mais sobre: JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d4a7433b6e2882a90c9c6fdfe0180b5f5ab7a8e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476872"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_coltyp"></a>JET_COLTYP

O **JET_COLTYP** de constantes descreve todos os tipos de coluna possíveis que podem ser encontrados em uma tabela.


| <p>Constante/valor</p> | <p>Descrição</p> | 
|-----------------------|--------------------|
| <p>JET_coltypNil<br />0</p> | <p>Um tipo de coluna inválido.</p> | 
| <p>JET_coltypBit<br />1</p> | <p>Um tipo de coluna que permite três valores: <strong>True,</strong> <strong>False</strong>ou <strong>NULL.</strong> Esse tipo de coluna tem um byte de comprimento e é um tamanho fixo. <strong>False</strong> classifica antes <strong>de True.</strong> Observe que o tamanho desse tipo não combina com o tamanho do tipo booliana variante.</p> | 
| <p>JET_coltypUnsignedByte<br />2</p> | <p>Um inteiro sem sinal de 1 byte que pode assumir valores entre 0 (zero) e 255.</p> | 
| <p>JET_coltypShort<br />3</p> | <p>Um inteiro com sinal de 2 byte que pode assumir valores entre -32768 e 32767. Valores negativos são classificação antes de valores positivos.</p> | 
| <p>JET_coltypLong<br />4</p> | <p>Um inteiro com sinal de 4 byte que pode assumir valores entre 2147483648 e 2147483647. Valores negativos são classificação antes de valores positivos.</p> | 
| <p>JET_coltypCurrency<br />5</p> | <p>Um inteiro com sinal de 8 byte que pode assumir valores entre 9223372036854775808 e 9223372036854775807. Valores negativos são classificação antes de valores positivos. Esse tipo de coluna é idêntico ao tipo de moeda variante. Esse tipo de coluna também pode ser usado como um inteiro com sinal de 8 byte nativo.</p> | 
| <p>JET_coltypIEEESingle<br />6</p> | <p>Um número de ponto flutuante de precisão simples (4 byte).</p> | 
| <p>JET_coltypIEEEDouble<br />7</p> | <p>Um número de ponto flutuante de precisão dupla (8 byte).</p> | 
| <p>JET_coltypDateTime<br />8</p> | <p>Um número de ponto flutuante de precisão dupla (8 byte) que representa uma data em dias fracionados desde o ano 1900. Esse tipo de coluna é idêntico ao tipo de data variante.</p> | 
| <p>JET_coltypBinary<br />9</p> | <p>Um comprimento fixo ou variável, coluna binária bruta que pode ter até 255 bytes de comprimento.</p><p>Esse tipo de coluna pode ser usado para implementar um GUID se configurado como uma coluna binária de 16 byte de comprimento fixo. A única ressalva é que a ordenação relativa de valores em um índice sobre tal coluna não corresponderá à ordenação relativa da renderização padrão de cadeia de caracteres do Registro de um GUID (ou seja, "{ 0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}").</p> | 
| <p>JET_coltypText<br />10</p> | <p>Uma coluna de texto de comprimento fixo ou variável que pode ter até 255 caracteres ASCII de comprimento ou 127 caracteres Unicode de comprimento.</p><p>Todas as cadeias de caracteres são armazenadas como um número contado de caracteres. As cadeias de caracteres não precisam ser terminadas em nulo. Além disso, não é necessário que a contagem inclua um terminador nulo. Por fim, os caracteres nulos inseridos podem ser armazenados.</p><p>Cadeias de caracteres ASCII são sempre tratadas como não diferenciando maiúsculas de minúsculas para fins de classificação e pesquisa. Além disso, somente os caracteres que precedem o primeiro caractere nulo (se algum) são considerados para classificação e pesquisa.</p><p>As cadeias de caracteres Unicode usam a API do Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> para criar chaves de classificação que são posteriormente usadas para classificar e pesquisar esses dados. Por padrão, as cadeias de caracteres Unicode são consideradas na localidade em inglês dos EUA e são classificação e pesquisadas usando os seguintes sinalizadores de normalização: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH. No Windows 2000, é possível personalizar esses sinalizadores por índice para também incluir NORM_IGNORENONSPACE. No Windows XP e versões posteriores, é possível solicitar qualquer combinação dos seguintes sinalizadores de normalização por índice: LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH e SORT_STRINGSORT.</p><p>Em todas as versões, é possível personalizar a localidade por índice. Qualquer localidade pode ser usada desde que o pacote de idiomas apropriado tenha sido instalado no computador. Por fim, todos os caracteres nulos encontrados em uma cadeia de caracteres Unicode são completamente ignorados.</p> | 
| <p>JET_coltypLongBinary<br />11</p> | <p>Um comprimento fixo ou variável, coluna binária bruta que pode ter até 2147483647 bytes de comprimento. Esse tipo é considerado um Valor Longo. Um Valor Longo é especial porque pode ser grande e porque pode ser acessado como um fluxo. Esse tipo é idêntico ao JET_coltypBinary.</p> | 
| <p>JET_coltypLongText<br />12</p> | <p>Uma coluna de texto fixa ou variável que pode ter até 2147483647 caracteres ASCII de comprimento ou 1073741823 caracteres Unicode de comprimento. Esse tipo é considerado um Valor Longo. Um Valor Longo é especial porque pode ser grande e porque pode ser acessado como um fluxo. Esse tipo é idêntico ao JET_coltypText.</p> | 
| <p>JET_coltypSLV<br />13</p> | <p>Esse tipo de coluna está obsoleto.</p> | 
| <p>JET_coltypUnsignedLong<br />14</p> | <p>Um inteiro sem sinal de 4 byte que pode assumir valores entre 0 (zero) e 4294967295.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, Windows Server 2008 e versões posteriores.</p> | 
| <p>JET_coltypLongLong<br />15</p> | <p>Um inteiro com sinal de 8 byte que pode assumir valores entre 9223372036854775808 e 9223372036854775807. Valores negativos são classificação antes de valores positivos.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, Windows Server 2008 e versões posteriores.</p> | 
| <p>JET_coltypGUID<br />16</p> | <p>Uma coluna binária de 16 byte de comprimento fixo que representa de forma nativa o tipo de dados GUID. Os valores de coluna GUID são classificação da mesma maneira que esses valores classificariam como cadeias de caracteres quando em formato padrão (ou seja, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, Windows Server 2008 e versões posteriores.</p> | 
| <p>JET_coltypUnsignedShort<br />17</p> | <p>Um inteiro sem sinal de 2 byte que pode assumir valores entre 0 e 65535.</p><p><strong>Windows Vista e Windows Server 2008:</strong>  Esse tipo de coluna tem suporte no Windows Vista, Windows Server 2008 e versões posteriores.</p> | 
| <p>JET_coltypMax<br />18</p> | <p>Uma constante que descreve o máximo (ou seja, um que não é o maior número de colunas válido) com suporte no mecanismo.</p><p>Esse valor deve ser usado com cuidado porque ele será alterado à medida que novos tipos de coluna forem suportados. por exemplo, ele tem um valor literal diferente em Windows 2000 do que no Windows XP e versões posteriores.</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
