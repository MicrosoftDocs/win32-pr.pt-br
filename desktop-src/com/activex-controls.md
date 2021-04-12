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
# <a name="activex-controls"></a>Controles ActiveX

A tecnologia de controles ActiveX permanece em uma base que consiste em objetos COM, conectáveis, documentos compostos, páginas de propriedades, automação OLE, persistência de objetos e objetos de imagem e imagens fornecidos pelo sistema. Conforme resumido abaixo, cada uma dessas tecnologias principais desempenha uma função nos controles.

<dl> <dt>

<span id="COM"></span><span id="com"></span>INTERFACES
</dt> <dd>

Um controle é essencialmente um objeto COM que expõe a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , por meio da qual os clientes podem obter ponteiros para suas outras interfaces. Os controles podem dar suporte ao licenciamento por meio de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e Autoregistro. Consulte [a Component Object Model](the-component-object-model.md) para obter mais informações sobre com, licenciamento e Autoregistro.

</dd> <dt>

<span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objetos conectáveis
</dt> <dd>

Os controles podem dar suporte a interfaces de saída por meio de objetos conectáveis para que o controle possa se comunicar com seu cliente. Por exemplo, uma interface de saída pode disparar uma ação no cliente, pode notificar o cliente sobre alguma alteração no controle ou pode solicitar permissão do cliente antes de o controle executar alguma ação. Consulte [eventos em objetos com e conectáveis](events-in-com-and-connectable-objects.md) para obter mais informações sobre como os objetos conectáveis funcionam.

</dd> <dt>

<span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transferência de dados uniforme
</dt> <dd>

Os controles podem oferecer suporte a serem arrastados e descartados dentro de um contêiner com a ajuda de seu contêiner. Consulte [**IOleInPlaceObjectWindowless:: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) para obter mais informações sobre arrastar e soltar.

</dd> <dt>

<span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documentos compostos
</dt> <dd>

Um controle pode ser um objeto ativo in-loco que pode ser inserido em um cliente que contém. Um usuário final ativa o controle para iniciar uma ação no aplicativo de contêiner. Consulte [documentos compostos](compound-documents.md) para obter mais informações sobre a ativação in-loco e outras interfaces de documentos compostos.

</dd> <dt>

<span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Páginas de propriedades
</dt> <dd>

Os controles podem fornecer páginas de propriedades para que os usuários finais possam exibir e alterar as propriedades do controle. Consulte [páginas de propriedades e folhas de propriedades](property-pages-and-property-sheets.md) para obter mais informações sobre como as páginas de propriedades funcionam.

</dd> <dt>

<span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automação OLE
</dt> <dd>

Os controles podem fornecer programação por meio da automação OLE para que os clientes possam aproveitar os recursos do controle por meio de uma linguagem de programação fornecida pelo cliente. Consulte a seção automação OLE para obter mais informações sobre a automação OLE.

</dd> <dt>

<span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Armazenamento persistente
</dt> <dd>

Um controle pode implementar uma ou mais de várias interfaces de persistência para dar suporte à persistência de seu estado. O implementador de controle deve decidir quais tipos de persistência são mais importantes e implementar as interfaces de persistência apropriadas. O cliente decide qual interface prefere usar. Consulte [a Component Object Model](the-component-object-model.md) para obter mais informações sobre todas as interfaces de persistência.

</dd> <dt>

<span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objetos de fonte e imagem
</dt> <dd>

Os controles podem usar esses objetos fornecidos pelo sistema para fornecer uma representação visual de si mesmos no cliente. O objeto Font implementa várias interfaces, incluindo [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) e [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp). Um objeto Font pode ser criado com [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect). O objeto Picture também implementa várias interfaces, incluindo [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp). Um objeto de imagem pode ser criado usando [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) e pode ser carregado de um fluxo com [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).

</dd> </dl>

É importante entender que esses recursos podem ser usados em qualquer objeto OLE. Uma não precisa implementar um controle para usar esses recursos. Além disso, a única interface necessária em um controle é IUnknown. O controle, opcionalmente, dá suporte a outras interfaces com base na necessidade de dar suporte aos recursos relacionados.

Além desses recursos, as seguintes interfaces e funções são específicas para a tecnologia de controles: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor). Além disso, os controles específicos são um conjunto de padrões para propriedades e métodos aos quais um controle ou um contêiner de controle pode dar suporte.

> [!Note]  
> A biblioteca do sistema OleAut32.dll contém implementações das funções ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)). Além disso, OleAut32.dll contém as implementações dos objetos de fonte e imagem padrão, bem como uma biblioteca de tipos para todas as interfaces usadas com controles, bem como os tipos de dados e estruturas de dados adicionais.

 

Para mais informações, consulte os seguintes tópicos:

-   [Arquitetura de controles ActiveX](activex-controls-architecture.md)
-   [Interfaces de controles ActiveX](activex-controls-interfaces.md)
-   [Propriedades e métodos](properties-and-methods.md)
-   [Eventos de controle](control-events.md)
-   [Representação visual](visual-representation.md)
-   [Manipulação de teclado para controles](keyboard-handling-for-controls.md)
-   [Persistência](persistence.md)
-   [Registro e licenciamento](registration-and-licensing.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes de contêiner de controle e controle ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 