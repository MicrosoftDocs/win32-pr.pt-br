---
description: Os serviços de transliteração ELS mapeiam o texto UTF-16 de um sistema de escrita para outro sistema de escrita.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Serviços de transliteração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d442ed0a9c45d5fb40ffa3f84438f6b2a46ad0a5a6587e3a9fd16dd2f2fd9cff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788266"
---
# <a name="transliteration-services"></a>Serviços de transliteração

Os serviços de transliteração ELS mapeiam o texto UTF-16 de um sistema de escrita para outro sistema de escrita. Cada serviço é realmente uma aplicação de dados a um conjunto específico de scripts Unicode de entrada e saída, e a transliteração real é interna à plataforma ELS. O aplicativo pode, opcionalmente, enumerar os serviços disponíveis para scripts de entrada e saída específicos e selecionar o serviço que ele requer.

A plataforma mantém metadados para os serviços de transliteração de ELS. Os metadados de cada serviço fornecem uma descrição do serviço e lista os scripts de entrada e saída aos quais o serviço dá suporte. Os metadados são representados por uma estrutura de [**\_ \_ informações de serviço de mapeamento**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) recuperada pela função [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .

## <a name="input-to-a-transliteration-service"></a>Entrada para um serviço de transliteração

A entrada para um serviço de transliteração é o texto UTF-16 em um sistema de escrita.

## <a name="output-of-a-transliteration-service"></a>Saída de um serviço de transliteração

A saída de um serviço de transliteração é o texto UTF-16 mapeado para um segundo sistema de escrita. Se nenhum mapeamento de transliteração apropriado estiver disponível para qualquer parte determinada do texto de entrada, a parte permanecerá inalterada.

## <a name="transliteration-service-operation"></a>Operação do serviço de transliteração

Um serviço de transliteração mapeia o texto Unicode de um script de entrada para um script de saída, caractere por caractere ou termo por termo, conforme apropriado. O aplicativo pode optar por obter o serviço de transliteração específico de interesse especificando scripts de entrada e saída ao chamar [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)ou fornecendo o GUID do serviço. Outra opção para o aplicativo é enumerar todos os serviços de transliteração disponíveis especificando a categoria de serviço "transliteração" ao chamar **MappingGetServices**. Nesse caso, o aplicativo chama cada serviço e compara os resultados com o texto original para ver se os resultados foram alterados pela operação de um serviço específico.

O aplicativo pode solicitar reconhecimento de texto para um serviço de transliteração de ELS com uma chamada para [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext). Quando ele recebe a solicitação, o serviço de transliteração aloca um buffer para conter os dados transliterados e, em seguida, executa o reconhecimento de texto para cada ponto de código na cadeia de caracteres de entrada fornecida pelo aplicativo.

> [!Note]  
> O texto original e o texto transliterado podem ter comprimentos diferentes.

 

## <a name="transliteration-service-guids"></a>GUIDs do serviço de transliteração

Os GUIDs dos serviços de transliteração são declarados em Elssrvc. h, conforme mostrado no código a seguir.


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os serviços lingüísticos estendidos](about-extended-linguistic-services.md)
</dt> </dl>

 

 



