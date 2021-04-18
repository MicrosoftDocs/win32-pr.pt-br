---
description: Decoder-Specific entradas do registro
ms.assetid: 64ef260a-ed7f-4253-a644-bd3352b0ee41
title: Decoder-Specific entradas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17485e7adca62abd31643d84d371a0002724ea9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785946"
---
# <a name="decoder-specific-registry-entries"></a>Decoder-Specific entradas do registro


Além das entradas de Registro necessárias para todos os codificadores e decodificadores, as seguintes entradas de registro são necessárias especificamente para decodificadores.

Essas entradas registram seu decodificador na categoria de decodificadores do Windows Imaging Component (WIC). O primeiro GUID nessas entradas é o identificador de categoria (CATID) para [**WICBitmapDecoders**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

```
HKEY_CLASSES_ROOT
   CLSID
      {7ED96837-96F0-4812-B211-F13C24117ED3}
         Instance
            {Decoder CLSID}
               CLSID = {Decoder CLSID}
               FriendlyName = {Name of Decoder}
```

Como observado na seção [descoberta e arbitragem](-wic-howwicworks.md) de como funciona o Windows Imaging Component, o mecanismo que permite que um decodificador apropriado para uma imagem específica seja descoberto em tempo de execução é baseado na correspondência de um padrão de identificação inserido no arquivo de imagem com um padrão especificado na entrada de registro do decodificador. Para habilitar a descoberta em tempo de execução de decodificadores, você deve registrar o padrão de identificação exclusivo para o formato de imagem da seguinte maneira. Todas essas entradas de registro são necessárias, exceto a entrada **EndOfStream** , que é opcional, conforme descrito na tabela a seguir.

```
HKEY_CLASSES_ROOT
   CLSID
      {Decoder CLSID}
         Patterns
            {0}
               Position = Offset in block
               Length = Length of pattern
               Pattern = Pattern to match
               Mask = FF FF FF FF
               EndOfStream = 0|1
```



| Valor       | Descrição                                                                                                                                                                                                                                                                                                                     |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posição    | O deslocamento no arquivo onde o padrão pode ser encontrado.                                                                                                                                                                                                                                                                        |
| Comprimento      | O comprimento do padrão.                                                                                                                                                                                                                                                                                                      |
| Padrão     | Os bits reais que compõem o padrão. Esses são os bits que correspondem ao padrão de identificação em um arquivo de imagem durante a descoberta.                                                                                                                                                                                |
| Mask        | Permite valores curinga em padrões. A máscara é aplicada pela execução de uma operação AND lógica no padrão e na máscara. Qualquer bit no padrão que corresponda a um bit na máscara com um valor de 0 é ignorado.                                                                                                       |
| EndOfStream | O deslocamento do padrão de identificação deve ser calculado a partir do final do fluxo, em vez do início. Alguns formatos de imagem colocam o padrão de identificação no final do arquivo ou próximo dele. Como o padrão é buscar desde o início, a menos que o padrão esteja próximo do final do arquivo, você pode omitir essa entrada. |



 

Um codec pode dar suporte a mais de um padrão de identificação. Nesse caso, você repetiria todas as chaves em padrões de **\_ classe HKEY \_ \\ \\ {Decoder CLSID} \\ Patterns** e usará a chave numérica (0 no exemplo) para distinguir entre os diferentes padrões. Você deve incluir cada um dos quatro valores na chave para cada padrão.

## <a name="registering-a-container-format-with-metadata-readers"></a>Registrando um formato de contêiner com leitores de metadados

Se você criar um novo formato de contêiner para o codec, também deverá criar entradas de registro para dar suporte à descoberta de leitores de metadados para os blocos de metadados em suas imagens, assim como você fez para os gravadores de metadados. As entradas a seguir precisam ser criadas no identificador de classe (CLSID) do leitor de metadados para cada formato de metadados com suporte no formato de contêiner. (Observe que, se o seu codec usar um contêiner TIFF, então essa informação já estará no registro.)

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Reader CLSID}
         Containers
            {Container Format GUID}
               
                  Position = Offset relative to its container
                  Pattern = Pattern used for metadata header
                  Mask = FF FF FF FF
                  DataOffset = Offset from beginning of header
```

Como as entradas para leitores de metadados também são usadas para descoberta, elas são muito semelhantes às entradas para decodificadores. Essas entradas são usadas pela fábrica de componentes para localizar os leitores de metadados com suporte no seu contêiner e para selecionar o apropriado, quando sua implementação de [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) solicitar um leitor de metadados.



| Valor      | Descrição                                                                                                                                                                                                                                                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posição   | O deslocamento no contêiner do bloco de metadados onde o cabeçalho de metadados pode ser encontrado. Para blocos de metadados de nível superior, esse é o deslocamento no fluxo de arquivos. Para blocos de metadados aninhados em outros blocos de metadados, é o deslocamento relativo ao bloco de metadados recipiente. |
| Padrão    | Os bits reais que compõem o padrão. Esses são os bits que correspondem ao padrão de identificação em um arquivo de imagem durante a descoberta.                                                                                                                            |
| Mask       | O cabeçalho de metadados geralmente é definido pelo manipulador de metadados. Você deve usar o cabeçalho de metadados padrão para cada leitor, a menos que, por algum motivo, o padrão deva ter um formato diferente em seu contêiner.                                                          |
| DataOffset | O deslocamento do início do cabeçalho de metadados no qual os dados reais começam. Nos casos em que os metadados não estão localizados em um deslocamento específico do cabeçalho, essa entrada pode ser omitida.                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Entradas de registro específicas do codificador](-wic-encoderregentries.md)
</dt> <dt>

[Integração com a Galeria de fotos do Windows e o Windows Explorer](-wic-integrationregentries.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



