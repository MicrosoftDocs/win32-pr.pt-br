---
title: Sobrecarregando IPropertyNotifySink
description: Sobrecarregando IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4faca0027144498138e1a60bf3df9a29b618aeb7eb09198ff97a3dd7616be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310019"
---
# <a name="overloading-ipropertynotifysink"></a>Sobrecarregando IPropertyNotifySink

muitos contêineres de controle de ActiveX implementam uma janela de navegação de propriedade sem controle. Se as propriedades de um controle forem alteradas por meio das páginas de propriedades do controle, as propriedades do controle poderão ficar fora de sincronia com a exibição do contêiner dessas propriedades (o controle é sempre certo, é claro). para garantir que ele sempre tenha os valores atuais para as propriedades de um controle, um contêiner de controle de ActiveX pode sobrecarregar a interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (associação de dados) e também usá-la para ser notificado de que uma propriedade de controle foi alterada. essa técnica é opcional e não é necessária para ActiveX contêineres de controle ou ActiveX controles.

Observe que um controle deve usar [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) somente para vinculação de dados; é livre usar [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) para uma ou ambas as finalidades.

 

 




