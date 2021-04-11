---
description: Modelo de objeto VDS
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: Modelo de objeto VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104172390"
---
# <a name="vds-object-model"></a>Modelo de objeto VDS

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O VDS fornece acesso indireto a dispositivos de armazenamento baseados em host, como discos e dispositivos de CD-ROM, e a matrizes de disco que são gerenciadas por controladores RAID de hardware. Enquanto algumas entidades de armazenamento modelam dispositivos físicos, outros modelam construções virtuais: volumes, partições e assim por diante. Os objetos descritos neste tópico representam as entidades físicas e virtuais do VDS.

Os aplicativos chamam os métodos que são expostos por esses objetos e o VDS chama o provedor apropriado para executar as operações de armazenamento solicitadas. Um aplicativo nunca chama um programa de provedor diretamente.

### <a name="classification-of-objects"></a>Classificação de objetos

Como mostra a ilustração a seguir, os programas de provedor de software implementam objetos que modelam entidades baseadas em host; programas de provedor de hardware implementam objetos que modelam dispositivos RAID de hardware internos e externos; os objetos comuns restantes são independentes do provedor ou são implementados pelo VDS. Um eixo, que não é um objeto VDS, é um termo para mídia de armazenamento genérico que compreende as extensões de disco ou unidade.

![Diagrama que mostra uma classificação de objetos, definidos como ' objetos comuns ', ' objetos de provedor de software ' e ' objetos de provedor de hardware '.](images/vdsobjectmodel.png)

Para saber mais sobre o comportamento de cada objeto, selecione um dos seguintes tópicos:

-   Carregador de serviço e objetos de serviço, consulte [Startup and Service Objects](startup-and-service-objects.md).
-   Enumeração e objetos assíncronos, consulte [objetos auxiliares](helper-objects.md).
-   Objeto do provedor, consulte [objeto do provedor](provider-object.md).
-   Objetos de pacote, disco, volume e volume Plex, consulte [objetos de provedor de software](software-provider-objects.md).
-   Objetos de subsistema, controlador, unidade, LUN e LUN Plex, consulte [objetos de provedor de hardware](hardware-provider-objects.md).

### <a name="object-creation"></a>Criação de objetos

As operações de configuração e consulta associadas à criação de objetos podem levar um tempo considerável para serem concluídas; dessa forma, o VDS invoca todos os métodos de forma assíncrona. O provedor de descoberta retorna todos os eventos de conclusão, erro ou alteração de estado. Os provedores de software também registram em log todos os erros e alterações de estado significativas.

### <a name="object-deletion"></a>Exclusão de objeto

Vários métodos VDS excluem ou transformam objetos VDS. Um chamador pode manter uma referência, por meio de um ponteiro de interface, para um objeto excluído depois que o método retorna. Quando o chamador libera a interface, o VDS exclui o objeto.

Com relação à exclusão de objetos, os chamadores devem evitar invocar qualquer coisa, exceto o método [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nessas interfaces. O provedor deve ser robusto o suficiente para lidar com chamadores errônea; se um chamador invocar um método em um objeto excluído, o provedor deverá retornar **o \_ objeto VDS E \_ \_ excluído**.

### <a name="service-initialization"></a>Inicialização do serviço

O VDS fornece um identificador de classe (CLSID) para o carregador de serviço e os objetos de serviço, mas apenas o CLSID do carregador de serviço é público. A inicialização do serviço ocorre quando os provedores, um aplicativo de chamada e o serviço executam as seguintes tarefas:

-   Cada novo provedor invoca o método [**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) durante a instalação para se registrar no VDS. A chamada cria uma chave do registro no hive do sistema, identificada pelo GUID do objeto do provedor. Contido nessa chave está o CLSID do objeto do provedor, o nome, a versão e o GUID da versão do provedor.
    > [!Note]  
    > Os GUIDs de objeto do provedor são persistentes; os GUIDs de objeto de software e hardware não são.

     

-   Um aplicativo chama a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , passando o CLSID do carregador de serviço como um argumento. Com um ponteiro para o objeto do carregador de serviço, o aplicativo pode iniciar o VDS local ou remotamente passando o nome do computador desejado como um parâmetro para o método [**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) .
-   Quando o aplicativo inicial é anexado ao serviço, o VDS primeiro chama [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em cada CLSID encontrado na chave do registro e, em seguida, chama o método [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) em cada provedor para inicializar os programas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o VDS](about-vds.md)
</dt> <dt>

[**IVdsAdmin:: RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**IVdsServiceLoader:: loadservice**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
