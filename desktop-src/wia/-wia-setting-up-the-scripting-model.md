---
description: Para usar o modelo de script da aquisição de imagens do Windows (WIA), você deve ter o arquivo Wiascr.dll instalado e registrado no computador.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configurando o ambiente de desenvolvimento do modelo de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164524"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>Configurando o ambiente de desenvolvimento do modelo de script

Para usar o modelo de script da aquisição de imagens do Windows (WIA), você deve ter o arquivo Wiascr.dll instalado e registrado no computador.

> [!Note]  
> Este sistema de scripts foi substituído pela camada de automação da WIA (aquisição de imagem do Windows). Consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Copie esse arquivo do SDK do WIA para o diretório *% windir%*/system32 (por exemplo, c \\ : \\ Windows system32). Na linha de comando, navegue até esse diretório e digite **regsvr32 Wiascr.dll**.

Isso insere as informações necessárias no registro do sistema.

Agora você está pronto para usar o modelo de script WIA.

 

 
