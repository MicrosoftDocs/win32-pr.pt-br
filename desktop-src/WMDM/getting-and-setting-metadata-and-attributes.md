---
title: Obtendo e configurando metadados e atributos
description: Obtendo e configurando metadados e atributos
ms.assetid: 83534998-4e7d-49b6-a160-ef9a0ddea5db
keywords:
- Windows Gerenciador de Dispositivos de mídia, atributos
- Gerenciador de Dispositivos, atributos
- aplicativos de área de trabalho, atributos
- provedores de serviços, atributos
- Guia de programação, atributos
- Atributos
- Windows Gerenciador de Dispositivos de mídia, metadados
- Gerenciador de Dispositivos, metadados
- aplicativos de área de trabalho, metadados
- provedores de serviços, metadados
- Guia de programação, metadados
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d92c8311c3fff3c4785116604e53652c4f07b6b63b3a2c4389cc3dd4b6a5f35a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957556"
---
# <a name="getting-and-setting-metadata-and-attributes"></a>Obtendo e configurando metadados e atributos

Um aplicativo pode obter dois tipos de informações sobre um armazenamento ou dispositivo: atributos e metadados. Atributos são valores Boolianos mais simples que geralmente descrevem informações do sistema de arquivos, como se um armazenamento tem objetos filho, se ele pode ser renomeado, lido ou excluído, e assim por diante. Os atributos são recuperados como valores de sinalizadores chamando [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) ou [**IWMDMStorage2:: GetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2). Os atributos são definidos chamando [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata).

Um aplicativo também pode solicitar dados mais complexos (numéricos, cadeias de caracteres ou outros tipos de dados) como *metadados*. Os valores de metadados são identificados por nomes de cadeia de caracteres exclusivos. Windows Gerenciador de Dispositivos de mídia define uma lista de constantes de cadeia de caracteres que podem ser usadas para solicitar valores; esses valores definidos são listados em [constantes de metadados](metadata-constants.md). Um provedor de serviços pode definir suas próprias constantes, mas um aplicativo de chamada deve estar ciente dessas definições para solicitar ou definir esses valores de metadados personalizados. O aplicativo solicita metadados chamando [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) ou [**IWMDMStorage4:: GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata).

Um aspecto importante de obter e definir metadados e atributos é entender de onde vêm os valores recuperados. O provedor de serviços ou o dispositivo pode obter esses valores de vários locais diferentes, incluindo o seguinte:

-   No cabeçalho do arquivo. Por exemplo, em um arquivo ASF, a taxa de bits é armazenada no cabeçalho do arquivo.
-   De valores definidos explicitamente pelo aplicativo ao chamar um método. Esses valores podem ser salvos em um repositório de metadados externo no provedor de serviços ou no dispositivo. Esse armazenamento pode ou não persistir quando o dispositivo se desconectar ou desligar. Por exemplo, a contagem de execuções e as classificações de estrelas do usuário normalmente são armazenadas em repositórios externos no computador ou dispositivo.
-   Examinando as informações fornecidas pelo sistema de arquivos. Por exemplo, se um arquivo é somente leitura ou se uma pasta tem filhos.
-   Abrindo e analisando os dados do arquivo.

É importante perceber que uma propriedade pode ser armazenada em mais de um local (dentro do cabeçalho do arquivo e também em um repositório local) e que pode ou não ser editável. Por exemplo, alterar uma descrição de arquivo pode ou não ser persistente; Se o provedor de serviços armazenar a descrição localmente, ele não será mantido no dispositivo. Da mesma forma, se a descrição do arquivo for extraída do cabeçalho do arquivo, a modificação será persistente somente se o provedor ou o dispositivo de serviço abrir e modificar os dados do cabeçalho. A maioria dos aplicativos faz uma melhor tentativa alterando os valores desejados, mas não depende de nenhuma propriedade ser alterada de forma persistente.

Mais informações sobre como obter e definir valores são fornecidas nas seções apropriadas para desenvolvedores de aplicativos e desenvolvedores de provedores de serviços mais adiante na documentação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tarefas comuns a aplicativos e provedores de serviços**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




