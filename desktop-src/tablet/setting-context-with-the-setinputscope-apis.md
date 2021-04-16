---
description: A técnica de programação recomendada para configurar contextos em um aplicativo que não está habilitado para tinta é usar as funções SetInputScope para associar o contexto aos campos no aplicativo.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Configurando o contexto com as APIs SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787013"
---
# <a name="setting-context-with-the-setinputscope-apis"></a>Configurando o contexto com as APIs SetInputScope

A técnica de programação recomendada para configurar contextos em um aplicativo que não está habilitado para tinta é usar as funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) para associar o contexto aos campos no aplicativo.

O Microsoft Windows XP Tablet PC Edition Development Kit 1,7 foi a primeira versão do Microsoft Windows a oferecer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope). O Windows Vista também fornece suporte para essas funções. As definições de **SetInputScope** são declaradas em InputScope. idl e InputScope. h. Para obter mais detalhes, consulte [estrutura de serviços de texto](../tsf/text-services-framework.md).

As funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) são a maneira recomendada de definir o contexto para controles e aplicativos que não são habilitados para tinta.

## <a name="common-input-scopes"></a>Escopos de entrada comuns

Usando as funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) e o conjunto definido de escopos de entrada comuns descritos na enumeração [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , você pode melhorar a precisão de reconhecimento dos reconhecedores de manuscrito da Microsoft.

> [!Note]  
> Os reconhecedores para inglês (Estados Unidos), inglês (Reino Unido), alemão, francês, italiano, espanhol, holandês e Português atualmente dão suporte ao uso de escopos de entrada comuns com [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).

 

 

 
