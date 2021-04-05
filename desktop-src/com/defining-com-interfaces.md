---
title: Definição de interfaces COM
description: A Microsoft define muitas interfaces COM. Na maioria dos casos, você pode reutilizar essas interfaces genéricas. No entanto, alguns aplicativos têm requisitos específicos que o tornam desejável ou necessário para definir suas próprias interfaces de objeto.
ms.assetid: 8a94bd7d-d101-411c-97de-9e9a46bf9591
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 516c02a2c337b2c76229094b0e42d75b44f65d16
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084924"
---
# <a name="defining-com-interfaces"></a>Definição de interfaces COM

A Microsoft define muitas interfaces COM. Na maioria dos casos, você pode reutilizar essas interfaces genéricas. No entanto, alguns aplicativos têm requisitos específicos que o tornam desejável ou necessário para definir suas próprias interfaces de objeto.

Todas as interfaces COM devem derivar, direta ou indiretamente, da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Dentro dessa restrição, sua interface personalizada pode dar suporte a praticamente qualquer método ou parâmetro, incluindo métodos assíncronos. Você também pode gerar uma biblioteca de tipos para suas interfaces personalizadas para que os clientes possam acessar informações sobre os métodos do objeto em tempo de execução. Depois de definir uma interface, descreva-a no linguagem IDL da Microsoft (MIDL), compile e registre-a, use-a assim como qualquer interface genérica. Com o Distributed COM, os métodos de interface estão disponíveis para processos remotos e outros processos no mesmo computador.

Por fim, a criação de interfaces COM requer um ambiente de desenvolvimento que inclua um compilador C/C++ e o compilador Midl.exe.

As etapas na criação de uma interface COM são as seguintes:

-   Decida como você deseja fornecer suporte de marshaling para sua interface; com o marshaling controlado por biblioteca de tipos ou com uma DLL de proxy/stub. Mesmo as interfaces em processo devem ser empacotadas se forem usadas em limites de apartamento. É uma boa ideia criar o suporte de marshaling em cada interface COM, mesmo se você não considerar que precisará dela. Consulte [marshaling de interface](interface-marshaling.md) para obter mais informações.
-   Descreva a interface ou as interfaces em um arquivo de definição de interface (IDL). Além disso, você pode especificar determinados aspectos locais de sua interface em um arquivo de configuração de aplicativo (ACF). Se você estiver usando o marshaling controlado por biblioteca de tipos, adicione uma instrução de [**biblioteca**](/windows/desktop/Midl/library) que referencie as interfaces para as quais você deseja gerar informações de tipo.
-   Use o compilador MIDL para gerar um arquivo de biblioteca de tipos e um arquivo de cabeçalho, ou arquivos de proxy/stub de linguagem C, arquivo de identificador de interface, arquivo de dados DLL e arquivo de cabeçalho. Consulte [compilação de MIDL](midl-compilation.md) para obter mais informações.
-   Dependendo do método de marshaling escolhido, grave um arquivo de definição de módulo (DEF), compile e vincule todos os arquivos gerados por MIDL em uma única DLL de proxy e registre a interface no registro do sistema ou registre a biblioteca de tipos. Consulte [carregando e registrando uma biblioteca de tipos](loading-and-registering-a-type-library.md) e [criando e registrando uma DLL de proxy](building-and-registering-a-proxy-dll.md) para obter mais informações.

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

 

 