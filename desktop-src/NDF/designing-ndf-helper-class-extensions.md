---
title: Criando extensões de classe auxiliar NDF
description: Este tópico destina-se a fornecer orientação genérica por meio do processo de desenvolvimento de extensão de classe auxiliar.
ms.assetid: f5dbd198-7d22-4e7e-830e-6753e9f4d6c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474a9f4ade01fe98a8db30568aa6a7c4978156d2c791747353071f020af27605
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802356"
---
# <a name="designing-ndf-helper-class-extensions"></a>Criando extensões de classe auxiliar NDF

Este tópico destina-se a fornecer orientação genérica por meio do processo de desenvolvimento de extensão de classe auxiliar. As diretrizes neste tópico se aplicam a todas as extensões de classe auxiliar. para obter diretrizes mais específicas, consulte [Windows classe de auxiliar extensível da plataforma de filtragem](windows-filtering-platform-extensible-helper-class.md) e [classes auxiliares extensível de diagnóstico sem fio 802,11](802-11-wireless-diagnostics-extensible-helper-classes.md).

## <a name="extending-ndf-functionality"></a>Estendendo a funcionalidade NDF

Windows O Vista e versões posteriores são fornecidos com uma variedade de classes auxiliares já implementadas que podem diagnosticar e reparar uma ampla gama de problemas. Às vezes, no entanto, desenvolvedores de terceiros talvez queiram estender essas classes auxiliares para diagnosticar e resolver problemas específicos de seus produtos e implementações particulares.

As seguintes classes auxiliares do NDF da Microsoft são extensíveis.

-   [Plataforma de filtragem do Windows](windows-filtering-platform-extensible-helper-class.md)
-   [Segurança sem fio](802-11-wireless-diagnostics-extensible-helper-classes.md)

## <a name="implementing-a-helper-class-extension"></a>Implementando uma extensão de classe auxiliar

A Microsoft envia duas interfaces que podem ser usadas para desenvolver extensões de classe auxiliar NDF.

A interface [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) é chamada por NDF para validar que ela tem todas as informações necessárias e que ela escolheu a classe auxiliar correta. Ele realiza isso por meio do método [**GetAttributeInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelperinfo-getattributeinfo) .

A interface [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) é chamada por NDF para a maioria das atividades que ocorrem durante o procedimento de diagnóstico. Vários de seus métodos são necessários, mas outros são opcionais para usos específicos.

Os métodos necessários incluem [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) e [**GetDiagnosticsInfo**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-getdiagnosticsinfo). As chamadas NDF são **inicializadas** para enviar parâmetros de chave para a extensão de classe auxiliar para inicializar seu estado de instância. O **GetDiagnosticsInfo** fornece uma estimativa de quanto tempo o diagnóstico pode levar e se requer representação do contexto do usuário original.

Outro método, [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth), é chamado para executar o diagnóstico no componente de rede correspondente à classe auxiliar. [**Cancelar**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cancel) é chamado quando o NDF determina um diagnóstico ou reparo contínuo deve ser interrompido. A [**limpeza**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-cleanup) permite que o NDF libere recursos do NDF que a extensão da classe auxiliar usou desde que a chamada para [**Initialize**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-initialize) foi feita.

Para obter informações sobre métodos adicionais, consulte [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper).

Extensões de classe auxiliar NDF são usadas para diagnosticar e resolver problemas de conectividade associados a um aplicativo ou componente específico. Eles também validam o êxito ou a falha de uma tentativa de resolução.

Os desenvolvedores que consideram a implementação de uma extensão de classe auxiliar devem executar as seguintes tarefas.

-   Identificar cenários de usuário em que as ações de diagnóstico e reparo são úteis.
-   Fornecer resoluções para problemas de conectividade frequentemente encontrados.
-   Se uma extensão de classe auxiliar for necessária, defina um modelo de integridade de componente usado para representar o estado de integridade do componente em NDF.

## <a name="identify-user-scenarios"></a>Identificar cenários de usuário

O teste e o uso de um aplicativo podem já ter fornecido padrões discerniis que uma extensão de classe auxiliar pode diagnosticar e possivelmente reparar. Os desenvolvedores de aplicativos podem usar esses dados para determinar os problemas de conectividade mais importantes para resolver e identificar os cenários de usuário nos quais os problemas de conectividade provavelmente ocorrerão.

Determinar a causa raiz de cada problema é vital nessa parte do processo. Isso pode exigir uma pesquisa extensiva, mas ajudará a criar um software muito mais fácil para os usuários e administradores usarem. Se uma causa raiz não for identificada, será difícil ou impossível oferecer a resolução de problemas usando a extensão de classe auxiliar.

## <a name="provide-resolutions"></a>Fornecer resoluções

Depois que uma equipe de desenvolvimento identificou as causas raiz dos problemas associados ao software, a próxima etapa é identificar as ações de resolução apropriadas para ajudar o usuário a resolver o problema o mais eficiente possível.

Nem todas as resoluções exigem que uma extensão de classe auxiliar ou uma ação automatizada seja criada. Em alguns casos, a equipe pode determinar que a melhor abordagem para resolver uma causa raiz é corrigir ou atualizar o componente, fornecer conteúdo de ajuda adicional para o componente ou desenvolver outras estratégias que forneçam melhores soluções de longo prazo.

Para problemas em que uma ação automatizada é ideal, a criação de uma extensão de classe auxiliar NDF é, em geral, uma excelente solução.

As extensões de classe auxiliar retornam informações sobre as causas raiz e reparam as informações aos usuários por meio do NDF. As cadeias de caracteres usadas para descrever as causas raiz e as informações de reparo devem ser simples e fáceis para que um usuário não técnico entenda. Para obter mais informações sobre essas cadeias de caracteres, consulte [diretrizes de interface do usuário para extensões de classe auxiliar NDF](user-interface-guidelines-for-ndf-helper-class-extensions.md).

## <a name="define-a-component-health-model"></a>Definir um modelo de integridade de componente

Os desenvolvedores de software devem definir níveis de "integridade" associados à capacidade de gerenciamento de problemas de rede. Um modelo de integridade usado para desenvolver classes auxiliares define apenas dois níveis de integridade: íntegros e não íntegros. Esses níveis também podem ser aplicados às extensões de classe auxiliar NDF.

Um componente íntegro indica uma ausência de problemas. Um componente pode ser considerado não íntegro devido a seus próprios problemas ou devido a problemas que ocorrem em outros componentes dos quais ele depende.



| Termo                                                                                                                             | Descrição                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span id="LowHealth"></span><span id="lowhealth"></span><span id="LOWHEALTH"></span>LowHealth<br/>                         | Esse estado indica um nível inaceitável de falhas desse componente e que o componente é o problema.<br/>    |
| <span id="LowHealth_Below"></span><span id="lowhealth_below"></span><span id="LOWHEALTH_BELOW"></span>LowHealth abaixo<br/> | Esse estado indica um nível inaceitável de falhas de um componente do computador local do qual esse componente depende.<br/> |



 

Quando o diagnóstico ocorre usando NDF, a extensão da classe auxiliar é solicitada uma série de perguntas para determinar seu estado de integridade. Se a extensão responder que ela não está íntegra, o NDF pedirá esclarecer perguntas, tentar diagnosticar o problema, sua localização e onde procurar em seguida. Cada classe auxiliar deve ser capaz de responder à questão de integridade baixa para direcionar melhor as atividades de diagnóstico apropriadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Classe auxiliar extensível da plataforma de filtragem](windows-filtering-platform-extensible-helper-class.md)
</dt> <dt>

[802,11 classes auxiliares extensíveis de diagnóstico sem fio](802-11-wireless-diagnostics-extensible-helper-classes.md)
</dt> </dl>

 

 





