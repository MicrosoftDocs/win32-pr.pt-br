---
description: Esta seção contém informações sobre as interfaces usadas para controlar a aparência e o comportamento do painel de entrada do Tablet PC.
ms.assetid: 58f49d5b-8b38-45e7-94e1-8a4434d6e13b
title: Interfaces do painel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 798dc60f34171ce7254bca74c27a51fa12eaba65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171840"
---
# <a name="text-input-panel-interfaces"></a>Interfaces do painel de entrada de texto

Esta seção contém informações sobre as interfaces usadas para controlar a aparência e o comportamento do painel de entrada do Tablet PC.

> [!Note]  
> As interfaces do painel de entrada de texto não são compatíveis com a automação.

 

## <a name="in-this-section"></a>Nesta seção



| Interface                                                                | Descrição                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface IHandWrittenTextInsertion**](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | Usado pelo código de entrada de texto personalizado do aplicativo para inserir o texto no campo de texto e no armazenamento de backup de serviços de texto.<br/> |
| [**Interface ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | Fornece controle sobre o painel de entrada do Tablet PC.<br/>                                                                                  |
| [**Interface ITextInputPanelEventSink**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | Define métodos que manipulam os eventos da [**interface ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .<br/>                                      |
| [**Interface ITextInputPanelRunInfo**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | Fornece um método para determinar se o painel de entrada de texto está em execução no momento.<br/>                                                      |
| [**Interface ITipAutocompleteClient**](itipautocompleteclient.md)       | Permite que o cliente chame o objeto de provedor de preenchimento automático do painel de entrada de texto do aplicativo.<br/>                                      |
| [**Interface ITipAutocompleteProvider**](itipautocompleteprovider.md)   | Gerencia o lado do aplicativo da integração de preenchimento automático do painel de entrada de texto.<br/>                                                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do painel de entrada de texto](text-input-panel-reference.md)
</dt> </dl>

 

 




