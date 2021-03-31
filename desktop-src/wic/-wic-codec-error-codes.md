---
description: Este documento contém uma lista dos códigos de erro definidos pelo Windows Imaging Component (WIC).
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: Códigos de erro de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd502ca1866114e2b471059bc9d9af1b0f96309f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920876"
---
# <a name="codec-error-codes"></a>Códigos de erro de codec

Este documento contém uma lista dos códigos de erro definidos pelo Windows Imaging Component (WIC).

-   [Erros de WIC por código](#wic-errors-by-code)
-   [Erros de WIC por valor](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>Erros de WIC por código

A tabela a seguir é uma lista dos códigos de erro usados pelo WICAPIs classificados em ordem alfabética. 

| Código de erro                                      | Valor do erro                      |
|-------------------------------------------------|----------------------------------|
| WINCODEC de \_ erro \_ anulado                          | 0x80004004 (E \_ abortar)            |
| WINCODEC \_ Err \_ ACCESSDENIED                     | 0x80070005 (E \_ ACCESSDENIED)     |
| WINCODEC \_ Err \_ ALREADYLOCKED                    | 0x88982f0D                       |
| WINCODEC \_ Err \_ BADHEADER                        | 0x88982f61                       |
| WINCODEC \_ Err \_ BADIMAGE                         | 0x88982f60                       |
| WINCODEC \_ Err \_ BADMETADATAHEADER                | 0x88982f63                       |
| WINCODEC \_ Err \_ BADSTREAMDATA                    | 0x88982f70                       |
| WINCODEC \_ Err \_ CODECNOTHUMBNAIL                 | 0x88982f44                       |
| WINCODEC \_ Err \_ CODECPRESENT                     | 0x88982f43                       |
| WINCODEC \_ Err \_ CODECTOOMANYSCANLINES            | 0x88982f46                       |
| WINCODEC \_ Err \_ COMPONENTINITIALIZEFAILURE       | 0x88982f8B                       |
| WINCODEC \_ Err \_ COMPONENTNOTFOUND                | 0x88982f50                       |
| WINCODEC \_ Err \_ DUPLICATEMETADATAPRESENT         | 0x88982f8D                       |
| WINCODEC \_ Err \_ FRAMEMISSING                     | 0x88982f62                       |
| \_ \_ erro genérico de erro WINCODEC \_                   | 0x80004005 (E \_ falha)             |
| WINCODEC \_ Err \_ IMAGESIZEOUTOFRANGE              | 0x88982f51                       |
| WINCODEC \_ Err \_ INSUFFICIENTBUFFER               | 0x88982f8C                       |
| WINCODEC \_ Err \_ INTERNALERROR                    | 0x88982f48                       |
| WINCODEC \_ Err \_ INVALIDPARAMETER                 | 0x80070057 (E \_ INVALIDARG)       |
| WINCODEC \_ Err \_ INVALIDQUERYCHARACTER            | 0x88982f93                       |
| WINCODEC \_ Err \_ INVALIDQUERYREQUEST              | 0x88982f90                       |
| WINCODEC \_ Err \_ INVALIDREGISTRATION              | 0x88982f8A                       |
| WINCODEC \_ Err não \_ implementado                   | 0x80004001 (E \_ NOTIMPL)          |
| WINCODEC \_ Err não \_ inicializado                   | 0x88982f0C                       |
| OUTOFMEMORY WINCODEC de \_ erro \_                      | 0x8007000E (E \_ OUTOFMEMORY)      |
| WINCODEC \_ Err \_ PALETTEUNAVAILABLE               | 0x88982f45                       |
| WINCODEC \_ Err \_ PROPERTYNOTFOUND                 | 0x88982f40                       |
| WINCODEC \_ Err \_ PROPERTYNOTSUPPORTED             | 0x88982f41                       |
| WINCODEC \_ Err \_ PROPERTYSIZE                     | 0x88982f42                       |
| WINCODEC \_ Err \_ PROPERTYUNEXPECTEDTYPE           | 0x88982f8E                       |
| WINCODEC \_ Err \_ REQUESTONLYVALIDATMETADATAROOT   | 0x88982f92                       |
| WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS | 0x88982f49                       |
| WINCODEC \_ Err \_                      | 0x88982f71                       |
| WINCODEC \_ Err \_ STREAMREAD                       | 0x88982f72                       |
| WINCODEC \_ Err \_ STREAMNOTAVAILABLE               | 0x88982f73                       |
| WINCODEC \_ Err \_ TOOMUCHMETADATA                  | 0x88982f52                       |
| WINCODEC \_ Err \_ UNKNOWNIMAGEFORMAT               | 0x88982f07                       |
| WINCODEC \_ Err \_ UNEXPECTEDMETADATATYPE           | 0x88982f91                       |
| WINCODEC \_ Err \_ UNEXPECTEDSIZE                   | 0x88982f8F                       |
| WINCODEC \_ Err \_ UNSUPPORTEDOPERATION             | 0x88982f81                       |
| WINCODEC \_ Err \_ UNSUPPORTEDPIXELFORMAT           | 0x88982f80                       |
| WINCODEC \_ Err \_ UNSUPPORTEDVERSION               | 0x88982f0B                       |
| WINCODEC \_ Err \_ VALUEOUTOFRANGE                  | 0x88982f05                       |
| WINCODEC \_ Err \_ VALUEOVERFLOW                    | \_ \_ estouro ARITMÉTICO de INTSAFE E \_ |
| WINCODEC \_ errstate \_                       | 0x88982f04                       |



 

## <a name="wic-errors-by-value"></a>Erros de WIC por valor

A tabela a seguir é uma lista dos códigos de erro usados pelo WICAPIs classificados em ordem numérica. 

| Código de erro                       | Valor do erro                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_ falha)             | \_ \_ erro genérico de erro WINCODEC \_                   |
| 0x80070057 (E \_ INVALIDARG)       | WINCODEC \_ Err \_ INVALIDPARAMETER                 |
| 0x8007000E (E \_ OUTOFMEMORY)      | OUTOFMEMORY WINCODEC de \_ erro \_                      |
| 0x80004001 (E \_ NOTIMPL)          | WINCODEC \_ Err não \_ implementado                   |
| 0x80004004 (E \_ abortar)            | WINCODEC de \_ erro \_ anulado                          |
| 0x80070005 (E \_ ACCESSDENIED)     | WINCODEC \_ Err \_ ACCESSDENIED                     |
| \_ \_ estouro ARITMÉTICO de INTSAFE E \_ | WINCODEC \_ Err \_ VALUEOVERFLOW                    |
| 0x88982f04                       | WINCODEC \_ errstate \_                       |
| 0x88982f05                       | WINCODEC \_ Err \_ VALUEOUTOFRANGE                  |
| 0x88982f07                       | WINCODEC \_ Err \_ UNKNOWNIMAGEFORMAT               |
| 0x88982f0B                       | WINCODEC \_ Err \_ UNSUPPORTEDVERSION               |
| 0x88982f0C                       | WINCODEC \_ Err não \_ inicializado                   |
| 0x88982f0D                       | WINCODEC \_ Err \_ ALREADYLOCKED                    |
| 0x88982f40                       | WINCODEC \_ Err \_ PROPERTYNOTFOUND                 |
| 0x88982f41                       | WINCODEC \_ Err \_ PROPERTYNOTSUPPORTED             |
| 0x88982f42                       | WINCODEC \_ Err \_ PROPERTYSIZE                     |
| 0x88982f43                       | WINCODEC \_ Err \_ CODECPRESENT                     |
| 0x88982f44                       | WINCODEC \_ Err \_ CODECNOTHUMBNAIL                 |
| 0x88982f45                       | WINCODEC \_ Err \_ PALETTEUNAVAILABLE               |
| 0x88982f46                       | WINCODEC \_ Err \_ CODECTOOMANYSCANLINES            |
| 0x88982f48                       | WINCODEC \_ Err \_ INTERNALERROR                    |
| 0x88982f49                       | WINCODEC \_ Err \_ SOURCERECTDOESNOTMATCHDIMENSIONS |
| 0x88982f50                       | WINCODEC \_ Err \_ COMPONENTNOTFOUND                |
| 0x88982f51                       | WINCODEC \_ Err \_ IMAGESIZEOUTOFRANGE              |
| 0x88982f52                       | WINCODEC \_ Err \_ TOOMUCHMETADATA                  |
| 0x88982f60                       | WINCODEC \_ Err \_ BADIMAGE                         |
| 0x88982f61                       | WINCODEC \_ Err \_ BADHEADER                        |
| 0x88982f62                       | WINCODEC \_ Err \_ FRAMEMISSING                     |
| 0x88982f63                       | WINCODEC \_ Err \_ BADMETADATAHEADER                |
| 0x88982f70                       | WINCODEC \_ Err \_ BADSTREAMDATA                    |
| 0x88982f71                       | WINCODEC \_ Err \_                      |
| 0x88982f72                       | WINCODEC \_ Err \_ STREAMREAD                       |
| 0x88982f73                       | WINCODEC \_ Err \_ STREAMNOTAVAILABLE               |
| 0x88982f80                       | WINCODEC \_ Err \_ UNSUPPORTEDPIXELFORMAT           |
| 0x88982f81                       | WINCODEC \_ Err \_ UNSUPPORTEDOPERATION             |
| 0x88982f8A                       | WINCODEC \_ Err \_ INVALIDREGISTRATION              |
| 0x88982f8B                       | WINCODEC \_ Err \_ COMPONENTINITIALIZEFAILURE       |
| 0x88982f8C                       | WINCODEC \_ Err \_ INSUFFICIENTBUFFER               |
| 0x88982f8D                       | WINCODEC \_ Err \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f8E                       | WINCODEC \_ Err \_ PROPERTYUNEXPECTEDTYPE           |
| 0x88982f8F                       | WINCODEC \_ Err \_ UNEXPECTEDSIZE                   |
| 0x88982f90                       | WINCODEC \_ Err \_ INVALIDQUERYREQUEST              |
| 0x88982f91                       | WINCODEC \_ Err \_ UNEXPECTEDMETADATATYPE           |
| 0x88982f92                       | WINCODEC \_ Err \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982f93                       | WINCODEC \_ Err \_ INVALIDQUERYCHARACTER            |



 

 

 



