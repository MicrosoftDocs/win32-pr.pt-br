---
title: Visão geral das diretrizes de contêiner de controle e controle
description: Visão geral das diretrizes de contêiner de controle e controle
ms.assetid: c4cf2409-0085-43e6-afa2-f9c03cc50565
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd72851775898f4fd140c7d101d72993c34e3eb
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103639087"
---
# <a name="overview-of-control-and-control-container-guidelines"></a>Visão geral das diretrizes de contêiner de controle e controle

Um controle ActiveX é essencialmente um objeto OLE simples que dá suporte à interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Em geral, ele dará suporte a mais interfaces para oferecer funcionalidade, mas todas as interfaces adicionais podem ser exibidas como opcionais e, como tal, um contêiner de controle não deve depender de nenhuma interface adicional com suporte. Ao não especificar interfaces adicionais às quais um controle deve dar suporte, um controle pode direcionar com eficiência uma área específica de funcionalidade sem precisar dar suporte a interfaces específicas para se qualificar como um controle. Como sempre com OLE, seja em um controle ou em um contêiner de controle, nunca deve ser considerado que uma interface está disponível e as convenções de verificação de retorno padrão sempre devem ser seguidas. É importante que um contêiner controle ou controle seja degradado normalmente e ofereça funcionalidade alternativa se uma interface necessária não estiver disponível.

Um contêiner de controle ActiveX deve ser capaz de hospedar um controle ActiveX mínimo; Ele também dará suporte a várias interfaces adicionais, conforme especificado em [contêineres](containers.md). Há uma série de interfaces e métodos aos quais um contêiner pode, opcionalmente, dar suporte, que são agrupados em áreas funcionais conhecidas como *categorias de componentes*. Um contêiner pode dar suporte a qualquer combinação de categorias de componente, por exemplo, uma categoria de componente existe para a ligação de dados e um contêiner pode ou não oferecer suporte à funcionalidade de associação de dados, dependendo das necessidades de mercado do contêiner. Se um controle precisar de suporte a DataBinding de um contêiner para funcionar, ele inserirá esse requisito no registro. Isso permite que um contêiner de controle ofereça apenas para inserir os controles que ele sabe que ele pode hospedar com êxito. É importante observar que as categorias de componente são especificadas como parte do OLE e não são específicas para controles ActiveX, a arquitetura de controles usa categorias de componentes para identificar áreas de funcionalidades às quais um componente OLE pode dar suporte. As categorias de componente não são cumulativas ou exclusivas, portanto, um contêiner de controle pode dar suporte a uma categoria sem necessariamente dar suporte a outra.

É importante que os controles que exigem recursos opcionais ou recursos específicos para um determinado contêiner sejam claramente empacotados e comercializados com esses requisitos. Os contêineres da mesma forma que oferecem determinados recursos ou categorias de componentes devem ser comercializados e empacotados como oferecendo esses níveis de suporte ao hospedar controles ActiveX. É recomendável que o controle o destino e o teste com o máximo de contêineres possível e degradar normalmente para oferecer funcionalidade menor ou alternativa se as interfaces ou os métodos não estiverem disponíveis. Em uma situação em que um controle não pode executar sua função de trabalho designada sem o suporte de uma categoria de componente, essa categoria deve ser inserida como um requisito no registro para impedir que o controle seja inserido em um contêiner inadequado.

Essas diretrizes definem as interfaces e os métodos que um controle pode esperar que um contêiner de controle dê suporte, embora como sempre um controle deva verificar os valores de retorno ao usar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) ou outros métodos para obter ponteiros para essas interfaces. Um contêiner não deve esperar que um controle dê suporte a nada mais do que a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , e essas diretrizes identificam quais interfaces um controle pode dar suporte e qual significa a presença de uma interface específica.

## <a name="why-the-activex-control-and-control-container-guidelines-are-important"></a>Por que o controle ActiveX e as diretrizes de contêiner de controle são importantes

Os controles ActiveX se tornaram a principal arquitetura para o desenvolvimento de componentes de software programáveis para uso em vários contêineres diferentes, desde ferramentas de desenvolvimento de software até ferramentas de produtividade do usuário final. Para que um controle opere bem em uma variedade de contêineres, o controle deve ser capaz de assumir algum nível mínimo de funcionalidade sobre o qual ele pode depender em todos os contêineres.

Ao seguir essas diretrizes, os desenvolvedores de controle e de contêineres tornam seus controles e contêineres mais confiáveis e interoperáveis e, por fim, melhores e mais utilizáveis componentes para a criação de soluções baseadas em componentes.

## <a name="what-to-do-when-an-interface-you-need-is-not-available"></a>O que fazer quando uma interface que você precisa não está disponível

Os programas OLE devem usar [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para adquirir ponteiros de interface e devem verificar o valor de retorno. Os aplicativos OLE não podem pressupor com segurança que **QueryInterface** terá sucesso.

Esse requisito se aplica a todos os aplicativos OLE. Se a interface solicitada não estiver disponível (ou seja, [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) retorna E \_ nointerface), o controle ou o contêiner deverá degradar normalmente, mesmo que isso signifique que ele não pode executar sua função de trabalho designada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes de contêiner de controle e controle ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




