---
title: As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado
description: As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935406"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

As seguintes APIs do Gerenciador de métodos de entrada não são suportadas por IMEs do chinês simplificado no Windows 8.1:

-   Interface IFECommon
-   Interface IFEDictionary
-   Interface IFELanguage
-   Interface IImePad
-   Interface IImePadApplet
-   Interface IImeSpecifyApplets

## <a name="manifestations"></a>Manifestações

As funções que usam essas APIs não funcionam com o IME do chinês simplificado.

## <a name="solution"></a>Solução

Os aplicativos devem ser projetados para que os usuários possam concluir a tarefa desejada sem usar a API especificada.

## <a name="resources"></a>Recursos

-   [Interfaces do Gerenciador de métodos de entrada](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interface IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Interface IFEDictionary](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 