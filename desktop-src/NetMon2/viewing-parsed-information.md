---
description: O Visualizador de quadros Monitor de Rede exibe dados analisados em três painéis.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Exibindo informações analisadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557312"
---
# <a name="viewing-parsed-information"></a>Exibindo informações analisadas

O Visualizador de quadros Monitor de Rede exibe dados analisados em três painéis. O painel superior exibe um resumo do quadro que inclui o protocolo identificado. O painel central exibe as propriedades de dados formatados que podem ser organizadas hierarquicamente como parte da exibição do analisador. O painel inferior exibe dados brutos realçados selecionados no painel central.

Você pode especificar como as informações no visualizador são exibidas quando você desenvolve seu próprio analisador. A ilustração a seguir mostra como as informações podem ser exibidas no Visualizador de quadros Monitor de Rede.

![Visualizador de quadros do monitor de rede](images/parseui.png)

> [!Note]  
> Os analisadores não exibem quadros. Os analisadores reconhecem os campos nas informações fornecidas e, em seguida, notificam Monitor de Rede para exibir o quadro. A filtragem é uma operação de nível superior que permite filtrar consultas para abranger analisadores.

 

No analisador, use apenas as funções que podem ser executadas em aplicativos Microsoft Win32. Antes de anexar Propriedades aos dados brutos, um analisador deve primeiro registrar todas as propriedades possíveis com o kernel Monitor de Rede. O analisador envia uma mensagem ao kernel para criar um banco de dados de propriedade e, em seguida, preenche o banco de dados de propriedades com cada propriedade possível para seu protocolo. Cada propriedade no banco de dados de propriedades contém informações como uma descrição textual, um tipo de dado e um qualificador que são usados para formatar os dados brutos e uma rotina de formatação usada para exibir os dados.

 

 



