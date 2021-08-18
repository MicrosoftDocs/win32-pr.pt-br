---
title: configuração (Windows multimídia)
description: saiba como um Windows driver de multimídia pode permitir que os usuários escolham definições de configuração exibindo uma caixa de diálogo de configuração.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- drivers instaláveis, configuração
- drivers instaláveis, DRV_CONFIGURE mensagem
- DRV_CONFIGURE mensagem
- DRV_QUERYCONFIGURE mensagem
- Mensagem DRVCONFIGINFO
- Configurando drivers instaláveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1f5079878ba3da60484efb8afccc2effbbd8ec7212dfd339ab0cba5f43653a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144959"
---
# <a name="configuration-windows-multimedia"></a>configuração (Windows multimídia)

Um driver instalável pode permitir que os usuários escolham as definições de configuração para o driver e o hardware associado exibindo uma caixa de diálogo de configuração ao processar a mensagem do [**drv \_ Configure**](drv-configure.md) . O driver é responsável por criar e gerenciar a caixa de diálogo, processar qualquer entrada do usuário na caixa de diálogo e alterar a configuração do driver ou do hardware conforme solicitado pelo usuário. O driver deve fornecer um procedimento de caixa de diálogo separado para processar mensagens de janela para a caixa de diálogo e um modelo de caixa de diálogo para definir a aparência e o conteúdo da caixa de diálogo.

Antes de receber a \_ mensagem de configuração de DRV, um driver recebe a mensagem [**\_ QUERYCONFIGURE drv**](drv-queryconfigure.md) . O driver deve retornar um valor diferente de zero para a consulta para garantir o recebimento da mensagem de configuração de DRV subsequente \_ .

Ao inicializar a caixa de diálogo de configuração, o driver normalmente recupera as informações de configuração do registro. Para ajudar a localizar essas informações, a \_ mensagem de configuração de drv normalmente inclui o endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do registro e o valor associado ao driver. Se o usuário solicitar alterações na configuração, o driver deverá atualizar as informações de configuração no registro.

 

 
