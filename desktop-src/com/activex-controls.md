---
title: Controles ActiveX
description: Controles ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366737"
---
# <a name="activex-controls"></a><span data-ttu-id="5d3dd-103">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="5d3dd-103">ActiveX Controls</span></span>

<span data-ttu-id="5d3dd-104">A tecnologia de controles ActiveX permanece em uma base que consiste em objetos COM, conectáveis, documentos compostos, páginas de propriedades, automação OLE, persistência de objetos e objetos de imagem e imagens fornecidos pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="5d3dd-105">Conforme resumido abaixo, cada uma dessas tecnologias principais desempenha uma função nos controles.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="5d3dd-106"><span id="COM"></span><span id="com"></span>INTERFACES</span><span class="sxs-lookup"><span data-stu-id="5d3dd-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-107">Um controle é essencialmente um objeto COM que expõe a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , por meio da qual os clientes podem obter ponteiros para suas outras interfaces.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="5d3dd-108">Os controles podem dar suporte ao licenciamento por meio de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e Autoregistro.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="5d3dd-109">Consulte [a Component Object Model](the-component-object-model.md) para obter mais informações sobre com, licenciamento e Autoregistro.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objetos conectáveis</span><span class="sxs-lookup"><span data-stu-id="5d3dd-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-111">Os controles podem dar suporte a interfaces de saída por meio de objetos conectáveis para que o controle possa se comunicar com seu cliente.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="5d3dd-112">Por exemplo, uma interface de saída pode disparar uma ação no cliente, pode notificar o cliente sobre alguma alteração no controle ou pode solicitar permissão do cliente antes de o controle executar alguma ação.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="5d3dd-113">Consulte [eventos em objetos com e conectáveis](events-in-com-and-connectable-objects.md) para obter mais informações sobre como os objetos conectáveis funcionam.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferência de dados uniforme</span><span class="sxs-lookup"><span data-stu-id="5d3dd-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-115">Os controles podem oferecer suporte a serem arrastados e descartados dentro de um contêiner com a ajuda de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="5d3dd-116">Consulte [**IOleInPlaceObjectWindowless:: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) para obter mais informações sobre arrastar e soltar.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documentos compostos</span><span class="sxs-lookup"><span data-stu-id="5d3dd-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-118">Um controle pode ser um objeto ativo in-loco que pode ser inserido em um cliente que contém.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="5d3dd-119">Um usuário final ativa o controle para iniciar uma ação no aplicativo de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="5d3dd-120">Consulte [documentos compostos](compound-documents.md) para obter mais informações sobre a ativação in-loco e outras interfaces de documentos compostos.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Páginas de propriedades</span><span class="sxs-lookup"><span data-stu-id="5d3dd-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-122">Os controles podem fornecer páginas de propriedades para que os usuários finais possam exibir e alterar as propriedades do controle.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="5d3dd-123">Consulte [páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md) para obter mais informações sobre como as páginas de propriedades funcionam.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automação OLE</span><span class="sxs-lookup"><span data-stu-id="5d3dd-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-125">Os controles podem fornecer programação por meio da automação OLE para que os clientes possam aproveitar os recursos do controle por meio de uma linguagem de programação fornecida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="5d3dd-126">Consulte a seção automação OLE para obter mais informações sobre a automação OLE.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Armazenamento persistente</span><span class="sxs-lookup"><span data-stu-id="5d3dd-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-128">Um controle pode implementar uma ou mais de várias interfaces de persistência para dar suporte à persistência de seu estado.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="5d3dd-129">O implementador de controle deve decidir quais tipos de persistência são mais importantes e implementar as interfaces de persistência apropriadas.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="5d3dd-130">O cliente decide qual interface prefere usar.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="5d3dd-131">Consulte [a Component Object Model](the-component-object-model.md) para obter mais informações sobre todas as interfaces de persistência.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="5d3dd-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objetos de fonte e imagem</span><span class="sxs-lookup"><span data-stu-id="5d3dd-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="5d3dd-133">Os controles podem usar esses objetos fornecidos pelo sistema para fornecer uma representação visual de si mesmos no cliente.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="5d3dd-134">O objeto Font implementa várias interfaces, incluindo [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) e [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="5d3dd-135">Um objeto Font pode ser criado com [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="5d3dd-136">O objeto Picture também implementa várias interfaces, incluindo [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="5d3dd-137">Um objeto de imagem pode ser criado usando [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) e pode ser carregado de um fluxo com [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="5d3dd-138">É importante entender que esses recursos podem ser usados em qualquer objeto OLE.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="5d3dd-139">Uma não precisa implementar um controle para usar esses recursos.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="5d3dd-140">Além disso, a única interface necessária em um controle é IUnknown.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="5d3dd-141">O controle, opcionalmente, dá suporte a outras interfaces com base na necessidade de dar suporte aos recursos relacionados.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="5d3dd-142">Além desses recursos, as seguintes interfaces e funções são específicas para a tecnologia de controles: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="5d3dd-143">Além disso, os controles específicos são um conjunto de padrões para propriedades e métodos aos quais um controle ou um contêiner de controle pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="5d3dd-144">A biblioteca do sistema OleAut32.dll contém implementações das funções ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span><span class="sxs-lookup"><span data-stu-id="5d3dd-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="5d3dd-145">Além disso, OleAut32.dll contém as implementações dos objetos de fonte e imagem padrão, bem como uma biblioteca de tipos para todas as interfaces usadas com controles, bem como os tipos de dados e estruturas de dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="5d3dd-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="5d3dd-146">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="5d3dd-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="5d3dd-147">Arquitetura de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="5d3dd-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="5d3dd-148">Interfaces de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="5d3dd-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="5d3dd-149">Propriedades e métodos</span><span class="sxs-lookup"><span data-stu-id="5d3dd-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="5d3dd-150">Eventos de controle</span><span class="sxs-lookup"><span data-stu-id="5d3dd-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="5d3dd-151">Representação visual</span><span class="sxs-lookup"><span data-stu-id="5d3dd-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="5d3dd-152">Manipulação de teclado para controles</span><span class="sxs-lookup"><span data-stu-id="5d3dd-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="5d3dd-153">Persistência</span><span class="sxs-lookup"><span data-stu-id="5d3dd-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="5d3dd-154">Registro e licenciamento</span><span class="sxs-lookup"><span data-stu-id="5d3dd-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="5d3dd-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d3dd-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d3dd-156">Diretrizes de contêiner de controle e controle ActiveX</span><span class="sxs-lookup"><span data-stu-id="5d3dd-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 