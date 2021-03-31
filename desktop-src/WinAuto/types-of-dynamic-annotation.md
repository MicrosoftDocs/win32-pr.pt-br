---
title: Tipos de anotação dinâmica
description: Há três tipos de anotação dinâmica com suporte na anotação direta do Microsoft Acessibilidade Ativa, anotação mapeada por valor e anotação de servidor. Cada tipo oferece vantagens específicas, portanto, é importante entender as diferenças.
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822638"
---
# <a name="types-of-dynamic-annotation"></a>Tipos de anotação dinâmica

Há três tipos de anotação dinâmica com suporte no Microsoft Acessibilidade Ativa: *anotação direta*, *anotação mapeada por valor* e *anotação de servidor*. Cada tipo oferece vantagens específicas, portanto, é importante entender as diferenças.

## <a name="direct-annotation"></a>Anotação direta

A anotação direta é a forma mais simples de anotação dinâmica. Ele é mais aplicável a elementos acessíveis cuja propriedade anotada não depende do estado do controle e não requer o suporte adicional fornecido pela anotação mapeada por valor e anotação de servidor. A anotação direta é usada para substituir o valor de uma ou mais propriedades do Microsoft Acessibilidade Ativa de um elemento acessível e para substituir ou adicionar uma propriedade de automação da interface do usuário da Microsoft ao controle. Todas as anotações feitas em uma propriedade do Microsoft Acessibilidade Ativa são refletidas na tradução de automação da interface do usuário, bem como no proxy de automação do Microsoft Acessibilidade Ativa para interface do usuário. Para obter mais informações, consulte [anotação direta](direct-annotation.md).

## <a name="value-map-annotation"></a>Anotação de mapa de valor

Além de anotar diretamente as propriedades do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , há muitas vezes uma necessidade de converter um valor específico do controle em uma cadeia de caracteres que pode ser compreendida por um usuário final. Um exemplo é o controle deslizante de resolução de tela na guia **configurações** da janela **Propriedades de exibição** (no **painel de controle**). Embora cada posição do controle deslizante corresponda a uma resolução diferente (por exemplo, 640 x 480, 1024 x 768), o controle não tem conhecimento dessa relação e não pode transmitir essas informações ao Microsoft Acessibilidade Ativa.

A anotação mapeada por valor facilita essa tarefa. Usando essa forma de anotação, você pode especificar cadeias de caracteres para valores de controle deslizante e especificar funções, Estados e descrições para ícones em exibições de lista e árvore. Para obter mais informações, consulte [anotação de mapa de valor](value-map-annotation.md).

## <a name="server-annotation"></a>Anotação do servidor

A anotação de servidor permite que os desenvolvedores registrem um objeto de retorno de chamada em solicitações de cliente de serviço para a propriedade anotada de um elemento. Esse objeto de retorno de chamada deve implementar a interface [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) e ser registrado com o Microsoft acessibilidade ativa Annotation Services. Depois de registrado, será solicitado que ele faça a manutenção de todas as solicitações do cliente para o valor da Propriedade do elemento acessível.

Um recurso particularmente útil de anotação do servidor é que um servidor pode ser registrado uma vez para lidar com solicitações de um contêiner e de todos os seus filhos. Portanto, por exemplo, um único servidor pode ser configurado uma vez para lidar com solicitações de todos os itens é uma caixa de listagem. Para obter mais informações, consulte [anotação do servidor](server-annotation.md).

 

 




