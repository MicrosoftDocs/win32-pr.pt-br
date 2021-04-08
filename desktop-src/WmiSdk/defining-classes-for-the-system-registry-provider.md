---
description: Um aplicativo de gerenciamento que usa o provedor de registro do sistema pode definir classes com propriedades que representam dados de registro para chaves específicas e, em seguida, armazena as classes no repositório do WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definindo classes para o provedor de registro do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922283"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definindo classes para o provedor de registro do sistema

Um aplicativo de gerenciamento que usa o provedor de registro do sistema pode definir classes com propriedades que representam dados de registro para chaves específicas e, em seguida, armazena as classes no repositório do WMI. A maioria dos processos para definir uma classe para o registro do sistema é idêntica à definição de qualquer outra classe. No entanto, o provedor de registro do sistema requer que você use tipos de dados e qualificadores específicos.

O procedimento a seguir descreve como definir uma classe para o provedor de registro do sistema.

**Para definir uma classe para o provedor de registro do sistema**

1.  Crie a classe como você faria com qualquer outra classe.

    Para obter mais informações, consulte [criando uma classe](creating-a-class.md).

2.  Mapeie os tipos de dados do registro apropriados para os tipos apropriados do WMI.

    O provedor de registro do sistema mapeia os tipos de dados do registro para tipos de dados específicos do WMI. Para obter mais informações, consulte [mapeando um tipo de dados do registro para um tipo de dados do WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Use os qualificadores necessários para definir o local do provedor de registro e o local da chave do registro apropriada.

    O provedor de registro do sistema usa três qualificadores para definir o local de várias classes, provedores e entradas de registro. Para obter mais informações, consulte [definindo uma classe de registro com qualificadores](defining-a-registry-class-with-qualifiers.md).

 

 



