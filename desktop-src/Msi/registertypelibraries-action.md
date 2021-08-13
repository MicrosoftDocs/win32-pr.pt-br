---
description: A ação RegisterTypeLibraries registra bibliotecas de tipos com o sistema. Essa ação é aplicada a cada arquivo referenciado na tabela TypeLib agendada para instalação.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Ação RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac42c831c8413f297d3df2302523a2372b11d1efcffe82ce0d3a82da722832cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626759"
---
# <a name="registertypelibraries-action"></a>Ação RegisterTypeLibraries

A ação RegisterTypeLibraries registra bibliotecas de tipos com o sistema. Essa ação é aplicada a cada arquivo referenciado na tabela [TypeLib](typelib-table.md) agendada para instalação.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação RegisterTypeLibraries deve vir após a [ação InstallFiles.](installfiles-action.md)

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) da biblioteca de tipos registrada. |



 

## <a name="remarks"></a>Comentários

A ação RegisterTypeLibraries requer que o idioma da biblioteca de tipos seja corretamente autorado no campo Idioma da tabela TypeLib. A autoração incorreta do campo Idioma pode fazer com que o instalador falhe ao registrar uma biblioteca de tipos válida de outra forma.

 

 



