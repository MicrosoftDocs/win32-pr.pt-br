---
description: O método Render Inicializa o grafo de filtro de DVD.
ms.assetid: 910f1e3f-b3bb-498b-93da-3a974a3117e8
title: Método Render
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 677abab1c669642c1e51e0041c98949d923147c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105754752"
---
# <a name="render-method"></a>Método Render

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `Render` método inicializa o grafo de filtro de DVD.

``` syntax
MSWebDVD.Render(iRender = 0)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iRender"></span><span id="irender"></span><span id="IRENDER"></span>*iRender*
</dt> <dd>

Especifica um valor inteiro que indica se o grafo de filtro será destruído e recriado.



| Valor | Descrição                                                                                         |
|-------|-----------------------------------------------------------------------------------------------------|
| 0     | O gráfico de filtro não será destruído e recriado se ele já existir. Este é o valor padrão. |
| 1     | O gráfico de filtro será destruído e recriado se ele já existir.                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O `Render` método permite que o objeto **MSWebDVD** inicialize completamente o grafo de filtro do DirectShow subjacente na inicialização. Isso elimina o ligeiro atraso que, de outra forma, ocorre quando o usuário emite o primeiro comando para reproduzir um disco ou mostrar um menu. Não há nenhum caso no qual `Render` precise ser chamado antes de chamar qualquer outro método. Por exemplo, se o aplicativo chamar [**PlayTitle**](playtitle-method.md) antes que o grafo de filtro tenha sido inicializado, o objeto **MSWebDVD** será chamado `Render` automaticamente antes de tentar reproduzir o disco.

 

 



