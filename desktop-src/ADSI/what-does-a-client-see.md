---
title: O que um cliente vê
description: Este tópico lista as maneiras como um cliente visualiza dados ADSI.
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- extensões ADSI, o que um cliente vê
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d38563de47cfc80bdcf265249bf3e4cf10bc46471e18672221fed8c3047efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082170"
---
# <a name="what-does-a-client-see"></a>O que um cliente vê?

-   Um cliente vê a ADSI e todos os seus objetos de extensão como um objeto.
-   Um cliente ADSI vê uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que trata todas as interfaces duplas e de expedição no objeto, independentemente de a interface dupla ou de expedição ser implementada pelo agregador no provedor ou por uma extensão. Consulte Resolução [de conflitos de nome de função/propriedade na Automação em Extensões](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).
-   A ADSI não expõe nenhuma informação de tipo por meio dos métodos [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) ou [**IDispatch::GetTypeInfoCount.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) A ADSI fornece informações de tipo por meio da biblioteca de tipos.

 

 