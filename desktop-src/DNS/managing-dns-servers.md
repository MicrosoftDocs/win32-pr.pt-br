---
title: Gerenciando servidores DNS
description: Saiba mais sobre como gerenciar servidores DNS. Um Servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: 9ac68e35-112a-44d3-918d-2caea47b6e52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccce0b6c4a292e2fe46ec8584a601deee9267d2c5f1bfdeebaefa05db630f437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433376"
---
# <a name="managing-dns-servers"></a>Gerenciando servidores DNS

Um Servidor DNS é um computador que conclui o processo de resolução de nomes no DNS. Os Servidores DNS contêm arquivos, chamados *arquivos de zona,* que permitem resolver nomes para endereços IP (ou vice-versa). Quando consultado, um servidor DNS responde de uma das três maneiras:

-   O servidor retorna as informações de resolução de nome ou resolução de IP solicitadas.
-   O servidor retorna um ponteiro para outro servidor DNS que pode fazer o serviço da solicitação.
-   O servidor indica que ele não tem as informações solicitadas.

Os Servidores DNS podem, durante a preparação para retornar as informações de resolução solicitadas, consultar outros servidores DNS. Mas além disso, os Servidores DNS não executam nenhuma operação diferente daquelas mencionadas na lista anterior.

Há três tipos principais de servidores DNS : servidores primários, servidores secundários e servidores de cache. Consulte [Servidores DNS](dns-servers.md) para obter mais informações sobre esses servidores DNS.

## <a name="administration-steps"></a>Etapas de administração

O provedor WMI DNS permite a administração de servidores DNS do próprio servidor ou de hosts remotos. As etapas gerais necessárias para administrar um servidor DNS usando o provedor WMI DNS são:

-   Conectando-se ao provedor WMI DNS
-   Obter uma instância de servidor
-   Listando ou modificando uma propriedade de servidor ou usando um método

Para ilustrar como implementar essas etapas de administração, são fornecidos exemplos. As tarefas a seguir estão vinculadas a seus exemplos de script associados.

-   [Interrompendo um servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Iniciando um servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Reiniciando um servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Adicionando um endereço IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Removendo um endereço IP](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Listando propriedades do servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Exibindo tipos de propriedade do servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)
-   [Modificando propriedades do servidor DNS](dns-wmi-provider-samples-managing-a-dns-server.md)

 

 




