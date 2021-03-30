---
title: Gerenciando servidores DNS
description: Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe97e8b8b02e9d2198e49d0574b2d3fb8bc87df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636544"
---
# <a name="managing-dns-servers"></a>Gerenciando servidores DNS

Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS. Os servidores DNS contêm arquivos, chamados de *arquivos de zona*, que permitem que eles resolvam nomes para endereços IP (ou vice-versa). Quando consultado, um servidor DNS responde de uma destas três maneiras:

-   O servidor retorna a resolução de nome ou as informações de resolução de IP solicitadas.
-   O servidor retorna um ponteiro para outro servidor DNS que pode atender à solicitação.
-   O servidor indica que ele não tem as informações solicitadas.

Os servidores DNS podem, durante o curso de preparação, retornar as informações de resolução solicitadas, consultar outros servidores DNS. Mas, além disso, os servidores DNS não executam nenhuma operação diferente daquelas mencionadas na lista anterior.

Há três tipos principais de servidores DNS – servidores primários, servidores secundários e servidores de cache. Consulte [servidores DNS](dns-servers.md) para obter mais informações sobre esses servidores DNS.

## <a name="administration-steps"></a>Etapas de administração

O provedor WMI de DNS permite a administração de servidores DNS a partir do próprio servidor ou de hosts remotos. As etapas gerais necessárias para administrar um servidor DNS usando o provedor WMI de DNS são:

-   Conectando-se ao provedor WMI de DNS
-   Obtendo uma instância de servidor
-   Listando ou modificando uma propriedade de servidor ou usando um método

Para ilustrar como implementar essas etapas de administração, são fornecidos exemplos. As tarefas a seguir estão vinculadas a seus exemplos de script associados.

-   [Interrompendo um servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Iniciando um servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Reiniciando um servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Adicionando um endereço IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Removendo um endereço IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Listando propriedades do servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Exibindo tipos de Propriedade do servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Modificando Propriedades do servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




