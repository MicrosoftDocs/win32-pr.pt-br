---
description: Uma família de imagens é um grupo de uma ou mais imagens atualizadas de um produto que foram atualizadas para a versão mais recente.
ms.assetid: 06a77b35-b593-47e6-9083-46a6b65b7481
title: Tabela ImageFamilies (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ece99e3c42626eb2155f16f2198703dc31b682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921202"
---
# <a name="imagefamilies-table-patchwizdll"></a>Tabela ImageFamilies (Patchwiz.dll)

Uma família de imagens é um grupo de uma ou mais imagens atualizadas de um produto que foram atualizadas para a versão mais recente. Cada imagem atualizada pode pertencer a apenas uma família. Imagens atualizadas que pertencem a uma família de imagens compartilham um ou mais arquivos. Cada família de imagens tem seu próprio arquivo de gabinete no arquivo. msp que contém os patches binários e os novos arquivos necessários para atualizar as diferenças entre os arquivos de destino e atualizados. O arquivo de gabinete não replica os patches binários e os novos arquivos usados pelos arquivos compartilhados.

Uma tabela ImageFamilies contendo pelo menos um registro é necessária em cada banco de dados de criação de patch (arquivo. PCP). Essa tabela é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

A tabela ImageFamilies contém as informações de aplicação de patch que serão adicionadas à [tabela de mídia](media-table.md). Um patch adiciona uma entrada à tabela de mídia. Cada registro nas tabelas ImageFamilies refere-se a um grupo de imagens de produtos relacionadas que foram atualizadas para a versão mais recente do produto.

A tabela ImageFamilies tem as colunas a seguir. Um valor nulo pode ser usado nas colunas MediaSrcPropName, MediaDiskId e FileSequenceStart se o patch for aplicado com Windows Installer e Patchwiz.dll versão 2,0.



| Coluna            | Tipo    | Chave | Nullable |
|-------------------|---------|-----|----------|
| Família            | text    | S   | N        |
| MediaSrcPropName  | text    |     | S        |
| MediaDiskId       | Número inteiro |     | S        |
| FileSequenceStart | Número inteiro |     | S        |
| DiskPrompt        | text    |     | S        |
| VolumeLabel       | text    |     | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes
</dt> <dd>

O valor inserido neste campo é um identificador para um grupo de imagens de produtos relacionadas que foram atualizadas para a versão mais recente do produto. Limitado a um total de 8 caracteres alfanuméricos ou sublinhados. O instalador insere um fluxo de gabinete no arquivo de patch Windows Installer (arquivo. msp) para cada família na tabela. O gabinete contém os patches binários e os novos arquivos necessários para atualizar uma imagem de destino em uma imagem atualizada do produto. O instalador prefixa o nome da família com PCW \_ cab \_ para gerar o nome do fluxo do gabinete que ele insere no campo de gabinete da nova entrada da [tabela de mídia](media-table.md) .

</dd> <dt>

<span id="MediaSrcPropName"></span><span id="mediasrcpropname"></span><span id="MEDIASRCPROPNAME"></span>MediaSrcPropName
</dt> <dd>

O valor inserido no campo de origem da nova entrada da [tabela de mídia](media-table.md) da imagem atualizada. Esse campo pode ser nulo somente se você estiver usando a versão 2,0 de Patchwiz.dll e se o MinimumRequiredMsiVersion na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) for definido como 200.

</dd> <dt>

<span id="MediaDiskId"></span><span id="mediadiskid"></span><span id="MEDIADISKID"></span>MediaDiskId
</dt> <dd>

O instalador insere esse valor no campo DiskId do novo registro da [tabela de mídia](media-table.md) . O valor de DiskId deve ser maior que qualquer DiskId atual no pacote de destino. O limite para MediaDiskId é 32767. Esse campo pode ser nulo somente se você estiver usando a versão 2,0 de Patchwiz.dll e se o MinimumRequiredMsiVersion na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) for definido como 200.

</dd> <dt>

<span id="FileSequenceStart"></span><span id="filesequencestart"></span><span id="FILESEQUENCESTART"></span>FileSequenceStart
</dt> <dd>

Esse campo é o número de sequência para o arquivo inicial. Esse mesmo número de sequência de arquivo não deve existir em dois patches para o mesmo produto. Para garantir isso, o valor nesse campo deve ser maior que todos os números de sequência usados em patches anteriores ou no pacote de instalação original. O maior número de sequência em um patch pode ser determinado pela adição do número total de entradas no arquivo de gabinete do patch ao número FileSequenceStart para esse patch. Uma maneira de determinar isso é examinar o arquivo. ddf gerado por [Patchwiz.dll](patchwiz-dll.md) durante a criação do patch. O limite para FileSequenceStart é 32767. Esse campo pode ser nulo somente se você estiver usando a versão 2,0 de Patchwiz.dll e se o MinimumRequiredMsiVersion na [tabela de Propriedades (Patchwiz.dll)](properties-table-patchwiz-dll-.md) for definido como 200.

</dd> <dt>

<span id="DiskPrompt"></span><span id="diskprompt"></span><span id="DISKPROMPT"></span>DiskPrompt
</dt> <dd>

O instalador insere esse valor no campo DiskPrompt do novo registro de [tabela de mídia](media-table.md) .

</dd> <dt>

<span id="VolumeLabel"></span><span id="volumelabel"></span><span id="VOLUMELABEL"></span>VolumeLabel
</dt> <dd>

O instalador insere esse valor no campo VolumeLabel do novo registro de mídia.

</dd> </dl>

## <a name="remarks"></a>Comentários

O patch adiciona o nome do gabinete no arquivo. msp ao campo de gabinete do novo registro adicionado à [tabela de mídia](media-table.md). Como é um gabinete inserido, o nome é prefixado com um \# caractere ' '. O patch adiciona uma propriedade ao campo de origem do novo registro na tabela de mídia. Dois patches não podem ter a mesma propriedade de origem.

Os arquivos compartilhados na família de imagens devem ter a mesma chave de tabela de arquivos em cada imagem atualizada da família. Todas as chaves de tabela de arquivo compartilhadas entre as imagens atualizadas devem representar o mesmo arquivo e devem ser idênticas em todas as imagens atualizadas. A chave de tabela de arquivo é o valor inserido na coluna arquivo da [tabela de arquivos](file-table.md).

O limite para MediaDiskId e FileSequenceStart é 32767. Para aumentar esse limite, exporte a tabela ImageFamilies para um arquivo. IDT com [Msidb.exe](msidb-exe.md) e altere o tipo de coluna de i2 para I4 ou de i2 para i4 e, em seguida, importe o arquivo. IDT de volta para o banco de dados. PCP. As transformações e os patches não podem ser criados entre dois pacotes com tipos de coluna diferentes.

 

 



