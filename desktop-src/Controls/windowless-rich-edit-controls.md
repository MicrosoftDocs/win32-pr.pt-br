---
title: Controles de edição rich edit sem janela
description: Esta seção contém informações sobre os elementos de programação usados com controles de edição rich edit sem janela.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d03cbc4c694ce8e10a5b877298f148cd9ac47bd24c364aa3cde7fc19bc994e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655786"
---
# <a name="windowless-rich-edit-controls"></a>Controles de edição rich edit sem janela

Esta seção contém informações sobre os elementos de programação usados com controles de edição rich edit sem janela. O Component Object Model (COM) define um conjunto de interfaces para dar suporte a objetos sem janela. Objetos sem janela podem entrar no estado ativo in-locar sem ter sua própria janela, mas, em vez disso, usar a janela do contêiner. Consequentemente, um objeto sem janela usa menos recursos do sistema e oferece melhor desempenho por meio de ativação e desativação mais rápidas. Além disso, objetos sem janela podem ser não retangulares e transparentes.

### <a name="overviews"></a>Visões gerais



| Tópico                                                                          | Sumário                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre controles de edição rich edit sem janela](about-windowless-rich-edit-controls.md) | Um controle de edição avançada sem janelas, também conhecido como um objeto de serviços de texto, é um objeto que fornece a funcionalidade de um controle de [edição](rich-edit-controls.md) avançada sem fornecer a janela.<br/> |



 

### <a name="functions"></a>Funções



| Tópico                                            | Sumário                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | A [**função CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) cria uma instância de um objeto de serviços de texto. O objeto de serviços de texto dá suporte a uma variedade de interfaces, incluindo [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e o TOM (Modelo de Objeto de Texto).<br/> |



 

### <a name="interfaces"></a>Interfaces



| Tópico                                  | Sumário                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | A interface [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) é usada por um objeto de serviços de texto para obter serviços de host de texto.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Estende o TOM para fornecer funcionalidade extra para a operação sem janelas.<br/>                                     |



 

 

 





