---
description: Se você optar por converter seus pacotes MTS em aplicativos COM+ manualmente ou permitir que o processo de instalação do Microsoft Windows faça isso automaticamente, você deve estar ciente dos resultados da conversão, bem como dos problemas.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Resultados e problemas de conversão COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a347df5f0ad0b16aee509c9c1b2c2c848372d0df2ccbc376814b0d14eb61d138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129208"
---
# <a name="com-conversion-results-and-issues"></a>Resultados e problemas de conversão COM+

Se você optar por converter seus pacotes MTS em aplicativos COM+ manualmente ou permitir que o processo de instalação do Microsoft Windows faça isso automaticamente, você deve estar ciente dos resultados da conversão, bem como dos problemas.

## <a name="what-is-converted"></a>O que é convertido

Durante a conversão, o utilitário MTSTOCOM converte funções, atribuições de função, interfaces, métodos, usuários, a lista de computadores e a maioria das configurações do computador. O utilitário MTSTOCOM também converte a identidade e a senha de um pacote MTS.

Os novos atributos COM+ que não estavam disponíveis no MTS são definidos automaticamente com os padrões a seguir para todos os componentes do MTS convertidos. Esses padrões podem ser alterados usando a ferramenta administrativa serviços de componentes ou as interfaces administrativas COM+.

-   Ativação JIT habilitada.
-   Pool de objetos desabilitado.
-   Sincronização igual à configuração transação.

## <a name="conversion-issues"></a>Problemas de conversão

O COM+ é instalado automaticamente quando você instala Windows. Não é possível desinstalar o COM+. Os problemas relacionados às atualizações de instalações MTS e COM+ existentes incluem o seguinte:

-   Se você estiver usando o MTS 1.0 no momento, o MTS será atualizado automaticamente para COM+. No entanto, os pacotes definidos pelo usuário serão perdidos e você deverá re-crie-os.
-   Se você estiver usando o MTS 2.0 no momento, o MTS será atualizado automaticamente para COM+. Todos os pacotes definidos pelo usuário serão atualizados para aplicativos COM+. Todos os componentes devem funcionar como no MTS 2.0.
-   Se você estiver usando o MTS 1.0 e o MTS 2.0 e tiver instalado a opção SDK, os arquivos do SDK serão removidos. Você pode instalar o SDK COM+ mais recente por meio do SDK do Microsoft Windows.
-   Você não pode gerenciar um computador MTS remoto de um computador COM+.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conversão automática do MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Conversão manual do MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de Administração do MTS](mts-administration-library.md)
</dt> </dl>

 

 



