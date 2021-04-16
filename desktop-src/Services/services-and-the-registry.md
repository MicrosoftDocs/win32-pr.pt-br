---
description: Um serviço não deve acessar o HKEY \_ Current \_ User ou HKEY \_ classes \_ root, especialmente ao representar um usuário. Em vez disso, use a função RegOpenCurrentUser ou RegOpenUserClassesRoot.
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: Serviços e o registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754111"
---
# <a name="services-and-the-registry"></a>Serviços e o registro

Um serviço não deve acessar o **HKEY \_ Current \_ User** ou **HKEY \_ classes \_ root**, especialmente ao representar um usuário. Em vez disso, use a função [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) ou [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) .

Se você tentar acessar **HKEY \_ Current \_ User** ou **HKEY \_ classes \_ root** de um serviço pode falhar, ou pode parecer funcionar, mas há um vazamento subjacente que pode levar a problemas ao carregar ou descarregar o perfil do usuário.

 

 
