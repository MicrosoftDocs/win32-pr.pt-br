---
description: Esta seção descreve as interfaces do IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces do Gerenciador de Métodos de Entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e7267f5f38bb160a7f71b4f0379a2b03a3263b85a64dc8e666226dd3150911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809995"
---
# <a name="input-method-manager-interfaces"></a>Interfaces do Gerenciador de Métodos de Entrada

Esta seção descreve as interfaces do IMM.



| Interface                                                            | Descrição                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Fornece serviços relacionados ao IME que são comuns para idiomas diferentes.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Permite que os clientes acessem um dicionário de usuários do Microsoft IME.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Fornece serviços de processamento de idioma usando o Microsoft IME.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Insere texto em aplicativos de IMEPadApplets que implementam a interface [**IImePadApplet.**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Insições de cadeias de caracteres em aplicativos por meio da interface [**IImePad.**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Fornece acesso à lista de dicionários de plug-in do IME.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Especifica métodos chamados do objeto de interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) para emular a interface [**IImePadApplet.**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) |



 

 

 



