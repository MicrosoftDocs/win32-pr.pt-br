---
title: Licenciamento e IClassFactory2
description: Licenciamento e IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9376d5187588ba14da434161309409bf1d189a8f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366767"
---
# <a name="licensing-and-iclassfactory2"></a>Licenciamento e IClassFactory2

A interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) em um objeto de classe fornece o mecanismo básico de criação de objeto de com. Usando **IClassFactory**, um servidor pode controlar a criação de objetos em uma base de máquina. A implementação do método [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) pode permitir ou impedir a criação de objetos com base na existência de uma licença de computador. Uma licença de computador é uma informação separada do aplicativo que existe em um computador para indicar que o software foi instalado de uma fonte válida, como os discos de instalação do fornecedor. Se a licença do computador não existir, o servidor poderá impedir a criação do objeto. O licenciamento de máquina impede a pirataria em casos em que um usuário tenta copiar o software de um computador para outro, pois as informações de licença não são copiadas com o software e o computador que recebe a cópia não é licenciado.

No entanto, em um setor de software de componente, os fornecedores precisam de um nível mais preciso de controle sobre o licenciamento. Além do controle de licença de computador, um fornecedor precisa permitir que alguns clientes criem um objeto de componente ao mesmo tempo que nega a outros clientes o mesmo recurso. Isso requer que o aplicativo cliente obtenha uma chave de licença do componente enquanto o aplicativo cliente ainda está em desenvolvimento. O aplicativo cliente usa a chave de licença em tempo de execução para criar objetos em um computador sem licença.

Por exemplo, se um fornecedor fornecer uma biblioteca de controles para desenvolvedores, o desenvolvedor que adquire a biblioteca terá uma licença completa do computador, permitindo que os objetos sejam criados no computador de desenvolvimento. O desenvolvedor pode então criar um aplicativo cliente na máquina licenciada que incorpora um ou mais dos controles. Quando o aplicativo cliente resultante é executado em outro computador, os controles usados no aplicativo cliente devem ser criados no outro computador mesmo se esse computador não possuir uma licença de computador para os controles do fornecedor original.

A interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) fornece esse nível de controle. Para permitir o licenciamento baseado em chave para qualquer componente específico, você implementa **IClassFactory2** no objeto de fábrica de classes para esse componente. **IClassFactory2** é derivado de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), portanto, ao implementar **IClassFactory2**, o objeto de fábrica de classes atende aos requisitos de com básicos.

Para incorporar um componente licenciado ao seu aplicativo cliente, use os seguintes métodos no [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2):

-   O método [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) preenche uma estrutura [**LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo) com informações que descrevem o comportamento de licenciamento da fábrica de classes. Por exemplo, a fábrica de classes pode fornecer chaves de licença para licenciamento em tempo de execução se o membro **fRunTimeKeyAvail** for **true**.
-   O método [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) fornece uma chave de licença para o componente. Uma licença de computador deve estar disponível quando o cliente chama esse método.
-   O método [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) cria uma instância do componente licenciado se o parâmetro de chave de licença (BSTRÂ bstrKey) for válido.

> [!Note]  
> Em suas informações de tipo, um componente usa o atributo licenciado para marcar a coclasse que dá suporte a licenciamento por meio de [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2).

 

Primeiro, você precisa de uma ferramenta de desenvolvimento separada que também seja um cliente do componente licenciado. A finalidade dessa ferramenta é obter a chave de licença em tempo de execução e salvá-la em seu aplicativo cliente. Essa ferramenta é executada somente em um computador que possui uma licença de computador para o componente. A ferramenta chama os métodos [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) e [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) para obter a chave de licença de tempo de execução e salva a chave de licença em seu aplicativo cliente. Por exemplo, a ferramenta de desenvolvimento pode criar um arquivo de cabeçalho (. h) contendo a chave de licença BSTR e, em seguida, você deve incluir esse arquivo. h em seu aplicativo cliente.

Para instanciar o componente em seu aplicativo cliente, primeiro tente instanciar o objeto diretamente com [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance). Se **CreateInstance** for bem sucedido, a segunda máquina será licenciada para o componente e os objetos poderão ser criados ao mesmo tempo. Se **CreateInstance** falhar com a classe de código de retorno \_ E não \_ licenciado, a única maneira de criar o objeto é passar a chave de tempo de execução para o método [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) . **CreateInstanceLic** verifica a chave e cria o objeto se a chave for válida.

Dessa forma, um aplicativo criado com componentes (como controles) pode ser executado em um computador que não tem nenhuma outra licença — somente o aplicativo cliente que contém a licença de tempo de execução tem permissão para criar os objetos de componente em questão.

A interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) dá suporte à flexibilidade em esquemas de licenciamento. Por exemplo, o implementador de servidor pode criptografar as chaves de licença no componente para aumentar a segurança. Os implementadores de servidor também podem habilitar ou desabilitar níveis de funcionalidade em seus objetos, fornecendo chaves de licença diferentes para funções diferentes. Por exemplo, uma chave pode permitir um nível básico de funcionalidade, enquanto outra permite a funcionalidade básica e avançada, e assim por diante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Responsabilidades do servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 