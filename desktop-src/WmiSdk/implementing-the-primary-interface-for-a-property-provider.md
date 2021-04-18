---
description: Um provedor de propriedades usa os métodos IWbemPropertyProvider como a interface primária para o WMI. Com o IWbemPropertyProvider, você pode implementar o código para recuperar e modificar as propriedades de classe e instância.
ms.assetid: d08c2ca4-9f8a-4a27-80fc-688d7c56f5eb
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 942117547380000e0da7d22a5e933cba4b3ffced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815568"
---
# <a name="implementing-the-primary-interface-for-a-property-provider"></a>Implementando a interface primária para um provedor de propriedades

Um provedor de propriedades usa os métodos [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) como a interface primária para o WMI. Com o **IWbemPropertyProvider**, você pode implementar o código para recuperar e modificar as propriedades de classe e instância.

A tabela a seguir lista os métodos [**IWbemPropertyProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbempropertyprovider) que você pode implementar para um provedor de propriedades.



| Método                                                   | Recurso      |
|----------------------------------------------------------|--------------|
| [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) | Recuperação    |
| [**PutProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) | Modification |



 

> [!Note]  
> Você deve implementar um provedor de propriedades como um provedor em processo. O WMI inicializará os provedores de propriedades gravados como serviços ou arquivos executáveis, mas nunca chamará seus métodos [**GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) e [**putProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-putproperty) .

 

Se você optar por não oferecer suporte a um desses métodos, seu provedor poderá fornecer uma implementação de stub que retorne o **\_ provedor WBEM E \_ \_ não \_ compatível**.

Um provedor de propriedades identifica uma classe ou instância gerenciada por um conjunto de três qualificadores: **PropertyContext**, **InstanceContext** e **ClassContext**. O WMI passará constantes de cadeia de caracteres descrevendo esses três qualificadores para seu provedor de propriedades.

Seu provedor de propriedades deve estar preparado para lidar com os seguintes tipos de qualificadores de contexto:

-   O qualificador **InstanceContext** é anexado a uma instância e contém informações que se aplicam a todas as propriedades na instância.
-   O qualificador **ClassContext** é anexado a uma classe e contém informações que se aplicam a todas as instâncias na classe. Por exemplo, em uma classe usada para armazenar dados fornecidos pelo provedor de registro, **ClassContext** pode ser o caminho para a chave do registro que contém as propriedades a serem relatadas.
-   O qualificador **PropertyContext** especifica informações específicas de contexto que pertencem à propriedade. Por exemplo, em uma classe usada para armazenar dados fornecidos pelo provedor de registro, **PropertyContext** especifica o nome do valor do registro a ser armazenado pela propriedade.

Esses qualificadores podem trabalhar juntos. Você pode designar um valor de **InstanceContext** e **PropertyContext** para informar ao provedor como tratar tipos específicos de instâncias. Por exemplo, talvez você queira marcar instâncias que o provedor reconhecerá como legível, mas tendo apenas uma propriedade gravável.

O qualificador mais comum usado é **PropertyContext**. Portanto, o WMI fornece o qualificador **DynProps** como um atalho. O WMI considera que cada propriedade em uma instância marcada com **DynProps** também tem os qualificadores **dinâmico**, [**Provider**](/windows/desktop/api/Provider/nl-provider-provider)e **PropertyContext** .

 

 



