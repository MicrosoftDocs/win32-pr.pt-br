---
description: As seções a seguir descrevem como usar as propriedades internas do instalador e as propriedades adicionais definidas pelo autor do pacote.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Usando propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090476"
---
# <a name="using-properties"></a>Usando propriedades

As seções a seguir descrevem como usar as propriedades internas do instalador e as propriedades adicionais definidas pelo autor do pacote. As propriedades podem ser propriedades [públicas](public-properties.md) ou [privadas](private-properties.md). Cada propriedade que precisa ser definida na inicialização do instalador deve ter seu nome e o valor inicial listados na tabela de [Propriedades](property-table.md). Propriedades com um valor nulo não estão listadas na tabela de propriedades. Você pode obter ou definir propriedades de programas e ações personalizadas e definir propriedades públicas na linha de comando. O processo de instalação pode ser modificado usando propriedades em instruções condicionais.

[Restrições em nomes de propriedade](restrictions-on-property-names.md)

[Inicialização de valores de propriedade](initialization-of-property-values.md)

[Obtendo e definindo propriedades](getting-and-setting-properties.md)

[Usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md)

[Usando uma propriedade de diretório em um caminho](using-a-directory-property-in-a-path.md)

> [!Note]  
> Não use Propriedades para senhas ou outras informações que devam permanecer seguras. O instalador pode gravar o valor de uma propriedade criada na tabela de propriedades ou criado em tempo de execução em um log ou no registro do sistema.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[Referência de propriedade](property-reference.md)
</dt> </dl>

 

 



