---
description: Os ELS (serviços lingüísticos estendidos) são implementados como uma DLL (biblioteca de vínculo dinâmico) que fornece uma variedade de funcionalidades lingüísticas de suporte para o texto especificado pelo aplicativo.
ms.assetid: 23d4e42a-a5bb-467c-a8b9-6a57ae39daa0
title: Sobre os serviços lingüísticos estendidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6594fcfe67954a56cb09e239221b2b529d4d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759396"
---
# <a name="about-extended-linguistic-services"></a>Sobre os serviços lingüísticos estendidos

Os ELS (serviços lingüísticos estendidos) são implementados como uma DLL (biblioteca de vínculo dinâmico) que fornece uma variedade de funcionalidades lingüísticas de suporte para o texto especificado pelo aplicativo. A tecnologia inclui a plataforma ELS e os plug-ins para vários tipos de serviço linguísticos predefinidos acessíveis para o aplicativo por meio da plataforma.

> [!Note]  
> O módulo ELS é instalado automaticamente com o Windows 7 e posterior.

 

## <a name="els-platform"></a>Plataforma ELS

A plataforma ELS é a interface entre seu aplicativo e os serviços do ELS. Ele fornece uma maneira simples de implementar vários tipos de funcionalidades linguísticas por meio da mesma API, que permite que o aplicativo acesse e use serviços específicos. Para obter mais informações sobre a API, consulte [referência de serviços linguísticas estendidos.](extended-linguistic-services-reference.md)

> [!Note]  
> Quando o aplicativo chama qualquer uma das funções da API ELS, a plataforma aloca memória e recursos conforme necessário para comunicação com os serviços. O aplicativo é responsável por chamar a plataforma novamente para liberar esses recursos.

 

A plataforma é executada dentro do espaço de memória virtual do aplicativo e toda a memória alocada faz parte desse espaço. Portanto, seu aplicativo só precisa vincular à DLL do componente ELS (Elscore.dll) vinculando-se a Elscore. lib ou carregando dinamicamente Elscore.dll.

## <a name="els-services"></a>Serviços ELSs

Para o Windows 7 e posterior, a plataforma ELS dá suporte apenas aos seguintes serviços predefinidos.

-   [Detecção de Idioma da Microsoft](microsoft-language-detection.md)
-   [Detecção de script da Microsoft](microsoft-script-detection.md)
-   [Serviços de transliteração](transliteration-services.md)

> [!Note]  
> As versões futuras do ELS terão suporte para serviços adicionais fornecidos pela Microsoft ou pelos provedores de serviços.

 

Cada serviço é associado a uma categoria de serviço que descreve o que o serviço faz. A categoria é representada por uma cadeia de caracteres não localizável. Ele é usado por aplicativos para enumerar os serviços disponíveis. As categorias de serviço atuais são:

-   "Detecção de Idioma"
-   "Detecção de script"
-   Transliteração

A plataforma usa metadados de serviço para enumerar os serviços solicitados pelo aplicativo. Propriedades como o GUID (identificador global exclusivo) de serviço, os scripts e os idiomas de entrada e saída com suporte e a categoria de serviço podem ser usados pelo aplicativo para enumerar os serviços ELS desejados.

Cada serviço ELS é implementado como um plug-in com suporte de uma DLL que pode ser instalada no sistema operacional para que a plataforma ELS possa detectá-la e usá-la. Os serviços podem expor seus próprios subserviços, se necessário.

## <a name="main-els-operations"></a>Principais operações de ELS

Esta seção descreve as principais operações com suporte pela plataforma ELS. A plataforma dá suporte aos modos de chamada síncrono e assíncrono. O modo de chamada assíncrona usa um pool de threads de aplicativo para agendar threads para processamento de solicitações.

> [!Note]  
> Como a plataforma dá suporte a um modo assíncrono, os serviços ELSs não precisam implementar esse tipo de funcionalidade por conta própria.

 

### <a name="service-enumeration"></a>Enumeração de serviço

A plataforma ELS carrega e gerencia todos os serviços do ELS, tornando a operação transparente para o aplicativo. O aplicativo enumera os serviços disponíveis chamando [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices). Para obter instruções de programação, consulte [enumerando e liberando serviços](enumerating-and-freeing-services.md).

> [!Note]  
> É aconselhável por motivos de desempenho para que seu aplicativo enumere os serviços disponíveis apenas uma vez. A plataforma ELS verifica os serviços novamente na próxima enumeração para garantir que seus resultados de enumeração sejam sempre atuais.

 

### <a name="text-recognition"></a>Reconhecimento de texto

Após a enumeração de serviço, o aplicativo chama a função [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) para usar um serviço ELS específico para mapear qualquer intervalo de texto de texto de entrada para o texto de saída. Um exemplo de reconhecimento de texto é o uso de um serviço de detecção de idioma que recebe um segmento de texto e detecta sua linguagem mais provável.

Depois que o serviço reconheceu o texto, [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retorna com uma estrutura de [**recipiente de \_ Propriedades \_ de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_property_bag) preenchida com os dados de saída e as propriedades produzidas pelo serviço. Para evitar vazamentos de memória, o aplicativo deve liberar o recipiente de propriedades chamando [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) para cada vez que o [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext) retornar S \_ OK. Normalmente, o aplicativo faz isso quando termina de usar os dados de saída ou quando os dados de saída não são mais relevantes porque a região de entrada do texto foi modificada, por exemplo, editada ou excluída. Quando o recipiente de propriedades é liberado, **MappingFreePropertyBag** retorna.

Instruções de programação para reconhecimento de texto são fornecidas na [solicitação de reconhecimento de texto](requesting-text-recognition.md).

### <a name="service-termination"></a>Término do serviço

Quando o aplicativo não exigir mais serviços ELS, ele chamará [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices) antes de ser encerrado. Para obter mais informações, consulte [enumerando e liberando serviços](enumerating-and-freeing-services.md).

### <a name="versioning"></a>Controle de versão

As versões futuras do ELS permitirão que os serviços do ELS sejam atualizados. O aplicativo poderá verificar os números de versão da estrutura de [**informações do \_ serviço \_ de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) para detectar quaisquer alterações nos serviços.

> [!Note]  
> Seu aplicativo ELS não deve fazer a suposição de que diferentes versões do mesmo serviço possam recuperar exatamente os mesmos resultados.

 

 

 



