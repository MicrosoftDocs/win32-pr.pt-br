---
title: Configuração (Multimídia do Windows)
description: Saiba como um driver multimídia do Windows pode permitir que os usuários escolham definições de configuração exibindo uma caixa de diálogo de configuração.
ms.assetid: d61d6c8b-8dba-45c2-ba99-0b2111a2d624
keywords:
- drivers instaláveis, configuração
- drivers instaláveis, DRV_CONFIGURE mensagem
- DRV_CONFIGURE mensagem
- DRV_QUERYCONFIGURE mensagem
- Mensagem DRVCONFIGINFO
- configurando drivers instaláveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804e4d92d30d666d4d28c253a1a44572a707daa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403919"
---
# <a name="configuration-windows-multimedia"></a>Configuração (Multimídia do Windows)

Um driver instalável pode permitir que os usuários escolham definições de configuração para o driver e o hardware associado exibindo uma caixa de diálogo de configuração ao processar a mensagem [**DRV \_ CONFIGURE.**](drv-configure.md) O driver é responsável por criar e gerenciar a caixa de diálogo, processar qualquer entrada do usuário na caixa de diálogo e alterar a configuração do driver ou hardware conforme solicitado pelo usuário. O driver deve fornecer um procedimento de caixa de diálogo separado para processar mensagens de janela para a caixa de diálogo e um modelo de caixa de diálogo para definir a aparência e o conteúdo da caixa de diálogo.

Antes de receber a mensagem \_ DRV CONFIGURE, um driver recebe a [**mensagem \_ DRV QUERYCONFIGURE.**](drv-queryconfigure.md) O driver deve retornar um valor que não seja zero para a consulta para garantir o recebimento da mensagem DRV \_ CONFIGURE subsequente.

Ao inicializar a caixa de diálogo de configuração, o driver normalmente recupera informações de configuração do Registro. Para ajudar a localizar essas informações, a mensagem DRV CONFIGURE geralmente inclui o endereço de uma estrutura \_ [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) que contém os nomes da chave do Registro e o valor associados ao driver. Se o usuário solicitar alterações na configuração, o driver deverá atualizar as informações de configuração no Registro.

 

 
