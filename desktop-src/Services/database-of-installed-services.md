---
description: O SCM mantém um banco de dados dos serviços instalados no registro.
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: Banco de dados dos serviços instalados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922424"
---
# <a name="database-of-installed-services"></a>Banco de dados dos serviços instalados

O SCM mantém um banco de dados dos serviços instalados no registro. O banco de dados é usado pelo SCM e pelos programas que adicionam, modificam ou configuram serviços. A seguir está a chave do registro para este banco de dados: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services**.

Essa chave contém uma subchave para cada serviço instalado e serviço de driver. O nome da subchave é o nome do serviço, conforme especificado pela função [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) quando o serviço foi instalado por um programa de configuração de serviço.

Uma cópia inicial do banco de dados é criada quando o sistema é instalado. O banco de dados contém entradas para os drivers de dispositivo necessários durante a inicialização do sistema. O banco de dados inclui as seguintes informações sobre cada serviço instalado e serviço de driver:

-   O tipo de serviço. Isso indica se o serviço é executado em seu próprio processo ou compartilha um processo com outros serviços. Para serviços de driver, isso indica se o serviço é um driver de kernel ou um driver de sistema de arquivos.
-   O tipo de início. Isso indica se o serviço de serviço ou de driver é iniciado automaticamente na inicialização do sistema (serviço de início automático) ou se o SCM o inicia quando solicitado por um programa de controle de serviço (serviço de início de demanda). O tipo de inicialização também pode indicar que o serviço de serviço ou de driver está desabilitado; nesse caso, ele não pode ser iniciado.
-   O nível de controle de erro. Isso especificará a severidade do erro se o serviço de driver ou o Service falhar ao iniciar durante a inicialização do sistema e determinar a ação que o programa de inicialização executará.
-   O caminho totalmente qualificado do arquivo executável. A extensão do nome do arquivo é. EXE para serviços e. SYS para serviços de driver.
-   Informações de dependência opcionais usadas para determinar a ordem adequada para iniciar serviços ou serviços de driver. Para serviços, essas informações podem incluir uma lista de serviços que o SCM deve iniciar antes de poder iniciar o serviço especificado, o nome de um grupo de ordenação de carga do qual o serviço faz parte e um identificador de marca que indica a ordem de início do serviço em seu grupo de ordenação de carga. Para serviços de driver, essas informações incluem uma lista de drivers que devem ser iniciados antes do driver especificado.
-   Para serviços, um nome de conta e senha opcionais. O programa de serviço é executado no contexto desta conta. Se nenhuma conta for especificada, o serviço será executado no contexto da [conta LocalSystem](localsystem-account.md).
-   Para serviços de driver, um nome de objeto de driver opcional (por exemplo, o sistema de \\ arquivos \\ rdr ou \\ XNS de driver \\ ), usado pelo sistema de e/s para carregar o driver de dispositivo. Se nenhum nome for especificado, o sistema de e/s criará um nome padrão com base no nome do serviço de driver.

> [!Note]  
> Esse banco de dados também é conhecido como o banco de dados ServicesActive ou o banco de dados SCM. Você deve usar as funções fornecidas pelo SCM, em vez de modificar o banco de dados diretamente.

 

 

 



