---
title: Classificando componentes
description: Classificando componentes
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822868"
---
# <a name="classifying-components"></a>Classificando componentes

Embora um cliente possa navegar pela lista de CLSIDs no registro e selecionar um componente a ser usado, carregar cada componente no registro e consultá-lo para suas interfaces com suporte é muito demorado. Para determinar se um componente dá suporte às interfaces necessárias antes de criar uma instância do componente, um método para classificar os componentes em categorias foi desenvolvido.

Uma categoria de componente é um conjunto de interfaces que foram atribuídas a um GUID chamado CATID. Os componentes que implementam todas as interfaces em uma categoria de componente se registram como membros dessa categoria de componente. Os componentes que pertencem a uma determinada categoria de componente podem ser selecionados no registro. Ao se registrar como um membro de uma categoria de componente, o componente está garantindo que ele dê suporte a todas as interfaces de membro na categoria de componente.

Um componente pode ser membro de muitas categorias. Ele não está limitado a interfaces de suporte em uma categoria de componente. Ele pode dar suporte a qualquer interface, além daquelas em uma categoria de componente.

Ao contrário do registro padrão de componentes, nos quais os desenvolvedores devem escrever código que registra objetos manualmente, as categorias de componentes automatizam grande parte desse trabalho. Os seis métodos da interface [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definem categorias de componentes e registram objetos que as implementam ou exigem. O objeto do [Gerenciador de categorias de componentes](the-component-categories-manager.md) implementa essa interface. Consulte **ICatRegister** e [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) para obter informações adicionais sobre como usar categorias de componentes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 




