---
description: O serviço Distributed Link Tracking permite que os aplicativos cliente acompanhem as fontes de link que foram movidas.
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: Rastreamento de link distribuído e identificadores de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d28e151c21fd5320a41950be7647c1e8e0a88b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105757160"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>Rastreamento de link distribuído e identificadores de objeto

O armazenamento de uma referência a um arquivo ou diretório usando seu caminho e nome de arquivo não é confiável. Se um usuário renomear um arquivo, ele interromperá os links para o arquivo. Se um usuário renomear o diretório, ele interromperá os links para o arquivo e todos os arquivos e subdiretórios na árvore de diretórios.

O **serviço Distributed Link Tracking** permite que os aplicativos cliente acompanhem as fontes de link que foram movidas. Os clientes que assinam o serviço de rastreamento de link podem manter a integridade de suas referências e os objetos podem ser rastreados de forma transparente para o usuário.

## <a name="object-identifiers"></a>Identificadores de objeto

O serviço de rastreamento de link mantém seu vínculo com um objeto usando um **identificador de objeto (ID)**. Uma ID de objeto é um atributo opcional que identifica exclusivamente um arquivo ou diretório em um volume.

Um índice de todas as IDs de objeto é armazenado no volume. As operações de renomeação, backup e restauração preservam as IDs de objeto. No entanto, as operações de cópia não preservam as IDs de objeto, pois isso violaria sua exclusividade.

Você pode executar as seguintes operações em IDs de objeto:

-   Criação
-   Exclusão
-   Consulta

Ao criar uma ID de objeto, você estabelece a identidade do arquivo para o serviço de rastreamento de link. Por outro lado, quando você exclui uma ID de objeto, o serviço de rastreamento de link para de manter os links para o arquivo. Para obter uma lista dos códigos de controle do sistema de arquivos que executam operações em IDs de objeto, consulte [códigos de controle de gerenciamento de arquivos](file-management-control-codes.md).

O serviço Distributed Link Tracking rastreia fontes de link para atalhos de shell e vínculos OLE em volumes do sistema de arquivos NTFS. O link cliente pode corrigir um link desfeito com informações atualizadas no novo local da origem do link.

## <a name="link-tracking-features"></a>Recursos de rastreamento de link

Os atalhos do Shell incluem o controle de link heurístico que usa um algoritmo de pesquisa de árvore para encontrar uma correspondência para uma origem do link movido. O algoritmo de pesquisa é baseado no último caminho conhecido das informações de arquivo e arquivo que inclui a data de criação, o tamanho do arquivo e o nome e a extensão do arquivo.

A vinculação OLE inclui o mesmo controle de link heurístico. O Windows também inclui o mesmo controle de link heurístico com algumas melhorias adicionadas para a pesquisa de espaços de nome para gerar resultados em alguns cenários comuns. Os aprimoramentos incluem o procedimento a seguir que depende dos limites de tempo impostos por um aplicativo cliente.

**Para procurar por espaços de nome**

1.  Pesquise quatro níveis de diretório abaixo do último diretório.
2.  Mova um diretório para cima e repita as etapas 1 e 2 outra três vezes, o que pode gerar resultados se o objeto tiver sido movido para a proximidade.
3.  Pesquise quatro níveis abaixo da raiz da área de trabalho, o que pode gerar resultados se o objeto tiver sido movido para um local na mesma área de trabalho.
4.  Pesquise quatro níveis abaixo da raiz em cada unidade fixa local.
5.  Repita as etapas de 4 a 1-3 sem o limite de quatro diretórios.

> [!Note]  
> Esses esquemas de rastreamento de link são transparentes para o usuário final. No entanto, eles nem sempre geram resultados positivos e podem ser demorados.

 

Para obter mais informações sobre atalhos do Shell, consulte [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).

Para obter mais informações sobre links OLE, consulte [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).

Se um link for feito em um arquivo no NTFS 3,0 ou posterior, e o arquivo for movido para qualquer outro volume com NTFS 3,0 ou posterior no mesmo domínio, o arquivo poderá ser encontrado pelo serviço de controle, sujeito a considerações de tempo. Além disso, se o arquivo for movido para fora do domínio ou dentro de um grupo de trabalho, ele será encontrado.

Para obter a versão NTFS de um volume, abra um prompt de comando com direitos de acesso de administrador e execute o seguinte comando:

**fsutil fsinfo ntfsinfo** *X ** * *:*

em que *X* é a letra da unidade do volume.

Quando um link é criado para um arquivo, o arquivo de destino é considerado a **origem do link** e o criador do link é o **cliente do link**. Por exemplo, se um atalho do Shell for criado para vincular a um documento de texto, o documento de texto será a origem do link e o atalho do shell será o link cliente.

O serviço Distributed Link Tracking mantém links de arquivos para as seguintes situações que ocorrem em um domínio:

-   O arquivo de origem do link é movido de um volume do sistema de arquivos NTFS para outro dentro do mesmo domínio.
-   O nome do computador que contém a origem do link é renomeado.
-   Os compartilhamentos de rede no computador de origem do link são alterados.
-   O volume que contém o arquivo de origem do link é movido para outro computador dentro do mesmo domínio.

O serviço de controle de link distribuído também tenta manter links nas situações anteriores, mesmo quando eles não ocorrem dentro de um domínio, ou seja, eles são entre domínios ou dentro de um grupo de trabalho. Os links sempre podem ser mantidos nessas situações quando o compartilhamento de rede no computador de origem do link é alterado. Eles também podem ser mantidos quando uma fonte de link é movida dentro de um computador. Geralmente, os links podem ser mantidos quando a origem do link é movida para outro computador, mas essa forma de controle é menos confiável ao longo do tempo.

## <a name="link-tracking-functionality"></a>Funcionalidade de rastreamento de link

A funcionalidade de rastreamento de link é implementada principalmente na forma dos dois serviços do sistema a seguir:

-   Cliente de Rastreamento de Link Distribuído
-   Servidor de rastreamento de link distribuído

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Cliente de rastreamento de link distribuído
</dt> <dd>

O cliente de rastreamento de link distribuído é executado em todos os computadores e gerencia as atividades de rastreamento de link para esse computador. Essas atividades incluem a pesquisa de fontes de link e o processamento de movimentações de fonte de link. Quando uma fonte de link é movida, o serviço passa informações para o servidor de rastreamento de link distribuído que é executado em controladores de domínio.

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Servidor de rastreamento de link distribuído
</dt> <dd>

O servidor de rastreamento de link distribuído é executado em cada controlador de domínio em um domínio. O serviço aceita notificações de alterações de arquivo e volume do serviço de controle em um computador e permite que o cliente de rastreamento de link distribuído consulte o local atual de uma fonte de link.

Esse serviço de servidor mantém informações nos controladores de domínio sobre volumes e arquivos que foram movidos. As informações sobre as movimentações não podem aumentar além de um tamanho específico e são removidas automaticamente se se tornarem desnecessárias.

</dd> </dl>

Os serviços de rastreamento de link são expostos pelas interfaces [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) e [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) . Portanto, eles são usados por atalhos do Shell. Quando o método [**IShellLink:: resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) é chamado e o arquivo Referent não pode ser encontrado, por exemplo, quando o usuário ativa um atalho do Shell, o serviço de controle é chamado automaticamente para localizar o arquivo. Da mesma forma, quando a implementação de [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) não pode localizar um arquivo, por exemplo, em seu método [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) , ele chama automaticamente o serviço de rastreamento.

## <a name="link-tracking-limitations"></a>Limitações de rastreamento de link

Os serviços de rastreamento de link distribuído estão disponíveis apenas no sistema de arquivos NTFS e só estão disponíveis para fontes de link no NTFS 3,0 ou posterior. Portanto, se uma fonte de link for movida para um volume do sistema de arquivos FAT, as informações de rastreamento serão perdidas. Além disso, se uma fonte de link for movida entre o NTFS 3,0 ou posterior, mas o computador que está executando a movimentação estiver executando uma versão anterior do Windows, as informações de rastreamento de link serão perdidas. Quando as informações de rastreamento de link são perdidas, nenhum dano é feito para o próprio arquivo de origem do link, ele simplesmente não é rastreável pelos serviços de controle de link distribuído.

Para obter a versão NTFS de um volume, abra um prompt de comando com direitos de acesso de administrador e execute o seguinte comando:

**fsutil fsinfo ntfsinfo** *X ** * *:*

em que *X* é a letra da unidade do volume.

Os links para arquivos em mídia removível não são mantidos. Além disso, o serviço de controle não reconhece um novo volume do sistema de arquivos NTFS até que o sistema seja reinicializado. Um novo volume pode ser disponibilizado por causa de reparticionamento, reformatação de um volume do sistema de arquivos FAT para o sistema de arquivos NTFS ou conexão de uma nova unidade externa.

 

 
