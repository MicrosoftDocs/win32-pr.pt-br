---
title: Usando StoServe
description: StoServe é uma DLL que se destina principalmente como um servidor COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3a220f03e17892b02a94c1e76bafc4a869c0922973c7277589627d233175a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034746"
---
# <a name="using-stoserve"></a>Usando StoServe

**StoServe é** uma DLL que se destina principalmente como um servidor COM. Embora ele possa ser carregado implicitamente vinculando-se ao seu associado. Arquivo LIB, normalmente é usado após uma chamada Explícita de LoadLibrary, geralmente de dentro da função COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **O StoServe** é um servidor em processo de auto-registro.

Para usar **o StoServe**, um programa cliente não precisa incluir STOSERVE. H ou link para STOSERVE. Lib. Um cliente COM do **StoServe** obtém acesso somente por meio dos serviços CLSID e COM do objeto. Para **StoServe**, esse CLSID é CLSID \_ DllPaper (definido no arquivo PAPGUIDS. H no diretório \\ irmão INC). O [exemplo de código StoCl ltda](structured-storage-client-sample--stoclien-.md) mostra como o cliente obtém esse acesso.

O makefile que cria esse exemplo registra automaticamente o servidor no Registro. Você pode iniciar manualmente seu autoregisto em emissão do seguinte comando no prompt de comando no **diretório StoServe:**

**nmake** **register**

Isso pressu que você tenha um ambiente de compilação configurada. Caso não, você também pode invocar diretamente o comando REGISTER.EXE no prompt de comando enquanto estiver no **diretório StoServe.**

**..\\ registrar \\register.exe** **stoserve.dll**

Esses comandos de registro exigem um build anterior do exemplo REGISTER nesta série, bem como um build anterior do STOSERVE.DLL.

Nesta série, os makefiles usam o utilitário REGISTER.EXE do exemplo REGISTER. As versões recentes do SDK (Kit de Desenvolvimento de Software de Plataforma) e Visual C++ incluem um utilitário, REGSVR32.EXE, que pode ser usado de maneira semelhante para registrar servidores em processo e realizar marshaling de DLLs.

**O StoServe** usa muitas das classes e serviços do utilitário fornecidos pelo APPUTIL. Para obter mais detalhes sobre APPUTIL, estudar o código-fonte da biblioteca APPUTIL no diretório APPUTIL irmão e APPUTIL.HTM no diretório principal do tutorial.

 

 