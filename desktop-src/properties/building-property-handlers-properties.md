---
description: As propriedades são representadas por IDs conhecidas como PIDs (identificadores de propriedade).
ms.assetid: a773c7b3-a1a2-4cce-ae5f-b54217ea06f4
title: Noções básicas sobre manipuladores de propriedade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42139a869551f0f4dc786f02c66c673a49495ba01f5258aeeff12051bd3f60b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119946966"
---
# <a name="understanding-property-handlers"></a>Noções básicas sobre manipuladores de propriedade

As propriedades são representadas por IDs conhecidas como PIDs (identificadores de propriedade). Cada propriedade DEVE ter um GUID (identificador global exclusivo). Esse identificador consiste em um GUID, que representa uma coleção de propriedades chamada conjunto de propriedades mais uma cadeia de caracteres ou um inteiro de 32 bits para identificar a propriedade dentro do conjunto. Se a forma de inteiro de ID for usada, os valores 0x00000000, 0xFFFFFFFF e 0xFFFFFFFE serão considerados inválidos. Os fornecedores podem garantir que suas propriedades sejam definidas exclusivamente colocando-as em um conjunto de propriedades definido por seus próprios GUIDs.

> [!IMPORTANT]
> É essencial que você defina propriedades com cuidado e estrategicamente para a primeira versão do esquema. As alterações nas propriedades personalizadas (como largura da coluna ou tipo de propriedade) não serão refletidas no banco de dados depois que um esquema tiver sido registrado. A única maneira de fazer com que essas alterações sejam reconhecidas depois que o esquema tiver sido registrado uma vez em um sistema seria recriar o índice e, em seguida, registrar o novo esquema ou registrar o esquema e, em seguida, criar uma nova propriedade (que consiste em um nome canônico e uma PKEY) para cada versão subequente; por `PKEY_GroupName_PropertyNameV2` exemplo, `PKEY_GroupName_PropertyNameV3` , e assim por diante). Não é recomendável criar novas propriedades dessa maneira, pois várias colunas diferentes podem afetar o desempenho do sistema.

 

Este tópico é organizado da seguinte forma:

-   [Metadados](#metadata)
    -   [Abrir metadados](#open-metadata)
-   [Sobre manipuladores de propriedades](#about-property-handlers)
-   [Tecnologia herdda](#legacy-technology)
-   [Tópicos relacionados](#related-topics)

## <a name="metadata"></a>Metadados

No Windows Vista e posterior, um novo sistema de propriedades baseado em metadados é central para organizar itens como arquivos, email e contatos. Nesse novo sistema de propriedades, os itens podem ser pesquisados com base em seus metadados e os usuários podem ler ou gravar esses metadados. Os metadados nesse sistema são representados por um conjunto extensível *de* propriedades implementadas como pares nome/valor.

No Windows Vista e posterior, um amplo conjunto de propriedades abrange as especificações de itens, como fotos, música, documentos, mensagens, contatos e arquivos. IsVs (fornecedores independentes de software) podem introduzir suas próprias propriedades para a plataforma se nenhuma propriedade existente atender às suas necessidades.

### <a name="open-metadata"></a>Abrir metadados

O sistema de propriedades no Windows Vista e posterior é um sistema de metadados aberto. Um formato de arquivo armazena qualquer propriedade atribuída a ela e expõe esse valor quando consultado, independentemente da relevância ou significado. Isso permite que desenvolvedores de terceiros anexem propriedades extras ao arquivo sem exigir uma alteração no manipulador de propriedades associado a ele. Os metadados abertos são um conceito poderoso. Para obter mais informações sobre como dar suporte a metadados abertos para um formato de arquivo baseado em XML, consulte "Dando suporte a metadados abertos" em [Inicializando manipuladores de propriedades](./building-property-handlers-property-handlers.md).

> [!Note]  
> Manipuladores de propriedades sempre estão associados a tipos de arquivo específicos; portanto, se o formato de arquivo contiver propriedades que exigem um manipulador de propriedades personalizado, você sempre deverá registrar uma extensão de nome de arquivo exclusiva para cada formato de arquivo.

 

## <a name="about-property-handlers"></a>Sobre manipuladores de propriedades

No Windows Vista e posterior, o Windows tem um sistema de propriedades extensível para armazenar e recuperar metadados nos arquivos e itens de dados que você acessa. Windows O Explorer e o Windows Search, juntamente com outros aplicativos, usam manipuladores de propriedade para ler e modificar os metadados. Se você for um desenvolvedor proprietário de um tipo de arquivo específico, deverá registrar um manipulador de propriedades para dar ao sistema de propriedades acesso aos metadados em seus arquivos. Em alguns casos, você pode usar um manipulador de propriedades existente que pode ler e entender seu formato de arquivo e suas propriedades; em outros casos, talvez seja necessário desenvolver um novo manipulador de propriedades para o tipo de arquivo.

A primeira etapa na escrita de um manipulador de propriedades é considerar quais propriedades o tipo de arquivo dá suporte. Os valores de propriedade são armazenados no fluxo de arquivos, principalmente para habilitar a capacidade de transporte. Quando os valores de propriedade são armazenados no próprio arquivo, como estão nesse sistema, um usuário pode copiar um arquivo para outro computador, uma unidade flash USB ou outro sistema de arquivos ou envia o arquivo como um anexo de email, as propriedades viajam com o arquivo e nunca ficam fora de sincronia ou perdidas. Portanto, se o formato de arquivo dá suporte ao armazenamento de informações extras, é melhor armazenar as propriedades no próprio arquivo.

A próxima etapa é determinar quais propriedades o arquivo deve fornecer. Inicialmente, você pode achar que um conjunto limitado de propriedades é adequado. Um arquivo de áudio pode dar suporte apenas a propriedades relacionadas a áudio e terminar lá. No entanto, esse arquivo de áudio pode ser uma gravação de uma sessão de uma corte de direito, arquivada por um escritório de advocacia. Nesse caso, a empresa de advocacia certamente deseja associar outras propriedades que não são de áudio a esse arquivo, como o número do caso. O provedor do formato de arquivo de áudio não pode determinar todos os cenários em que seu formato será usado. Portanto, eles devem considerar a habilitação do armazenamento em memória de qualquer propriedade arbitrária com suporte pelo sistema de propriedades.

## <a name="legacy-technology"></a>Tecnologia herdda

A tecnologia de fluxo secundário do NTFS (Sistema de Arquivos do Microsoft Windows NT) foi desenvolvida para dar suporte à persistência de informações extras com o arquivo por meio de um fluxo alternativo definido na camada do sistema de arquivos. Pode-se perguntar por que esses fluxos secundários não são usados como o método principal para armazenar propriedades, especialmente com suporte a metadados abertos. O principal motivo é a capacidade de transporte dessas informações extras. Infelizmente, esses fluxos alternativos são removidos em muitos cenários, incluindo o CSC (suporte a cache do lado do cliente), o envio de arquivos como anexos e a cópia de arquivos para um armazenamento não NTFS.

Os fluxos secundários não fornecem uma solução robusta na qual as propriedades têm a garantia de viajar com o arquivo e, portanto, o sistema de propriedades Windows Vista não fornece um mecanismo interno que explora os fluxos NTFS secundários para armazenamento de propriedades. ISVs também são altamente desacentados de criar manipuladores de propriedade que usam fluxos secundários para o armazenamento de propriedades. É claro que há cenários em que os fluxos secundários NTFS são apropriados, especialmente quando os aplicativos podem garantir que o arquivo com o qual eles estão lidando seja sempre armazenado em um volume NTFS e não viajarão como resultado da interação do usuário final.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando nomes de tipo](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[Usando listas de propriedades](./building-property-handlers-property-lists.md)
</dt> <dt>

[Inicializando manipuladores de propriedades](./building-property-handlers-property-handlers.md)
</dt> <dt>

[Registrando e distribuindo manipuladores de propriedade](./prophand-reg-dist.md)
</dt> <dt>

[Práticas recomendadas e perguntas frequentes do manipulador de propriedades](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
