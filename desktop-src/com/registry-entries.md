---
title: Entradas do registro (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Saiba mais sobre: entradas do registro (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089581"
---
# <a name="registry-entries-com"></a>Entradas do registro (COM)

Os valores do registro nas chaves do registro a seguir controlam aspectos da funcionalidade do COM:

-   [**HKEY \_ local \_ Machine \\ software \\ classes**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

A partir do Windows Server 2003, o COM usa apenas o token de processo atual para decidir qual hive de registro deve acessar, não o token de thread. Se COM não for capaz de acessar o hive do registro de perfil do usuário, ele acessará o hive do **\_ \_ \\ sistema do computador local hKey** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
