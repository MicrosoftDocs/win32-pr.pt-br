---
description: Windows O instalador implementa vários controles padrão que os autores do pacote podem colocar nas caixas de diálogo. No entanto, nem todos os controles padrão do Microsoft Windows estão disponíveis e os controles personalizados não podem ser criados para uso com a interface do usuário do instalador.
ms.assetid: 28416905-ce9a-4bb7-97b7-646c01f370ab
title: Visão geral dos controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee9d03f0f21f9cc0611a1fae4831b6ccbbda9f40eda873cdf4c26b259ec43f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638518"
---
# <a name="controls-overview"></a>Visão geral dos controles

Windows O instalador implementa vários controles padrão que os autores do pacote podem colocar nas caixas de diálogo. No entanto, nem todos os controles padrão do Microsoft Windows estão disponíveis e os controles personalizados não podem ser criados para uso com a interface do usuário do instalador.

Os controles são criados em caixas de diálogo no instalador de maneira semelhante a como as caixas de diálogo são criadas programaticamente usando a API de interface do usuário do Microsoft Windows. Um controle é criado a partir de um modelo registrado na tabela Controle. Esse modelo é ligeiramente diferente, já que ele contém o nome exclusivo da caixa de diálogo na qual o controle aparece.

Na API de interface do usuário do Microsoft Windows, a interação do usuário é realizada criando uma função de retorno de chamada para manipular mensagens postadas pelo controle . Além disso, a maioria dos Windows microsoft recebe mensagens, como aquelas enviadas pela [função SendMessage.](/windows/win32/api/winuser/nf-winuser-sendmessage)

A comunicação entre o usuário e os controles é realizada no instalador por meio do uso de [ControlEvents](controlevent-overview.md). No entanto, há um conjunto limitado de ControlEvents que são específicos para cada controle no conjunto limitado de controles no Windows Instalador. Os controles podem postar mais de um ControlEvent e podem receber mais de um ControlEvent.

Os controles podem publicar controlEvents específicos por meio do uso da tabela ControlEvent. Os controles podem receber ControlEvents por meio do uso da [tabela EventMapping](eventmapping-table.md).

Windows O instalador publica ControlEvents durante a execução de algumas ações também e os controles inscritos nesses ControlEvents na tabela EventMapping os recebem.

 

 
