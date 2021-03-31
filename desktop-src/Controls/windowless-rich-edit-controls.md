---
title: Controles de edição avançados sem janela
description: Esta seção contém informações sobre os elementos de programação usados com controles de edição ricos sem janela.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005122"
---
# <a name="windowless-rich-edit-controls"></a>Controles de edição avançados sem janela

Esta seção contém informações sobre os elementos de programação usados com controles de edição ricos sem janela. O COM (Component Object Model) define um conjunto de interfaces para oferecer suporte a objetos sem janela. Os objetos sem janela podem entrar no estado ativo no local não ter sua própria janela, mas sim usar a janela de seu contêiner. Consequentemente, um objeto sem janela usa menos recursos do sistema e oferece melhor desempenho por meio de ativação e desativação mais rápida. Além disso, os objetos sem janela podem ser não retangulares e transparentes.

### <a name="overviews"></a>Visões gerais



| Tópico                                                                          | Sumário                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles de edição avançados sem janela](about-windowless-rich-edit-controls.md) | Um controle de edição rico sem janela, também conhecido como objeto de serviços de texto, é um objeto que fornece a funcionalidade de um [controle de edição rico](rich-edit-controls.md) sem fornecer a janela.<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                            | Sumário                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Createtextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | A função [**Createtextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) cria uma instância de um objeto de serviços de texto. O objeto de serviços de texto dá suporte a uma variedade de interfaces, incluindo [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e o Tom (modelo de objeto de texto).<br/> |



 

### <a name="interfaces"></a>Interfaces



| Tópico                                  | Sumário                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | A interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) é usada por um objeto de serviços de texto para obter os serviços de host de texto.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Estende o TOM para fornecer funcionalidade extra para operação sem janelas.<br/>                                     |



 

 

 





