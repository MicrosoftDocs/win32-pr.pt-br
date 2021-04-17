---
title: Interfaces (páginas de controles e de propriedades)
description: As interfaces a seguir são usadas para criar objetos COM padrão e páginas de propriedades.
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105771431"
---
# <a name="interfaces-controls-and-property-pages"></a>Interfaces (páginas de controles e de propriedades)

As interfaces a seguir são usadas para criar objetos COM padrão e páginas de propriedades.



| Interface                                             | Descrição                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | Fornece um wrapper em um objeto de fonte do Windows.                                                                                                                                                             |
| [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | Expõe as propriedades de um objeto de fonte por meio da automação. Ele fornece um subconjunto dos métodos [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | Fornece os recursos para dar suporte a mnemônicos de teclado, propriedades de ambiente e eventos em objetos de controle.                                                                                                  |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | Fornece os métodos que permitem que um objeto do site gerencie cada controle inserido dentro de um contêiner.                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | Recupera as informações nas páginas de propriedades oferecidas por um objeto.                                                                                                                                        |
| [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | Gerencia um objeto de imagem e suas propriedades. Os objetos de imagem fornecem uma abstração neutra de idioma para bitmaps, ícones e metaarquivos.                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | Expõe as propriedades do objeto de imagem por meio da automação. Ele fornece um subconjunto da funcionalidade disponível por meio de métodos [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .                                                |
| [**IPointerInactive**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | Permite que um objeto permaneça inativo na maior parte do tempo, ainda que participe da interação com o mouse, incluindo arrastar e soltar.                                                                         |
| [**IPrint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | Permite documentos compostos em geral e documentos ativos em particular para dar suporte à impressão programática.                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | Implementado por um objeto Sink para receber notificações sobre alterações de propriedade de um objeto que dá suporte a [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) como uma interface de saída.                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | Fornece os principais recursos de um objeto de página de propriedades que gerencia uma página específica dentro de uma folha de propriedades.                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | Uma extensão para [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) para dar suporte à seleção inicial de uma propriedade em uma página.                                                                                                 |
| [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | Fornece os principais recursos para um objeto de site da página de propriedades.                                                                                                                                                  |
| [**IQuickActivate**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | Habilita controles e contêineres para evitar gargalos de desempenho no carregamento de controles. Ele combina o tempo de carga ou o handshake de tempo de inicialização entre o controle e seu contêiner em uma única chamada. |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | Fornece controles de quadro simples que atuam como contêineres simples para outros controles aninhados.                                                                                                                      |
| [**ISpecifyPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | Indica que um objeto dá suporte a páginas de propriedades.                                                                                                                                                            |



 

 

 
