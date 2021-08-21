---
title: Interfaces necessárias (COM)
description: Saiba mais sobre as interfaces ActiveX contêiner de controle que podem ou devem ser implementadas por contêineres de controle.
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf19cb8d0c72b365f6a8faa263fc76ddede1e5231fc34a9090c064f54d75b7f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309658"
---
# <a name="required-interfaces-com"></a>Interfaces necessárias (COM)

A tabela a seguir lista as interfaces ActiveX contêiner de controle e indica quais interfaces são opcionais e que são obrigatórias e devem ser implementadas por contêineres de controle.



| Interface                                                                      | Obrigatório?      | Comentários                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ioleclientsite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Iadvisesink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | Não<br/>  | Somente quando o contêiner deseja (a) notificações de alteração de dados (controles com [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)), (b) exibir notificação de alteração (controles que não estão ativos e têm [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) ou [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)) e (c) outras notificações de controles que atuam como objetos inseridos padrão.<br/> |
| [**Ioleinplacesite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Iolecontrolsite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Ioleinplaceframe**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**Iolecontainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Sim<br/> | Consulte a observação 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch para** propriedades de ambiente<br/>                                | Sim<br/> | Consulte a observação 2 e Propriedades [de ambiente para controles](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Controlar conjuntos de eventos<br/>                                                  | Sim<br/> | Confira a observação 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | Não<br/>  | [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e suporte para quadros simples aninhados são opcionais.<br/>                                                                                                                                                                                                                                                    |
| [Ipropertynotifysink](data-binding-through-ipropertynotifysink.md)<br/> | Não<br/>  | Necessário apenas para contêineres que (a) têm sua própria interface do usuário de edição de propriedade, o que exigiria atualização sempre que um controle alterasse uma propriedade em si ou (b) quisesse controlar as alterações de propriedade \[ [**requestedit**](/windows/desktop/Midl/requestedit) e outros recursos de associação de \] dados.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Sim<br/> | Obrigatório se o contêiner dá suporte a interfaces duplas. Consulte a observação 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**Iclassfactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | Não<br/>  | O suporte é altamente recomendado.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  [**IOleContainer é**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) implementado no objeto de documento ou formulário (ou análogo apropriado) que contém os sites de contêiner. Os controles **usam IOleContainer** para navegar até outros controles no mesmo documento ou formulário.
2.  O suporte para interfaces duplas não é obrigatório, mas é altamente recomendado. Escrever ActiveX contêineres de controle para aproveitar as interfaces duplas permitirá um melhor desempenho com controles que oferecem suporte à interface dupla.

ActiveX contêineres de controle devem dar suporte a exceções de Automação OLE. Se um contêiner de controle dá suporte a interfaces duplas, ele deve capturar exceções de automação por meio [de IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

