---
description: Se essa política de sistema por computador estiver definida como &\# 0034;1&0034;, o instalador não solicitará aos usuários quando os scripts em uma página da Web usarem a interface de automação do \# instalador.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9a78bded284a687994075fdda1276122df2ab68716c4aaf759b4f5750aeb15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990146"
---
# <a name="safeforscripting"></a>SafeForScripting

Se essa política [](system-policy.md) de sistema por computador estiver definida como "1", o instalador não solicitará aos usuários quando os scripts em uma página da Web usarem a interface de automação [do instalador.](automation-interface.md)

Antes de definir essa política, você deve considerar se o prompt de usuário anterior fornece um nível apropriado de segurança para seus usuários. Se essa política não estiver definida, quando um script hospedado por um navegador da Internet tentar instalar um aplicativo, o sistema avisará o usuário e pedirá que ele aceite ou recuse a instalação. Definir SafeForScripting suprime esse aviso e pode permitir a instalação de aplicativos no sistema sem o conhecimento do usuário. Essa política pode ser útil para uma empresa que usa ferramentas baseadas na Web para distribuir programas.

Para obter mais informações, consulte Diretrizes para a autor de instalações [seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas](digital-signatures-and-windows-installer.md) digitais e Windows instalador e download de uma instalação da [Internet.](downloading-an-installation-from-the-internet.md)

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ Instalador \_ do** Microsoft machine \\ **software** \\ **policies** \\  \\ **microsoft Windows** \\ 

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



