---
title: Controlando a visibilidade do objeto
description: Active Directory Domain Services fornecem a capacidade de ocultar objetos de usuários que foram negados determinados direitos.
ms.assetid: 3a65ec79-7de0-4d14-b980-1ca6a972ac70
ms.tgt_platform: multiple
keywords:
- controlando a visibilidade do objeto Active Directory
- Active Directory Active Directory, usando, controlando a visibilidade do objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b1ab364f0711174d5ac1dd1e4fbe98303c50b3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007347"
---
# <a name="controlling-object-visibility"></a>Controlando a visibilidade do objeto

Active Directory Domain Services fornecem a capacidade de ocultar objetos de usuários que foram negados determinados direitos. Se um objeto estiver oculto, um aplicativo que está sendo executado com as credenciais de um usuário não poderá enumerar ou se associar ao objeto.

Se um usuário receber o direito de controle de acesso à [**\_ lista do AD \_ ACTRL \_ DS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) diretamente em um contêiner, o usuário poderá exibir qualquer um dos objetos filho do contêiner. Da mesma forma, se um usuário tiver negado o direito de controle de acesso à **\_ lista do AD \_ ACTRL \_ DS \_** diretamente em um contêiner, o usuário não poderá exibir nenhum dos objetos filho do contêiner. Isso permite que o conteúdo de contêineres inteiros seja ocultado.

O servidor de Active Directory também pode ser colocado em um modo de objeto de lista especial definindo o terceiro caractere da propriedade [**dsHeuristics**](/windows/desktop/ADSchema/a-dsheuristics) como "1". O modo de objeto de lista pode ser desabilitado definindo o terceiro caractere da propriedade **dsHeuristics** como "0". Quando o servidor de Active Directory estiver no modo de objeto de lista, um objeto ainda estará visível se o usuário tiver recebido o [**direito \_ \_ ACTRL \_ DS da \_ lista do AD**](/windows/win32/api/iads/ne-iads-ads_rights_enum) no objeto pai. No entanto, se o usuário tiver negado o direito de **lista de AD \_ \_ ACTRL \_ DS \_** no pai, os objetos filho específicos ainda poderão se tornar visíveis se o usuário receber **o \_ \_ objeto de \_ lista \_ DS direito do ADS** diretamente nos objetos pai e filho. O modo de objeto de lista permite que o administrador do sistema conceda ou negue acesso a objetos individuais para usuários ou grupos. O modo de objeto de lista deve ser usado com moderação porque requer um número significativamente maior de chamadas de verificação de acesso a serem feitas pelo serviço de diretório para determinar se um objeto está visível para um usuário. Portanto, ele pode ter um efeito negativo sobre o desempenho de navegação ou leitura de objetos de Active Directory Domain Services.

 

 