---
title: Usando StoServe
description: StoServe é uma DLL que se destina principalmente a um servidor COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754485"
---
# <a name="using-stoserve"></a>Usando StoServe

**StoServe** é uma DLL que se destina principalmente a um servidor com. Embora ele possa ser carregado implicitamente, vinculando-se ao seu associado. Arquivo LIB, normalmente é usado após uma chamada LoadLibrary explícita, geralmente de dentro da função COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject). **StoServe** é um servidor em processo de registro automático.

Para usar o **StoServe**, um programa cliente não precisa incluir o StoServe. H ou link para STOSERVE. LIB. Um cliente COM do **StoServe** obtém acesso exclusivamente por meio do CLSID e dos serviços com do seu objeto. Para **StoServe**, esse CLSID é CLSID \_ DllPaper (definido no arquivo PAPGUIDS. H no \\ diretório irmão Inc. O exemplo de código [StoClien](structured-storage-client-sample--stoclien-.md) mostra como o cliente obtém esse acesso.

O makefile que cria esse exemplo registra automaticamente o servidor no registro. Você pode iniciar manualmente seu auto-registro emitindo o seguinte comando no prompt de comando no diretório **StoServe** :

 **registro** de NMAKE

Isso pressupõe que você tenha um ambiente de compilação configurado. Caso contrário, você também pode invocar diretamente o comando REGISTER.EXE no prompt de comando enquanto estiver no diretório **StoServe**

**..\\ registrar \\register.exe** **stoserve.dll**

Esses comandos de registro exigem uma compilação anterior do exemplo de registro nesta série, bem como uma compilação anterior do STOSERVE.DLL.

Nesta série, os makefiles usam o utilitário REGISTER.EXE do exemplo de registro. As versões recentes do SDK (Kit de desenvolvimento de software) de plataforma e Visual C++ incluem um utilitário, REGSVR32.EXE, que pode ser usado de forma semelhante para registrar servidores em processo e realizar marshaling de DLLs.

O **StoServe** usa muitos dos serviços e classes de utilitário fornecidos pelo APPUTIL. Para obter mais detalhes sobre o APPUTIL, estude o código-fonte da biblioteca APPUTIL no diretório APPUTIL irmão e APPUTIL.HTM no diretório principal do tutorial.

 

 