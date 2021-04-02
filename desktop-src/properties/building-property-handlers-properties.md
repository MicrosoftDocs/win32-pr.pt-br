---
description: As propriedades são representadas por IDs conhecidas como identificadores de propriedade (PIDs).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Noções básicas sobre manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 564d6f8bd325e649ff1356869932521d8c1cd885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165280"
---
# <a name="understanding-property-handlers"></a>Noções básicas sobre manipuladores de propriedade

As propriedades são representadas por IDs conhecidas como identificadores de propriedade (PIDs). Cada propriedade deve ter um GUID (identificador global exclusivo). Esse identificador consiste em um GUID, representando uma coleção de propriedades chamada um conjunto de propriedades, além de uma cadeia de caracteres ou um inteiro de 32 bits para identificar a propriedade dentro do conjunto. Se o formulário inteiro da ID for usado, os valores 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE serão considerados inválidos. Os fornecedores podem garantir que suas propriedades sejam definidas exclusivamente colocando-as em um conjunto de propriedades definido por seus próprios GUIDs.

> [!IMPORTANT]
> É fundamental que você defina as propriedades com cuidado e estrategicamente para a primeira versão do esquema. As alterações nas propriedades personalizadas (como a largura da coluna ou tipo de propriedade) não serão refletidas no banco de dados depois que um esquema tiver sido registrado. A única maneira de ter essas alterações reconhecidas depois que o esquema foi registrado uma vez em um sistema seria recriar o índice e, em seguida, registrar o novo esquema, ou registrar o esquema e, em seguida, criar uma nova propriedade (que consiste em um nome canônico e um PKEY) para cada versão do subequent; por exemplo `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` , e assim por diante). Não recomendamos a criação de novas propriedades dessa maneira, pois várias colunas estranhas podem afetar o desempenho do sistema.

 

Este tópico é organizado da seguinte maneira:

-   [Metadados](#metadata)
    -   [Abrir metadados](#open-metadata)
-   [Sobre manipuladores de propriedade](#about-property-handlers)
-   [Tecnologia herdada](#legacy-technology)
-   [Tópicos relacionados](#related-topics)

## <a name="metadata"></a>Metadados

No Windows Vista e posterior, um novo sistema de propriedades baseado em metadados é fundamental para organizar itens, como arquivos, email e contatos. Nesse novo sistema de propriedades, os itens podem ser pesquisados com base em seus metadados e os usuários podem ler ou gravar esses metadados. Os metadados nesse sistema são representados por um conjunto extensível de *Propriedades* implementadas como pares de nome/valor.

No Windows Vista e posterior, um amplo conjunto de propriedades aborda as especificidades de itens como fotos, música, documentos, mensagens, contatos e arquivos. ISVs (fornecedores independentes de software) podem introduzir suas próprias propriedades para a plataforma se nenhuma propriedade existente atender às suas necessidades.

### <a name="open-metadata"></a>Abrir metadados

O sistema de propriedades no Windows Vista e posterior é um sistema de metadados aberto. Um formato de arquivo armazena qualquer propriedade atribuída a ele e expõe esse valor quando consultado, independentemente da relevância ou significado. Isso permite que os desenvolvedores de terceiros anexem Propriedades extras ao arquivo sem a necessidade de uma alteração no manipulador de propriedades associado a ela. Os metadados abertos são um conceito poderoso. Para obter mais informações sobre como dar suporte a metadados abertos para um formato de arquivo baseado em XML, consulte "suporte a metadados abertos" em [inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md).

> [!Note]  
> Manipuladores de propriedade sempre são associados a tipos de arquivo específicos; Portanto, se o formato de arquivo contiver propriedades que exigem um manipulador de propriedade personalizada, você sempre deverá registrar uma extensão de nome de arquivo exclusiva para cada formato de arquivo.

 

## <a name="about-property-handlers"></a>Sobre manipuladores de propriedade

No Windows Vista e posterior, o Windows tem um sistema de propriedades extensível para armazenar e recuperar metadados nos arquivos e itens de dados que você acessa. O Windows Explorer e o sistema de pesquisa do Windows, juntamente com outros aplicativos, usam manipuladores de propriedade para ler e modificar esses metadados. Se você for um desenvolvedor que possui um tipo de arquivo específico, deverá registrar um manipulador de propriedades para dar ao sistema de propriedades acesso aos metadados em seus arquivos. Em alguns casos, você pode usar um manipulador de propriedades existente que possa ler e entender o formato de arquivo e suas propriedades; em outros casos, talvez seja necessário desenvolver um novo manipulador de propriedades para o tipo de arquivo.

A primeira etapa na escrita de um manipulador de propriedades é considerar as propriedades às quais o tipo de arquivo dá suporte. Os valores de propriedade são armazenados no fluxo de arquivos, principalmente para habilitar a transportabilidade. Quando os valores de propriedade são armazenados no próprio arquivo, como estão nesse sistema, um usuário pode copiar um arquivo para outro computador, uma unidade flash USB ou outro sistema de arquivos, ou enviar o arquivo como um anexo de email, as propriedades viajam com o arquivo e nunca saem da sincronização ou são perdidos. Portanto, se o formato de arquivo oferecer suporte ao armazenamento de informações extras, é melhor armazenar as propriedades no próprio arquivo.

A próxima etapa é determinar quais propriedades o arquivo deve fornecer. Inicialmente, você pode imaginar que um conjunto limitado de propriedades é adequado. Um arquivo de áudio pode dar suporte apenas a propriedades relacionadas a áudio e terminar. No entanto, esse arquivo de áudio pode ser uma gravação de uma sessão de um Tribunal de lei, arquivado por uma empresa jurídica. Nesse caso, a empresa jurídica certamente desejaria associar outras propriedades que não são de áudio a esse arquivo, como o número do caso. O provedor do formato de arquivo de áudio não pode, possivelmente, determinar todos os cenários nos quais seu formato nunca será usado. Portanto, eles devem considerar habilitar o armazenamento em aberto de qualquer propriedade arbitrária com suporte no sistema de propriedades.

## <a name="legacy-technology"></a>Tecnologia herdada

A tecnologia de fluxo secundário do sistema de arquivos do Microsoft Windows NT (NTFS) foi desenvolvida para dar suporte à persistência de informações extras com o arquivo por meio de um fluxo alternativo definido na camada do sistema de arquivos. Alguém pode estar imaginando por que esses fluxos secundários não são usados como o método Main para armazenar propriedades, especialmente com suporte a metadados abertos. O principal motivo é a transportabilidade dessas informações adicionais. Infelizmente, esses fluxos alternativos são removidos em vários cenários, incluindo o CSC (suporte de cache do lado do cliente), o envio de arquivos como anexos e a cópia de arquivos para um repositório não NTFS.

Os fluxos secundários não fornecem uma solução robusta em que as propriedades têm garantia de viajar com o arquivo e, portanto, o sistema de propriedades do Windows Vista não fornece um mecanismo interno que explora os fluxos NTFS secundários para o armazenamento de propriedades. Os ISVs também são altamente desencorajados de criar manipuladores de propriedade que usam fluxos secundários para o armazenamento de propriedades. É claro que há cenários em que os fluxos de NTFS secundários são apropriados, especialmente quando os aplicativos podem garantir que o arquivo com o qual estão lidando sempre seja armazenado em um volume NTFS e não se desloque como resultado da interação do usuário final.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando nomes de tipos](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedade](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
