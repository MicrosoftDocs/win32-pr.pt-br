---
title: Interfaces necessárias (COM)
description: Saiba mais sobre as interfaces de contêiner do controle ActiveX que podem ou devem ser implementadas por contêineres de controle.
ms.assetid: ae238882-d0c9-4120-b8a8-001bf9559cfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55015ee5837754c073d2590144687131c285bb80
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407639"
---
# <a name="required-interfaces-com"></a>Interfaces necessárias (COM)

A tabela a seguir lista as interfaces de contêiner do controle ActiveX e indica quais interfaces são opcionais e quais são obrigatórias e devem ser implementadas por contêineres de controle.



| Interface                                                                      | Necessário?      | Comentários                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)<br/>                            | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)<br/>                                  | Não<br/>  | Somente quando o contêiner desejar (a) as notificações de alteração de dados (controles com [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)), (b) exibir notificação de alteração (controles que não estão ativos e têm [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) ou [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)) e (c) outras notificações de controles atuando como objetos incorporados padrão.<br/> |
| [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite)<br/>                          | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)<br/>                          | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe)<br/>                        | Sim<br/> |                                                                                                                                                                                                                                                                                                                                                              |
| [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer)<br/>                              | Sim<br/> | Confira a Observação 1<br/>                                                                                                                                                                                                                                                                                                                                        |
| **IDispatch** para propriedades de ambiente<br/>                                | Sim<br/> | Consulte a observação 2 e [as propriedades de ambiente para controles](ambient-properties-for-controls.md)<br/>                                                                                                                                                                                                                                                             |
| Controlar conjuntos de eventos<br/>                                                  | Sim<br/> | Confira a observação 2<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)<br/>                        | Não<br/>  | O [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) e o suporte para estruturas simples aninhadas são opcionais.<br/>                                                                                                                                                                                                                                                    |
| [IPropertyNotifySink](data-binding-through-ipropertynotifysink.md)<br/> | Não<br/>  | Necessário apenas para contêineres que (a) têm sua própria interface de usuário de edição de propriedade que exigiria atualização sempre que um controle alterou uma propriedade ou (b) deseja controlar \[ [](/windows/desktop/Midl/requestedit) \] as alterações de propriedade requestedit e outros recursos de ligação de dados.<br/>                                                                            |
| [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>       | Sim<br/> | Obrigatório se o contêiner der suporte a interfaces duplas. Consulte a observação 2.<br/>                                                                                                                                                                                                                                                                                      |
| [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)<br/>                            | Não<br/>  | O suporte é altamente recomendado.<br/>                                                                                                                                                                                                                                                                                                                  |



 

1.  O [**IOleContainer**](/windows/desktop/api/OleIdl/nn-oleidl-iolecontainer) é implementado no documento ou no objeto de formulário (ou analógico apropriado) que mantém os sites de contêiner. Os controles usam **IOleContainer** para navegar para outros controles no mesmo documento ou formulário.
2.  O suporte para interfaces duplas não é obrigatório, mas é altamente recomendável. Escrever contêineres de controle ActiveX para aproveitar as vantagens de interfaces duplas proporcionará melhor desempenho com controles que oferecem suporte a interfaces duplas.

Contêineres de controle ActiveX devem dar suporte a exceções de automação OLE. Se um contêiner de controle oferecer suporte a interfaces duplas, ele deverá capturar exceções de automação por meio de [IErrorInfo](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Contêineres](containers.md)
</dt> </dl>

 

