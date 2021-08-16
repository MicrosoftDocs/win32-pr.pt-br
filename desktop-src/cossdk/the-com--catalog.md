---
description: O catálogo COM+ armazena atributos de aplicativo COM+, atributos de classe e atributos no nível do computador. Ele garante a consistência entre esses atributos e fornece operações comuns sobre esses atributos.
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

O catálogo COM+ armazena atributos de aplicativo COM+, atributos de classe e atributos no nível do computador. Ele garante a consistência entre esses atributos e fornece operações comuns sobre esses atributos.

O catálogo COM+ usa duas lojas diferentes, da seguinte maneira:

-   O banco de dados de registro COM+
-   O Windows de dados (**HKEY \_ CLASSES \_ ROOT**)

O catálogo apresenta uma exibição lógica unificada desses dois armazenamentos e os expõe por meio da Biblioteca de Administração COM+. Essa biblioteca fornece, por meio de uma linguagem de script, todas as funcionalidades da ferramenta administrativa dos Serviços de Componentes.

Para componentes COM existentes que não exigem novos serviços COM+, a busca ocorre no registro Windows existente. O catálogo COM+ também usa o registro Windows para a biblioteca de tipos e o registro de proxy/stub de interface.

## <a name="split-registration"></a>Dividir o registro

Para novos componentes que, na verdade, já são componentes COM existentes que são usados no ambiente de serviços (por exemplo, componentes do MTS), o aspecto COM básico do registro é armazenado no registro do Windows e novos serviços e atributos (por exemplo, componentes na fila) são armazenados no banco de dados de registro COM+. Isso é conhecido como um *registro dividido.*

Cada atributo é armazenado em apenas um local: o registro Windows ou o banco de dados de registro COM+. Novos componentes COM são registrados exclusivamente no banco de dados de registro COM+, com alguma duplicação no registro Windows para que as ferramentas existentes possam usá-los.

## <a name="transactional-updates-to-the-catalog"></a>Atualizações transacionais para o catálogo

Algumas operações no catálogo são executadas de maneira transacional. Quando você invoca a Biblioteca de Administração COM+ de um componente transacional, as atualizações para o banco de dados de registro COM+ ocorrerão dentro do limite de transação do componente de chamada.

No entanto, não há garantia de que as atualizações que envolvem alterações em outros armazenamentos (como o sistema de arquivos e Windows registro) sejam totalmente transacionais. Uma transação anulada pode deixar esses armazenamentos em um estado inconsistente com as alterações feitas entre si ou no banco de dados de registro COM+.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando pacotes de instalação para aplicativos COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Implantando proxies de aplicativo](deploying-application-proxies.md)
</dt> <dt>

[O utilitário de replicação COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



