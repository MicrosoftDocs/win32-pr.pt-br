---
title: Estendendo funções OpenGL
description: A biblioteca OpenGL dá suporte a várias implementações de suas funções.
ms.assetid: 9eb08fd4-899a-4610-9491-d7f377a19b46
keywords:
- OpenGL em Windows,funções de extensão
- funções de extensão OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dce68498d5a3e672e63da1ae05d9bb513a4121d110237d90cdad75df0ff84d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361338"
---
# <a name="extending-opengl-functions"></a>Estendendo funções OpenGL

A biblioteca OpenGL dá suporte a várias implementações de suas funções. Funções de extensão com suporte em um contexto de renderização não têm necessariamente suporte em um contexto de renderização diferente. Para um determinado contexto de renderização em um aplicativo usando funções de extensão, use apenas os endereços de função retornados pela [**função wglGetProcAddress.**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)

 

 




