---
title: Alocação de IDs WinEvent
description: Cada WinEvent destina-se a ser usado apenas para uma finalidade específica. Usar um WinEvent para uma finalidade não intencional pode causar colisões com outros aplicativos ou o sistema operacional, o que pode fazer com que os aplicativos ou o sistema operacional se tornem instáveis.
ms.assetid: 956d6db4-f342-4b11-bfd9-92725284223f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f339641e5a3b679f572bc3b60c3e68be7b65f2a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779871"
---
# <a name="allocation-of-winevent-ids"></a>Alocação de IDs WinEvent

Cada WinEvent destina-se a ser usado apenas para uma finalidade específica. Usar um WinEvent para uma finalidade não intencional pode causar colisões com outros aplicativos ou o sistema operacional, o que pode fazer com que os aplicativos ou o sistema operacional se tornem instáveis.

A Microsoft definiu várias categorias diferentes de WinEvents e, para cada categoria, definiu um ou mais intervalos de valores para uso como IDs de WinEvent. O intervalo reservado da Comunidade (0xA000 — 0xAFFF) está disponível para aplicativos que precisam definir novas WinEvents. O uso de valores desse intervalo ajuda a reduzir o risco de colisões; no entanto, os desenvolvedores que criam novos WinEvents ainda precisam colaborar para evitar colisões entre seus aplicativos.

A tabela a seguir mostra as categorias WinEvent e os intervalos de valores definidos para cada categoria.



| Categoria                                                | Intervalo         | Em uso no momento | Comentários                                                                                        |
|---------------------------------------------------------|---------------|------------------|-------------------------------------------------------------------------------------------------|
| Eventos do Microsoft Acessibilidade Ativa (reservado pelo sistema) | 0x0001-0x00FF | 0x0001-0x0020    | \_IDs de \_ \* evento do sistema de eventos                                                                     |
| Eventos do Microsoft Acessibilidade Ativa (reservado pelo sistema) | 0x4001-0x40FF | 0x4001-0x4007    | \_IDs de \_ \* eventos do console de eventos                                                                    |
| Eventos de automação da interface do usuário (reservado pelo sistema)                  | 0x4E00-0x4EFF | 0x4E20-0x4E33    | IDs de evento de automação da interface do usuário                                                                         |
| Eventos de automação da interface do usuário (reservado pelo sistema)                  | 0x7500-0x75FF | 0x7530-0x759B    | Propriedade de automação da interface do usuário – IDs de evento de alteração                                                        |
| Eventos do Microsoft Acessibilidade Ativa (reservado pelo sistema) | 0x8000-0x80FF | 0x8000-0x8015    | \_IDs de \_ \* evento de objeto de evento                                                                     |
| OEM reservado                                            | 0x0101-0x01FF | 0x0101-0x0122    | IDs de evento IAccessible2                                                                          |
| Comunidade reservada                                      | 0xA000-0xAFFF | Nenhum             | Reservado para novos eventos definidos por especificações de AIA (Aliança de interoperabilidade de acessibilidade) |
| ATOM                                                    | 0xC000-0xFFFF | 0xC000-0xFFFF    | Reservado para eventos personalizados alocados em tempo de execução                                                 |



 

Os tópicos a seguir descrevem os intervalos de WinEvent mais detalhadamente.

## <a name="microsoft-active-accessibility-and-ui-automation-events"></a>Eventos da Microsoft Acessibilidade Ativa e de automação da interface do usuário

Cinco intervalos de IDs WinEvent são reservados para uso pelo Microsoft Acessibilidade Ativa e automação de interface do usuário da Microsoft. O primeiro intervalo (0x0001 — 0x00FF) é reservado para eventos de nível de sistema, normalmente usado para descrever situações que afetam todos os aplicativos no sistema. O segundo intervalo (0x4001 — 0x40FF) é reservado para eventos específicos do console do Windows. O terceiro (0x4E00 — 0x4EFF) e o quarto intervalo (0x7500 – 0x75FF) são para a reflexão dos eventos de automação da interface do usuário. Por fim, o quinto intervalo (0x8000 — 0x80FF) é para eventos de nível de objeto que pertencem a situações específicas para objetos dentro de um aplicativo.

Todos os eventos da Microsoft Acessibilidade Ativa e de automação da interface do usuário são definidos nos arquivos de cabeçalho WinUser. h e UIAutomationClient. h.

## <a name="oem-reserved-events"></a>Eventos reservados do OEM

O intervalo reservado do OEM é aberto para qualquer pessoa que precise usar o WinEvents como um mecanismo de comunicação. Os desenvolvedores devem definir e publicar definições de eventos junto com seus parâmetros (ou também com tipos de objeto associados) para o processamento de eventos, de forma que as colisões acidentais de IDs de evento possam ser evitadas. A especificação IAccessible2 usa parte do intervalo reservado do OEM.

## <a name="community-reserved-events"></a>Eventos reservados da Comunidade

O intervalo reservado da Comunidade é para WinEvents especificado pela AIA (Accessibility Interoperability Alliance) para uso em todo o setor. Os desenvolvedores são altamente incentivados a definir e publicar uma especificação oficial antes de usar valores desse intervalo.

## <a name="atom-events"></a>Eventos ATOM

O intervalo ATOM é reservado para IDs de eventos que são alocados em tempo de execução por meio da API de extensibilidade de automação da interface do usuário. Não use os valores do intervalo ATOM para qualquer outra finalidade. O uso da função [**GlobalAddAtom**](/windows/desktop/api/winbase/nf-winbase-globaladdatoma) com um GUID de cadeia de caracteres é o método recomendado para alocar WinEvents do intervalo de Atom.

## <a name="using-values-from-a-reserved-range"></a>Usando valores de um intervalo reservado

De acordo com a especificação WinEvent, os valores do intervalo reservado do sistema ou qualquer outro intervalo não definido, não podem ser usados sem a revisão do SDK. Para novos WinEvents, os aplicativos devem usar valores dos intervalos reservados para o OEM reservado ou para a Comunidade. Antes de usar um novo WinEvent, os desenvolvedores são altamente aconselhados a compartilhar suas especificações de forma aberta e ampla e devem funcionar com a aliança de interoperabilidade de acessibilidade para definir as especificações de WinEvent.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[Aliança de interoperabilidade de acessibilidade](https://www.atia.org/)
</dt> </dl>

 

 