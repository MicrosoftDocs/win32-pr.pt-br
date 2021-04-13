---
title: Run-Time vincular a Wtsapi32.dll
description: Seu aplicativo pode usar a API Serviços de Área de Trabalho Remota para vincular dinamicamente ao Wtsapi32.dll em tempo de execução. Para fazer isso, seu aplicativo deve chamar a função LoadLibrary para carregar Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366407"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time vincular a Wtsapi32.dll

Se o seu aplicativo for executado em um ambiente que não seja um Serviços de Área de Trabalho Remota ambiente, mas você quiser que seu aplicativo forneça funcionalidade adicional quando ele for executado em um ambiente de Serviços de Área de Trabalho Remota, o aplicativo poderá usar a API do Serviços de Área de Trabalho Remota para implementar a funcionalidade adicional e vincular dinamicamente a Wtsapi32.dll em tempo de execução. Para fazer isso, seu aplicativo deve chamar a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar Wtsapi32.dll. Se a chamada **LoadLibrary** falhar, seu aplicativo poderá ser executado usando sua funcionalidade básica. Se **LoadLibrary** for executado com sucesso, seu aplicativo poderá chamar a função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para recuperar ponteiros para as funções de serviços de área de trabalho remota que você deseja chamar.

Se seu aplicativo for destinado apenas a um ambiente de Serviços de Área de Trabalho Remota, a vinculação dinâmica não será necessária. Nesse caso, você pode incluir Wtsapi32. h e vincular com Wtsapi32. lib. Em seguida, se seu aplicativo for iniciado em um ambiente diferente de Serviços de Área de Trabalho Remota, ele será encerrado porque Wtsapi32.dll não está presente.

Para obter informações sobre como determinar se seu aplicativo está sendo executado em um ambiente de Serviços de Área de Trabalho Remota, consulte [detectando o ambiente de serviços de área de trabalho remota](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes gerais de programação](general-programming-guidelines.md)
</dt> </dl>

 

 