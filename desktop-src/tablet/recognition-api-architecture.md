---
description: Um aplicativo habilitado para tinta se comunica com o sistema de reconhecimento por meio das APIs da plataforma Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Arquitetura da API de reconhecimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565097"
---
# <a name="recognition-api-architecture"></a>Arquitetura da API de reconhecimento

Um aplicativo habilitado para tinta se comunica com o sistema de reconhecimento por meio das APIs da plataforma Tablet PC. Os aplicativos usam o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para fazer isso. A plataforma do Tablet PC interage com o reconhecedor usando as interfaces do estilo C documentadas nesta seção. Na ilustração a seguir, a área dentro da linha tracejada mostra o que está documentado nesta seção.

![ilustração de arquitetura de reconhecimento com reconhecedor realçado](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Um reconhecedor personalizado deve incluir recapitular. h (instalado por padrão em C: \\ arquivos de programas que \\ o Microsoft Tablet PC Platform SDK \\ inclui). Exceto quando observado, sua DLL (biblioteca de vínculo dinâmico) deve exportar todas as funções de API, mesmo que você opte por ter algumas delas retorna E \_ NOTIMPL.

Sob nenhuma circunstância o reconhecedor será chamado diretamente por um aplicativo habilitado para tinta. Em vez disso, os aplicativos chamarão as APIs de automação ou as APIs gerenciadas para obter os resultados do reconhecedor.

 

 



