---
title: Funções ADSI
description: Active Directory interfaces de serviço expõem as seguintes funções auxiliares para clientes que não usam automação.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI, referência, ADSI, funções
- função ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291800"
---
# <a name="adsi-functions"></a>Funções ADSI

Active Directory interfaces de serviço expõem as seguintes funções auxiliares para clientes que não usam automação.



| Função                                           | Descrição                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | Cria um objeto enumerador para o objeto de contêiner ADSI especificado.                              |
| [**ADsBuildVarArrayInt**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | Cria uma matriz variante de uma matriz de **DWORD** s.                                                |
| [**ADsBuildVarArrayStr**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | Cria uma matriz variante de uma matriz de cadeias de caracteres Unicode.                                           |
| [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | Converte um blob de dados binários para o formato adequado para um filtro de pesquisa.                         |
| [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | Popula uma matriz Variant com elementos recuperados do objeto enumerador especificado.            |
| [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | Libera um objeto enumerador criado anteriormente pelo [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator). |
| [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | Recupera o último valor de código de erro do thread de chamada.                                         |
| [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | Associa a um objeto ADSI usando as credenciais atuais.                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | Associa a um objeto ADSI usando as credenciais especificadas                                                |
| [**ADsSetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | Define o valor do código de erro do thread de chamada.                                                   |
| [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | Aloca um bloco de memória.                                                                       |
| [**AllocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | Aloca memória para uma determinada cadeia de caracteres.                                                               |
| [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | Libera a memória alocada por [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).                                  |
| [**FreeADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | Libera a memória alocada para a cadeia de caracteres fornecida.                                                   |
| [**ReallocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | Atribui o conteúdo de memória existente a um local de memória criado recentemente.                            |
| [**ReallocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | Substitui uma cadeia de caracteres existente por uma nova.                                                        |



 

As seguintes funções ADSI são obsoletas.



| Função                                                  | Descrição |
|-----------------------------------------------------------|-------------|
| [**AdsFreeAllErrorRecords**](obsolete-adsi-functions.md) | Obsoleto.   |
| [**AdsDecodeBinaryData**](obsolete-adsi-functions.md)    | Obsoleto.   |
| [**PropVariantToAdsType**](obsolete-adsi-functions.md)   | Obsoleto.   |
| [**AdsTypeToPropVariant**](obsolete-adsi-functions.md)   | Obsoleto.   |
| [**AdsFreeAdsValues**](obsolete-adsi-functions.md)       | Obsoleto.   |
| [**InitAdsMem**](obsolete-adsi-functions.md)             | Obsoleto.   |
| [**AssertAdsmemLeaks**](obsolete-adsi-functions.md)      | Obsoleto.   |
| [**DumpMemorytracker**](obsolete-adsi-functions.md)      | Obsoleto.   |



 

 

 




