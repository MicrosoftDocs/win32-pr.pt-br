---
description: Um aplicativo de gerenciamento que usa o provedor do Registro do Sistema pode definir classes com propriedades que representam dados do Registro para chaves específicas e, em seguida, armazena as classes no repositório WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definindo classes para o provedor de registro do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deecdbc419c5a245e609380732474a39089f28cb8c2fd76c2ac57546f2d00110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097286"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definindo classes para o provedor de registro do sistema

Um aplicativo de gerenciamento que usa o provedor do Registro do Sistema pode definir classes com propriedades que representam dados do Registro para chaves específicas e, em seguida, armazena as classes no repositório WMI. A maioria dos processos para definir uma classe para o registro do sistema é idêntica à definição de qualquer outra classe. No entanto, o provedor do Registro do Sistema exige que você use tipos de dados e qualificadores específicos.

O procedimento a seguir descreve como definir uma classe para o provedor do Registro do Sistema.

**Para definir uma classe para o provedor do Registro do Sistema**

1.  Crie a classe como faria com qualquer outra classe.

    Para obter mais informações, consulte [Criando uma classe](creating-a-class.md).

2.  Mapeie os tipos de dados do Registro apropriados para os tipos WMI apropriados.

    O provedor do Registro do Sistema mapeia os tipos de dados do Registro para tipos de dados WMI específicos. Para obter mais informações, consulte [Mapeando um tipo de dados do Registro para um tipo de dados WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Use os qualificadores necessários para definir o local do provedor do Registro e o local da chave do Registro apropriada.

    O provedor do Registro do Sistema usa três qualificadores para definir o local de várias classes, provedores e entradas do Registro. Para obter mais informações, [consulte Definindo uma classe do Registro com qualificadores](defining-a-registry-class-with-qualifiers.md).

 

 



