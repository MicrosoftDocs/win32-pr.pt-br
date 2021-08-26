---
title: Definição de interfaces COM
description: A Microsoft define muitas interfaces COM. Na maioria dos casos, você pode reutilizar essas interfaces genéricas. No entanto, alguns aplicativos têm requisitos específicos que o torna desejável ou necessário definir suas próprias interfaces de objeto.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e676172e51fca810f0cbb7ba93b5d52b814319b6e8b890f20ba9c51617f7ac2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071016"
---
# <a name="defining-com-interfaces"></a>Definição de interfaces COM

A Microsoft define muitas interfaces COM. Na maioria dos casos, você pode reutilizar essas interfaces genéricas. No entanto, alguns aplicativos têm requisitos específicos que o torna desejável ou necessário definir suas próprias interfaces de objeto.

Todas as interfaces COM devem derivar, direta ou indiretamente, da interface [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) Dentro dessa restrição, sua interface personalizada pode dar suporte a praticamente qualquer método ou parâmetro, incluindo métodos assíncronos. Você também pode gerar uma biblioteca de tipos para suas interfaces personalizadas para que os clientes possam acessar informações sobre os métodos do objeto em tempo de operação. Depois de definir uma interface, descreva-a linguagem IDL da Microsoft (MIDL), compile-a e registre-a, assim como qualquer interface genérica. Com o COM distribuído, os métodos de interface estão disponíveis para processos remotos e para outros processos no mesmo computador.

Por fim, a criação de interfaces COM requer um ambiente de desenvolvimento que inclui um compilador C/C++ e o Midl.exe compilador.

As etapas na criação de uma interface COM são as seguintes:

-   Decida como você deseja fornecer suporte de marshaling para sua interface; seja com marshaling orientado por biblioteca de tipos ou com uma DLL proxy/stub. Até mesmo as interfaces em processo devem ser marshaladas se elas devem ser usadas entre limites de apartment. É uma boa ideia criar o suporte de marshaling em cada interface COM, mesmo que você não pense que precisará dele. Consulte [Marshaling de interface](interface-marshaling.md) para obter mais informações.
-   Descreva a interface ou interfaces em um arquivo de IDL (definição de interface). Além disso, você pode especificar determinados aspectos locais da interface em um arquivo de configuração de aplicativo (ACF). Se você estiver usando marshaling orientado [](/windows/desktop/Midl/library) por biblioteca de tipos, adicione uma instrução de biblioteca que faz referência às interfaces para as quais você deseja gerar informações de tipo.
-   Use o compilador MIDL para gerar um arquivo de biblioteca de tipos e um arquivo de header ou arquivos proxy/stub da linguagem C, arquivo de identificador de interface, arquivo de dados DLL e arquivo de header. Consulte [Compilação MIDL](midl-compilation.md) para obter mais informações.
-   Dependendo do método de marshaling escolhido, escreva um arquivo DEF (definição de módulo), compile e vincule todos os arquivos gerados por MIDL em uma única DLL de proxy e registre a interface no registro do sistema ou registre a biblioteca de tipos. Consulte [Carregando e registrando uma biblioteca de tipos](loading-and-registering-a-type-library.md) e criando e [registrando uma DLL de proxy](building-and-registering-a-proxy-dll.md) para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anatomia de um arquivo IDL](anatomy-of-an-idl-file.md)
</dt> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Regras de design de interface](interface-design-rules.md)
</dt> <dt>

[O Component Object Model](the-component-object-model.md)
</dt> </dl>

 

 