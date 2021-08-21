---
description: Como criar uma DLL DirectShow filtro de dados
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Como criar uma DLL DirectShow filtro de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443f8aff88cf73198ed7c417da77f6febf33e18806efba5431e18117ddd2c32e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079006"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Como criar uma DLL DirectShow filtro de dados

Este artigo descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow. Este artigo é uma continuação de [How to Implement IUnknown](how-to-implement-iunknown.md), que descreve como implementar a interface **IUnknown** derivando seu componente da classe base [**CUnknown.**](cunknown.md)

Este artigo inclui as seções a seguir.

-   [Fábricas de classes e modelos de fábrica](class-factories-and-factory-templates.md)
-   [Matriz de modelo de fábrica](factory-template-array.md)
-   [Funções DLL](dll-functions.md)

O registro de um DirectShow de dados (em vez de um objeto COM genérico) requer algumas etapas adicionais que não são abordadas neste artigo. Para obter informações sobre como registrar filtros, [consulte How to Register DirectShow Filters](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



