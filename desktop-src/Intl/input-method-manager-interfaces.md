---
description: Esta seção descreve as interfaces do IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces do Gerenciador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759661"
---
# <a name="input-method-manager-interfaces"></a>Interfaces do Gerenciador de métodos de entrada

Esta seção descreve as interfaces do IMM.



| Interface                                                            | Descrição                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Fornece serviços relacionados ao IME que são comuns para diferentes idiomas.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Permite que os clientes acessem um dicionário de usuário do Microsoft IME.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Fornece serviços de processamento de idioma usando o Microsoft IME.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Insere texto em aplicativos do IMEPadApplets que implementam a interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Insere cadeias de caracteres em aplicativos por meio da interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Fornece acesso à lista de dicionários de plug-ins do IME.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Especifica os métodos chamados do objeto de interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) para emular a interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) . |



 

 

 



