---
description: este documento contém uma lista de códigos de erro definidos por WIC (Windows Imaging Component).
ms.assetid: 1ded909c-311b-49e3-ba23-b22cd7a77bc6
title: Códigos de erro de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb8f3911516f11c4a0614461786d6f94eaf00e038e53babb47d4df595797bdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207255"
---
# <a name="codec-error-codes"></a>Códigos de erro de codec

este documento contém uma lista de códigos de erro definidos por WIC (Windows Imaging Component).

-   [Erros de WIC por código](#wic-errors-by-code)
-   [Erros de WIC por valor](#wic-errors-by-value)

## <a name="wic-errors-by-code"></a>Erros de WIC por código

A tabela a seguir é uma lista dos códigos de erro usados pelo WICAPIs classificados em ordem alfabética. 

| Código do Erro                                      | Valor do erro                      |
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



 

## <a name="wic-errors-by-value"></a>Erros do WIC por valor

A tabela a seguir é uma lista dos códigos de erro usados pelos WICAPIs classificação em ordem numérica. 

| Código do Erro                       | Valor do erro                                     |
|----------------------------------|-------------------------------------------------|
| 0x80004005 (E \_ FAIL)             | ERRO GENÉRICO DE ERRO DO WINCODEC \_ \_ \_                   |
| 0x80070057 (E \_ INVALIDARG)       | WINCODEC \_ ERR \_ INVALIDPARAMETER                 |
| 0x8007000E (E \_ OUTOFMEMORY)      | WINCODEC \_ ERR \_ OUTOFMEMORY                      |
| 0x80004001 (E \_ NOTIMPL)          | WINCODEC \_ ERR \_ NOTIMPLEMENTED                   |
| 0x80004004 (E \_ ABORT)            | WINCODEC \_ ERR \_ ABORTED                          |
| 0x80070005 (E \_ ACCESSDENIED)     | WINCODEC \_ ERR \_ ACCESSDENIED                     |
| ESTOURO \_ ARITMÉTICO INTSAFE E \_ \_ | WINCODEC \_ ERR \_ VALUEOVERFLOW                    |
| 0x88982f04                       | WINCODEC \_ ERR \_ WRONGSTATE                       |
| 0x88982f05                       | WINCODEC \_ ERR \_ VALUEOUTOFRANGE                  |
| 0x88982f07                       | WINCODEC \_ ERR \_ UNKNOWNIMAGEFORMAT               |
| 0x88982f0B                       | WINCODEC \_ ERR \_ UNSUPPORTEDVERSION               |
| 0x88982f0C                       | WINCODEC \_ ERR \_ NOTINITIALIZED                   |
| 0x88982f0D                       | WINCODEC \_ ERR \_ ALREADYLOCKED                    |
| 0x88982f40                       | WINCODEC \_ ERR \_ PROPERTYNOTFOUND                 |
| 0x88982f41                       | WINCODEC \_ ERR \_ PROPERTYNOTSUPPORTED             |
| 0x88982f42                       | WINCODEC \_ ERR \_ PROPERTYSIZE                     |
| 0x88982f43                       | WINCODEC \_ ERR \_ CODECPRESENT                     |
| 0x88982f44                       | CÓDIGO DE \_ ERRO DO WINCODECNOTHUMBNAIL \_                 |
| 0x88982f45                       | WINCODEC \_ ERR \_ PALETTEUNAVAILABLE               |
| 0x88982f46                       | WINCODEC \_ ERR \_ CODECTOOMANYSCANLINES            |
| 0x88982f48                       | WINCODEC \_ ERR \_ INTERNALERROR                    |
| 0x88982f49                       | WINCODEC \_ ERR \_ SOURCERECTDOESNOTMATCHDIMENSIONS |
| 0x88982f50                       | WINCODEC \_ ERR \_ COMPONENTNOTFOUND                |
| 0x88982f51                       | WINCODEC \_ ERR \_ IMAGESIZEOUTOFRANGE              |
| 0x88982f52                       | WINCODEC \_ ERR \_ TOOMUCHMETADATA                  |
| 0x88982f60                       | WINCODEC \_ ERR \_ BADIMAGE                         |
| 0x88982f61                       | WINCODEC \_ ERR \_ BADHEADER                        |
| 0x88982f62                       | WINCODEC \_ ERR \_ FRAMEMISSING                     |
| 0x88982f63                       | WINCODEC \_ ERR \_ BADMETADATAHEADER                |
| 0x88982f70                       | WINCODEC \_ ERR \_ BADSTREAMDATA                    |
| 0x88982f71                       | WINCODEC \_ ERR \_ STREAMWRITE                      |
| 0x88982f72                       | WINCODEC \_ ERR \_ STREAMREAD                       |
| 0x88982f73                       | WINCODEC \_ ERR \_ STREAMNOTAVAILABLE               |
| 0x88982f80                       | WINCODEC \_ ERR \_ UNSUPPORTEDPIXELFORMAT           |
| 0x88982f81                       | WINCODEC \_ ERR \_ UNSUPPORTEDOPERATION             |
| 0x88982f8A                       | WINCODEC \_ ERR \_ INVALIDREGISTRATION              |
| 0x88982f8B                       | WINCODEC \_ ERR \_ COMPONENTINITIALIZEFAILURE       |
| 0x88982f8C                       | WINCODEC \_ ERR \_ INSUFFICIENTBUFFER               |
| 0x88982f8D                       | WINCODEC \_ ERR \_ DUPLICATEMETADATAPRESENT         |
| 0x88982f8E                       | WINCODEC \_ ERR \_ PROPERTYUNEXPECTEDTYPE           |
| 0x88982f8F                       | WINCODEC \_ ERR \_ UNEXPECTEDSIZE                   |
| 0x88982f90                       | WINCODEC \_ ERR \_ INVALIDQUERYREQUEST              |
| 0x88982f91                       | WINCODEC \_ ERR \_ UNEXPECTEDMETADATATYPE           |
| 0x88982f92                       | WINCODEC \_ ERR \_ REQUESTONLYVALIDATMETADATAROOT   |
| 0x88982f93                       | WINCODEC \_ ERR \_ INVALIDQUERYCHARACTER            |



 

 

 



