---
description: Scripts e aplicativos escritos para sistemas operacionais de 32 bits devem continuar sendo executados corretamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Fornecendo dados WMI em uma plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49cb8a7e698723c6d4705a735591097fe7cf354db9684924d58f6b363c0ae6b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992636"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a>Fornecendo dados WMI em uma plataforma de 64 bits

Scripts e aplicativos escritos para sistemas operacionais de 32 bits devem continuar sendo executados corretamente. Se você tiver um provedor de 32 bits existente, poderá avaliar se precisa escrever uma versão de 64 bits para operação lado a lado. Em geral, ambas as versões não são necessárias e a versão de 64 bits pode ser a serviço de clientes locais ou remotos de 32 bits e 64 bits. No entanto, para o modo de compatibilidade do aplicativo de 32 bits, use seu provedor WMI de 32 bits existente em um sistema de 64 bits executado no modo WOW64 de 32 bits.

Em situações raras, os provedores de 32 bits e 64 bits devem ser executados lado a lado em sistemas de 64 bits. Nesse caso, a versão apropriada do provedor que é carregada depende se o chamador é de 32 bits ou 64 bits e local ou remoto. Um chamador que usa os sinalizadores de contexto do objeto de conexão, **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture**, pode solicitar que o WMI carregue um provedor não padrão. Para obter mais informações, [consulte Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).

No caso incomum em que você deve executar os provedores de 32 e 64 bits lado a lado, você deve garantir que os cenários de instalação e desinstalação sejam tratados com cuidado. Isso porque o WMI [](gloss-w.md) tem apenas um repositório e as versões de 32 bits e 64 bits do [**mofcomp.exe**](mofcomp.md) colocam os dados no mesmo repositório; não há nenhuma distinção entre um arquivo .mof de 32 bits ou de 64 bits. Reinstalar uma versão do provedor não prejudicará: os arquivos .mof serão compilados e as classes armazenadas no repositório. No entanto, uma segunda desinstalação que exclui um namespace pode interferir na operação do outro provedor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[Solicitando dados WMI em uma plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[Fornecendo dados ao WMI](providing-data-to-wmi.md)
</dt> </dl>

 

 



