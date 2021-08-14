---
description: O catálogo COM+ armazena atributos de aplicativo COM+, atributos de classe e atributos de nível de computador. Ele garante a consistência entre esses atributos e fornece operações comuns sobre esses atributos.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: O catálogo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b345c45fddab245c1e2290dc279742ac7b3b6b25c093d677c74b232077b43ae1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305263"
---
# <a name="the-com-catalog"></a>O catálogo COM+

O catálogo COM+ armazena atributos de aplicativo COM+, atributos de classe e atributos de nível de computador. Ele garante a consistência entre esses atributos e fornece operações comuns sobre esses atributos.

O catálogo COM+ usa dois repositórios diferentes, da seguinte maneira:

-   O banco de dados de registro do COM+
-   o registro de Windows **( \_ classe HKEY CLASSES \_ raiz**)

O catálogo apresenta uma exibição lógica e unificada dessas duas lojas e as expõe por meio da biblioteca de administração do COM+. Essa biblioteca fornece, por meio de uma linguagem de script, toda a funcionalidade da ferramenta administrativa serviços de componentes.

para componentes COM existentes que não exigem novos serviços COM+, a pesquisa ocorre no registro de Windows existente. o catálogo COM+ também usa o registro de Windows para o registro de biblioteca de tipos e proxy de interface/stub.

## <a name="split-registration"></a>Dividir registro

para novos componentes que realmente já são componentes COM que são usados no ambiente de serviços (por exemplo, componentes do MTS), o aspecto de COM básico do registro é armazenado no registro de Windows e novos serviços e atributos (por exemplo, componentes na fila) são armazenados no banco de dados de registro do COM+. Isso é conhecido como um *registro de divisão*.

cada atributo é armazenado em apenas um local: o registro de Windows ou o banco de dados de registro do COM+. os novos componentes COM são registrados exclusivamente no banco de dados de registro do COM+, com alguma duplicação no registro de Windows para que as ferramentas existentes possam usá-los.

## <a name="transactional-updates-to-the-catalog"></a>Atualizações transacionais para o catálogo

Algumas operações no catálogo são executadas de forma transacional. Quando você invoca a biblioteca de administração COM+ de um componente transacional, as atualizações para o banco de dados de registro do COM+ ocorrerão dentro do limite de transação do componente de chamada.

no entanto, as atualizações que envolvem alterações em outras lojas (como o sistema de arquivos e o registro de Windows) não têm garantia de serem totalmente transacionais. Uma transação anulada pode deixar esses repositórios em um estado inconsistente com as alterações feitas entre si ou com o banco de dados de registro do COM+.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando pacotes de instalação para aplicativos COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Implantando proxies de aplicativo](deploying-application-proxies.md)
</dt> <dt>

[O utilitário de replicação COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



