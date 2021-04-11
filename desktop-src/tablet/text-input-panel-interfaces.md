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
# <a name="text-input-panel-interfaces"></a><span data-ttu-id="0c69f-103">Interfaces do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="0c69f-103">Text Input Panel Interfaces</span></span>

<span data-ttu-id="0c69f-104">Esta seção contém informações sobre as interfaces usadas para controlar a aparência e o comportamento do painel de entrada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0c69f-104">This section contains information about the interfaces used to control the appearance and behavior of the Tablet PC Input Panel.</span></span>

> [!Note]  
> <span data-ttu-id="0c69f-105">As interfaces do painel de entrada de texto não são compatíveis com a automação.</span><span class="sxs-lookup"><span data-stu-id="0c69f-105">The Text Input Panel interfaces are not Automation compliant.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="0c69f-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="0c69f-106">In This Section</span></span>



| <span data-ttu-id="0c69f-107">Interface</span><span class="sxs-lookup"><span data-stu-id="0c69f-107">Interface</span></span>                                                                | <span data-ttu-id="0c69f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c69f-108">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c69f-109">**Interface IHandWrittenTextInsertion**</span><span class="sxs-lookup"><span data-stu-id="0c69f-109">**IHandWrittenTextInsertion Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-ihandwrittentextinsertion) | <span data-ttu-id="0c69f-110">Usado pelo código de entrada de texto personalizado do aplicativo para inserir o texto no campo de texto e no armazenamento de backup de serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="0c69f-110">Used by the application's custom text entry code to insert the text into both the text field and the Text Services backing-store.</span></span><br/> |
| [<span data-ttu-id="0c69f-111">**Interface ITextInputPanel**</span><span class="sxs-lookup"><span data-stu-id="0c69f-111">**ITextInputPanel Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)                     | <span data-ttu-id="0c69f-112">Fornece controle sobre o painel de entrada do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0c69f-112">Provides control over the Tablet PC Input Panel.</span></span><br/>                                                                                  |
| [<span data-ttu-id="0c69f-113">**Interface ITextInputPanelEventSink**</span><span class="sxs-lookup"><span data-stu-id="0c69f-113">**ITextInputPanelEventSink Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpaneleventsink)   | <span data-ttu-id="0c69f-114">Define métodos que manipulam os eventos da [**interface ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) .</span><span class="sxs-lookup"><span data-stu-id="0c69f-114">Defines methods that handle the [**ITextInputPanel Interface**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) events.</span></span><br/>                                      |
| [<span data-ttu-id="0c69f-115">**Interface ITextInputPanelRunInfo**</span><span class="sxs-lookup"><span data-stu-id="0c69f-115">**ITextInputPanelRunInfo Interface**</span></span>](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanelruninfo)       | <span data-ttu-id="0c69f-116">Fornece um método para determinar se o painel de entrada de texto está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="0c69f-116">Provides a method to determine if the Text Input Panel is currently running.</span></span><br/>                                                      |
| [<span data-ttu-id="0c69f-117">**Interface ITipAutocompleteClient**</span><span class="sxs-lookup"><span data-stu-id="0c69f-117">**ITipAutocompleteClient Interface**</span></span>](itipautocompleteclient.md)       | <span data-ttu-id="0c69f-118">Permite que o cliente chame o objeto de provedor de preenchimento automático do painel de entrada de texto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0c69f-118">Enables the client to call the application's Text Input Panel auto complete provider object.</span></span><br/>                                      |
| [<span data-ttu-id="0c69f-119">**Interface ITipAutocompleteProvider**</span><span class="sxs-lookup"><span data-stu-id="0c69f-119">**ITipAutocompleteProvider Interface**</span></span>](itipautocompleteprovider.md)   | <span data-ttu-id="0c69f-120">Gerencia o lado do aplicativo da integração de preenchimento automático do painel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="0c69f-120">Manages the application's side of the Text Input Panel auto complete integration.</span></span><br/>                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="0c69f-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c69f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c69f-122">Referência do painel de entrada de texto</span><span class="sxs-lookup"><span data-stu-id="0c69f-122">Text Input Panel Reference</span></span>](text-input-panel-reference.md)
</dt> </dl>

 

 




