---
description: Windows O instalador pode reparar, substituir e verificar arquivos contidos em um aplicativo. Uma reinstalação de aplicativo parcial ou completa poderá ser necessária se algum arquivo ou entrada de registro associado a qualquer recurso estiver ausente ou corrompido.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Reinstalando um recurso ou aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803fc3271cb69280ae84ae096e7a411dbf599f0a321bf15baac6dbd5ca8e1512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085996"
---
# <a name="reinstalling-a-feature-or-application"></a>Reinstalando um recurso ou aplicativo

Windows O instalador pode reparar, substituir e verificar arquivos contidos em um aplicativo. Uma reinstalação de aplicativo parcial ou completa poderá ser necessária se algum arquivo ou entrada de registro associado a qualquer recurso estiver ausente ou corrompido.

Quando um recurso ou aplicativo é reinstalado, todos os serviços, variáveis de ambiente e ações personalizadas que pertencem ao recurso ou ao aplicativo também são reinstalados. Observe que isso significa que qualquer alteração feita nas variáveis de ambiente entre a instalação original e a reinstalação será perdida.

A lista a seguir contém métodos de reinstalação de um recurso ou produto. Os dois primeiros métodos foram automatizados pelo instalador:

-   Repare, substitua ou verifique os arquivos chamando a função [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) .
-   Reinstale o produto inteiro chamando a função [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) .
-   Botão reinstalar, substituir ou verificar arquivos com um controle de interface do usuário do instalador por meio da [reinstalação do ControlEvent,](reinstall-controlevent.md).
-   Reinstale, substitua ou verifique os arquivos de uma linha de comando definindo a propriedade [**reinstalar**](reinstall.md) e a propriedade [**REINSTALLMODE**](reinstallmode.md) .

Para obter mais informações sobre como reinstalar um recurso ou aplicativo, consulte [resiliência](resiliency.md).

**Para reinstalar um produto usando o instalador**

-   Chame [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).

**Para reinstalar um recurso usando o instalador**

-   Chame [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).

**Para reinstalar um produto ou recurso com uma interface do usuário do instalador**

1.  Adicione um botão à caixa de diálogo especificada adicionando uma entrada à tabela de [controle](control-table.md).
2.  Adicione um [ControlEvent, REINSTALLMODE](reinstallmode-controlevent.md) à tabela ControlEvent,, com os campos de caixa de diálogo \_ e controle que \_ fazem referência ao controle de botão criado na etapa 1. No campo argumento, insira uma cadeia de caracteres que contém as letras correspondentes aos modos de reinstalação desejados (os valores aceitáveis para esse campo são idênticos aos aceitos para a propriedade [**REinstallmode**](reinstallmode.md) ). O valor na coluna de ordenação deste evento deve ser 1.
3.  Adicione um evento [REINSTALL ControlEvent,](reinstall-controlevent.md) à [tabela ControlEvent,](controlevent-table.md), novamente referenciando o mesmo controle de botão. O campo de argumento para esse evento normalmente será tudo, para forçar a reinstalação de todos os recursos, mas você pode posicionar o nome de um recurso específico aqui. O valor na coluna de ordenação deste evento deve ser 2.
4.  Adicione mais um evento vinculado ao mesmo controle de botão, para realmente iniciar a reinstalação. Isso pode ser um evento EndDialog (com um argumento de retorno). Em geral, no entanto, um evento NewDialog seria usado aqui para ir para uma caixa de diálogo de confirmação **que você deseja reinstalar?** . O valor na coluna ordenação desse evento deve ser 3.

    Se desejar, vários botões de [**reinstalação**](reinstall.md) podem ser criados para uma única caixa de diálogo, permitindo que o usuário selecione o tipo de reinstalação executada. Nesse caso, cada botão é criado conforme descrito no procedimento anterior, com um parâmetro [REINSTALLMODE ControlEvent,](reinstallmode-controlevent.md) diferente para cada botão.

Depois que um produto específico tiver sido instalado (com alguns ou todos os recursos do produto), uma reinstalação poderá ser executada na linha de comando:

**Para reinstalar um produto ou recurso de uma linha de comando**

1.  No prompt de comando, especifique a propriedade [**REINSTALL**](reinstall.md) .
2.  No prompt de comando, especifique a propriedade [**REinstallmode**](reinstallmode.md) .

    A especificação dessas propriedades permite que o usuário reinstale qualquer ou todos os recursos do produto. O tipo de reinstalação também pode ser especificado. Por exemplo, você pode especificar que apenas os arquivos que estão completamente ausentes devem ser reinstalados ou que somente arquivos corrompidos (por exemplo, qualquer arquivo executável cuja soma de verificação não corresponda ao conteúdo do arquivo real) sejam substituídos.

 

 



