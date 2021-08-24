---
description: A técnica programática recomendada para definir contextos em um aplicativo que não está habilitado para tinta é usar as funções SetInputScope para associar o contexto aos campos no aplicativo.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Definindo o contexto com as APIs SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0abe9992e4a4ee81190fdee022b11f443592e05d7c99f9a5e69d0a200f63ecbf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708146"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Definindo o contexto com as APIs SetInputScope

A técnica programática recomendada para definir contextos em um aplicativo que não está habilitado para tinta é usar as funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) para associar o contexto aos campos no aplicativo.

O Microsoft Windows XP Tablet PC Edition Development Kit 1.7 foi a primeira versão do Microsoft Windows oferecer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). Windows O Vista também dá suporte a essas funções. As **definições de SetInputScope** são declaradas em InputScope.idl e InputScope.h. Para obter mais detalhes, [consulte Estrutura de Serviços de Texto](../tsf/text-services-framework.md).

As [**funções SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) são a maneira recomendada de definir o contexto para controles e aplicativos que não estão habilitados para tinta.

## <a name="common-input-scopes"></a>Escopos de entrada comuns

Usando as [**funções SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) e o conjunto definido de escopos de entrada comuns descritos na enumeração [**InputScope,**](/windows/win32/api/inputscope/ne-inputscope-inputscope) você pode melhorar a precisão de reconhecimento dos reconhecedores de manuscrito da Microsoft.

> [!Note]  
> Atualmente, os reconhecedores para inglês (Estados Unidos), inglês (Reino Unido), alemão, francês, italiano, espanhol, holandês e português usam os escopos de entrada comuns com [**SetInputScope.**](/windows/win32/api/inputscope/nf-inputscope-setinputscope)

 

 

 
