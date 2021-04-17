---
description: Como criar uma DLL de filtro do DirectShow
ms.assetid: 142bc8a2-240d-418f-9374-62d34a76ec38
title: Como criar uma DLL de filtro do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee964115e040d11ae10562b05899b2895f03d2fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747801"
---
# <a name="how-to-create-a-directshow-filter-dll"></a>Como criar uma DLL de filtro do DirectShow

Este artigo descreve como implementar um componente como uma DLL (biblioteca de vínculo dinâmico) no Microsoft DirectShow. Este artigo é uma continuação de [como implementar IUnknown](how-to-implement-iunknown.md), que descreve como implementar a interface **IUnknown** derivando seu componente da classe base [**CUnknown**](cunknown.md) .

Este artigo inclui as seções a seguir.

-   [Fábricas de classes e modelos de fábrica](class-factories-and-factory-templates.md)
-   [Matriz de modelo de fábrica](factory-template-array.md)
-   [Funções de DLL](dll-functions.md)

O registro de um filtro do DirectShow (em oposição a um objeto COM genérico) requer algumas etapas adicionais que não são abordadas neste artigo. Para obter informações sobre como registrar filtros, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



