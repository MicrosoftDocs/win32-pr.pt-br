---
title: Objetos COM e estruturadas Armazenamento
description: Um dos usos atuais mais comuns de propriedades persistentes é usá-las para armazenar dados sobre um objeto do sistema, como um documento, com esse objeto.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- Objetos COM e estruturadas Armazenamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4c1405ddfaa060aa249090fc58b25b294a8c9aecc5f7b885d21b55bc162198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663586"
---
# <a name="com-objects-and-structured-storage"></a>Objetos COM e estruturadas Armazenamento

Um dos usos atuais mais comuns de propriedades persistentes é usá-las para armazenar dados sobre um objeto do sistema, como um documento, com esse objeto. É claro que há o potencial de armazenar propriedades com qualquer objeto, como uma impressora, portanto, só seria necessário verificar suas propriedades para determinar seu local, seu tipo e assim por diante. Um objeto de usuário pode ter um conjunto de propriedades que inclui dados como Nome, Sobrenome, Office e Telefone. Os aplicativos podem ser escritos para consultar um conjunto de objetos em todo o sistema com base em suas propriedades, por exemplo, exibindo todas as impressoras localizadas em um determinado prédio. No entanto, os sistemas atuais usam com mais frequência propriedades em documentos.

O padrão de conjunto de propriedades primário definido por COM é [The Summary Information Property Set](the-summary-information-property-set.md). Esse conjunto de propriedades é simples e comumente usado. A maioria dos documentos criados por aplicativos tem um conjunto comum de atributos úteis para os usuários desses documentos. Esses atributos incluem o nome do autor do documento, o assunto do documento, quando ele foi criado e assim por diante. Dois outros conjuntos de propriedades são definidos para Microsoft Office 95, Office 97 e posterior. Esses são o conjunto de propriedades Resumo do Documento COM e o conjunto de propriedades User-Defined propriedades. Para obter mais informações, consulte [Structured Armazenamento Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

No Windows 3.1, cada aplicativo tinha uma maneira diferente de armazenar esses dados em seus documentos. Para examinar as informações resumidas de um determinado documento, o usuário precisava executar o aplicativo que criou o documento, abri-lo e invocar a caixa de diálogo Informações de Resumo do aplicativo, para que somente o aplicativo pudesse exibir suas informações resumidas.

Os conjuntos de propriedades COM e as interfaces do conjunto de propriedades possibilitam ver as propriedades do documento sem executar o aplicativo de criação. Por exemplo, todas as versões do Microsoft Word 6.0 ou posterior e muitos outros aplicativos habilitados para COM agora salvam seus documentos usando o armazenamento estruturado com COM e o padrão de conjunto de propriedades descrito aqui. Portanto, outros aplicativos do Office Suite podem exibir The [Summary Information Property Set](the-summary-information-property-set.md) para esse arquivo, desde que esse arquivo seja um arquivo de armazenamento estruturado COM e o aplicativo de criação salvou as informações no formato Conjunto de Propriedades COM. O shell Windows 95 ou Windows 98, por exemplo, usa isso e permite que o usuário final ex veja as propriedades de qualquer documento do Word 6.0 ou posterior diretamente do shell.

Para usar conjuntos de propriedades de outros aplicativos, os outros aplicativos devem reconhecer como interpretar as propriedades em um conjunto de propriedades, o que implica um padrão. O COM tem estabelecido essa abordagem definindo um conjunto de propriedades padrão, o Conjunto de Propriedades de Informações de Resumo COM. Qualquer aplicativo que tenha a definição desse conjunto de propriedades pode acessar facilmente as informações resumidas contidas em qualquer documento criado por um aplicativo COM que usa essa especificação de conjunto de propriedades.

 

 




