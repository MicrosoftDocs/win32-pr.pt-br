---
description: Benefícios do MUI explicado
ms.assetid: 5b9851e0-4354-4088-b099-0f5f5fac4a35
title: Benefícios do MUI explicado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971f66ef7fc094912e87d7e9ab77284fecb0931d9222e6910931b281b6308286
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829692"
---
# <a name="benefits-of-mui-explained"></a>Benefícios do MUI explicado

-   [Benefícios do MUI para desenvolvedores](#mui-benefits-for-developers)
-   [Benefícios do MUI para empresas](#mui-benefits-for-enterprises)
-   [Benefícios do MUI para OEMs](#mui-benefits-for-oems)

## <a name="mui-benefits-for-developers"></a>Benefícios do MUI para desenvolvedores

Há muitas maneiras possíveis de implementar uma solução MUI em aplicativos, mas cada possibilidade é uma variação de um dos três métodos básicos:

1.  Compilar um binário (com recursos internos) para cada idioma. Esse é o padrão *de fato* para aplicativos herdados, pois esse é o modelo primário com suporte das ferramentas de desenvolvimento padrão, como o Microsoft Visual Studio. Esse modelo requer vários binários para vários idiomas e tem limitações em relação à implantação de imagem única e a cenários multilíngues. deve-se observar que os aplicativos desenvolvidos com esse modelo continuarão a funcionar no Windows Vista, e são fornecidas ferramentas que ajudam os desenvolvedores a passarem desse modelo para o modelo mais moderno descrito no terceiro método.
2.  Ter um binário de núcleo com neutralidade de idioma com uma DLL (biblioteca de vínculo dinâmico) de recursos de vários idiomas. Esse modelo é definitivamente compatível com MUI, mas dificulta a atualização dos binários de recursos para acomodar novos idiomas. Suponha que, além do inglês, francês e japonês, você também queira dar suporte a alemão. Um binário de recursos totalmente novo precisaria ser fornecido e implantado para seus usuários que talvez não precisem necessariamente de alemão.
3.  Ter um binário de núcleo com neutralidade de idioma com um conjunto de DLLs de recurso por idioma. essa é a maneira como o próprio sistema operacional é implementado no Windows Vista, e os desenvolvedores são incentivados a usar esse modelo para aplicativos, pois ele oferece mais do que os dois modelos anteriores.

antes da versão Windows Vista, a falta de suporte interno para esse último modelo tornou difícil a adoção. No entanto, isso mudou, e os benefícios desse modelo são numerosos e tornam um excelente modelo para seus aplicativos:

-   os aplicativos podem se tornar multilíngues e podem se comportar da mesma maneira que Windows Vista, fornecendo uma experiência de linguagem de exibição consistente para os usuários.
-   A flexibilidade é aumentada na liberação de idiomas adicionais para um aplicativo. Idiomas adicionais podem ser liberados independentemente do código principal, o que significa que o suporte para novos idiomas pode ser adicionado ao longo do tempo, conforme necessário.
-   O custo é reduzido na criação e manutenção de mais versões de idioma.
-   Os OEMs e as empresas podem integrar facilmente os aplicativos à imagem de seu PC globalizado — prontos para serem entregues a diferentes países.
-   ferramentas e diretrizes que ajudam você a migrar seu aplicativo para o modelo de MUI do Windows Vista estão disponíveis. Em particular, o MSDN fornece um [conjunto significativo de documentação](multilingual-user-interface.md) sobre o MUI.

## <a name="mui-benefits-for-enterprises"></a>Benefícios do MUI para empresas

O MUI oferece dois benefícios principais para as empresas:

-   Instalação de imagem única: o MUI permite que as empresas distribuam, ofereçam suporte e mantenham a mesma imagem em todo o mundo (ou qualquer parte dela) com uma única instalação. Windows O vista estende a distribuição de imagem única do sistema operacional, para que os aplicativos de negócios também possam ser implantados como parte da mesma imagem.
-   Suporte para áreas de trabalho multilíngues: vários pacotes de idiomas de interface do usuário localizados podem ser instalados em uma área de trabalho, o que permite que vários usuários compartilhem um único desktop e ainda usem seus próprios idiomas de interface do usuário preferenciais. Isso também se aplica a computadores públicos, que precisam de tratamento igual para todos os idiomas oficialmente falados (como pode ser o caso no Canadá e na União Europeia) e em computadores compartilhados para usuários móveis.

## <a name="mui-benefits-for-oems"></a>Benefícios do MUI para OEMs

O principal benefício dos OEMs é a instalação de imagem única que o MUI habilita, pois torna possível criar imagens que contêm todos os idiomas necessários para direcionar uma zona geográfica com eficiência e atrasar a escolha da linguagem na instalação inicial do computador do usuário. Em particular, isso permite um gerenciamento mais eficaz do inventário para OEMs.

ao fornecer suporte ao MUI para aplicativos, o Windows Vista também permite que os OEMs forneçam aplicativos de valor agregado em suas imagens, aproveitando a instalação de uma única imagem, desde que esses aplicativos estejam habilitados para o MUI.

 

 



