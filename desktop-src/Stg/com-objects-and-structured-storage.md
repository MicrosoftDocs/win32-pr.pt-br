---
title: Objetos COM e armazenamento estruturado
description: Um dos usos atuais mais comuns das propriedades persistentes é usá-los para armazenar dados sobre um objeto do sistema, como um documento, com esse objeto.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- Objetos COM e armazenamento estruturado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a3d2fb9c145538bbd6b5e87dfcc9523feff78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363732"
---
# <a name="com-objects-and-structured-storage"></a>Objetos COM e armazenamento estruturado

Um dos usos atuais mais comuns das propriedades persistentes é usá-los para armazenar dados sobre um objeto do sistema, como um documento, com esse objeto. Há, é claro, o potencial de armazenar propriedades com qualquer objeto, como uma impressora, portanto, seria necessário apenas examinar suas propriedades para determinar seu local, seu tipo e assim por diante. Um objeto de usuário pode ter um conjunto de propriedades que inclui dados como nome, sobrenome, escritório e telefone. Os aplicativos podem ser gravados para consultar um conjunto de objetos em todo o sistema com base em suas propriedades, por exemplo, exibindo todas as impressoras localizadas em um determinado edifício. Os sistemas atuais, no entanto, usam com mais frequência as propriedades em documentos.

O padrão do conjunto de propriedades primária definido por COM é [o conjunto de propriedades de informações de resumo](the-summary-information-property-set.md). Esse conjunto de propriedades é simples e comumente usado. A maioria dos documentos criados por aplicativos tem um conjunto comum de atributos úteis para os usuários desses documentos. Esses atributos incluem o nome do autor do documento, o assunto do documento, quando ele foi criado e assim por diante. Dois outros conjuntos de propriedades são definidos para Microsoft Office 95, Office 97 e posterior. Esses são os conjuntos de propriedades de resumo do documento COM e a propriedade User-Defined propriedades definidas. Para obter mais informações, consulte [formato de conjunto de propriedades serializadas de armazenamento estruturado](structured-storage-serialized-property-set-format.md).

No Windows 3,1, cada aplicativo tinha uma maneira diferente de armazenar esses dados em seus documentos. Para examinar as informações resumidas de um determinado documento, o usuário tinha que executar o aplicativo que criou o documento, abri-lo e invocar a caixa de diálogo informações de resumo do aplicativo, para que apenas o aplicativo pudesse exibir suas informações de resumo.

Os conjuntos de propriedades COM e as interfaces do conjunto de propriedades possibilitam ver as propriedades do documento sem executar o aplicativo de criação. Por exemplo, todas as versões do Microsoft Word 6,0 ou posteriores e muitos outros aplicativos habilitados para COM agora salvam seus documentos usando o armazenamento estruturado COM e o padrão do conjunto de propriedades descrito aqui. Assim, outros aplicativos do Office Suite são capazes de exibir [o conjunto de propriedades de informações de resumo](the-summary-information-property-set.md) para tal arquivo, desde que esse arquivo seja um arquivo de armazenamento estruturado com, e o aplicativo de criação salvou as informações no formato de conjunto de propriedades com. O Shell do Windows 95 ou do Windows 98, por exemplo, usa isso e permite que o usuário final exiba as propriedades de qualquer documento do Word 6,0 ou posterior diretamente do Shell.

Para usar conjuntos de propriedades de outros aplicativos, os outros aplicativos devem reconhecer como interpretar as propriedades dentro de um conjunto de propriedades, o que implica um padrão. O COM pioneira essa abordagem definindo um conjunto de propriedades padrão, o conjunto de propriedades de informações de resumo COM. Qualquer aplicativo que tenha a definição desse conjunto de propriedades pode acessar facilmente as informações resumidas contidas em qualquer documento criado por um aplicativo COM que usa essa especificação de conjunto de propriedades.

 

 




