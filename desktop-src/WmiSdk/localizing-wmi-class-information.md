---
description: O WMI implementa uma técnica que permite que várias versões localizadas da mesma classe sejam armazenadas no repositório.
ms.assetid: 01e1cee5-d882-45b6-ac93-68533c2c6c9d
ms.tgt_platform: multiple
title: Localizando informações da classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3784128c48282d05620faf470217b195b26614d81b5b847e7a7a8ad6b9252f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131208"
---
# <a name="localizing-wmi-class-information"></a>Localizando informações da classe WMI

O WMI implementa uma técnica que permite que várias versões localizadas da mesma classe sejam armazenadas no repositório.

A definição de classe é separada nas seguintes versões:

-   Uma versão com neutralidade de idioma que contém apenas uma definição de classe básica.
-   Uma versão específica a um idioma que contém informações localizadas, como descrições de propriedades específicas de uma localidade.

As definições de classe específicas de idioma são armazenadas em um namespace filho sob o namespace que contém uma definição de classe básica neutra de linguagem.

Quando você solicita uma definição de classe localizada para uma localidade específica, o WMI combina a definição de classe básica e as informações de classe localizadas para formar uma classe localizada completa. Você pode obter uma versão localizada de uma classe WMI especificando uma localidade ao se conectar ao WMI e definindo um sinalizador que indica que você deseja informações localizadas. Em seguida, o WMI mescla as informações do idioma neutro e das versões específicas do idioma da definição de classe para formar uma classe localizada.

As classes WMI que contêm informações localizadas são marcadas com o qualificador de **emenda** e são chamadas de classes emendadas; uma classe oferece suporte a informações localizadas se tiver esse qualificador. Você pode determinar em qual localidade a classe foi localizada verificando outro qualificador chamado [**localidade**](swbemobjectpath-locale.md). o qualificador de localidade contém um identificador de localização (Windows LCID) que identifica uma localidade. Por exemplo, a localidade para o inglês americano é 0x409. Se um qualificador em uma classe corrigida contiver informações localizadas, ele conterá o tipo de qualificador **corrigido** .

A localização do WMI inclui as seguintes tarefas:

-   [Criando definições de classe localizadas](creating-localized-class-definitions.md)
-   [Compilando arquivos MOF localizados](compiling-localized-mof-files.md)
-   [Localizando valores de propriedade](localizing-property-values.md)
-   [Recuperando classes corrigidas](retrieving-amended-classes.md)

Para obter mais informações, consulte [Considerações sobre a classe corrigida](amended-class-considerations.md).

 

 



