---
description: A classe CMediaType gerencia tipos de mídia. Essa classe herda a \_ estrutura do tipo de mídia am \_ . Ele pode ser convertido em uma variável do tipo de mídia do tipo AM \_ \_ .
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: Classe CMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755347"
---
# <a name="cmediatype-class"></a>Classe CMediaType

![hierarquia de classe CMediaType](images/mtype01.png)

A `CMediaType` classe gerencia os tipos de mídia. Essa classe herda a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Ele pode ser convertido em uma variável do tipo **de \_ mídia \_** do tipo am.



| Métodos públicos                                                      | Descrição                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | Método de construtor.                                                            |
| [**~ CMediaType**](cmediatype--cmediatype.md)                       | Método destruidor.                                                             |
| [**Definir**](cmediatype-set.md)                                       | Define o tipo de mídia de outro tipo de mídia.                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | Determina se um tipo principal foi atribuído a este objeto.              |
| [**Tipo**](cmediatype-type.md)                                     | Recupera o tipo principal.                                                      |
| [**Tipo de**](cmediatype-settype.md)                               | Especifica o tipo principal.                                                      |
| [**Subtipo**](cmediatype-subtype.md)                               | Recupera o subtipo.                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | Especifica o subtipo.                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | Determina se os exemplos têm um tamanho fixo ou uma variável.                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | Determina se o fluxo usa a compactação temporal.                            |
| [**Getsampleize**](cmediatype-getsamplesize.md)                   | Recupera o tamanho da amostra.                                                     |
| [**Setsampleize**](cmediatype-setsamplesize.md)                   | Especifica um tamanho de amostra fixo ou especifica que os exemplos têm um tamanho variável. |
| [**Setvariableize**](cmediatype-setvariablesize.md)               | Especifica que os exemplos não têm um tamanho fixo.                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | Especifica se os exemplos são compactados usando a compactação temporal.           |
| [**Formatar**](cmediatype-format.md)                                 | Recupera um ponteiro para o bloco de formato.                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | Recupera o comprimento do bloco de formato.                                      |
| [**Setformatype**](cmediatype-setformattype.md)                   | Especifica o tipo do formato.                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | Recupera o tipo de formato.                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | Especifica o bloco de formato.                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | Exclui o bloco de formato.                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | Aloca memória para o bloco de formato.                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | Realoca o bloco de formato para um novo tamanho.                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | Inicializa o tipo de mídia.                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | Determina se esse tipo de mídia corresponde a um tipo de mídia parcialmente especificado.        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | Determina se o tipo de mídia está parcialmente definido.                             |
| Operadores                                                           | Descrição                                                                    |
| [**operador =**](cmediatype-operator-.md)                          | Sobrecarrega o operador de atribuição para copiar um tipo de mídia.                        |
| [**operador = =**](cmediatype-operator--.md)                        | Testa a igualdade entre objetos `CMediaType`.                               |
| [**operador! =**](cmediatype-operator-neq.md)                      | Testa a desigualdade entre objetos `CMediaType`.                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Mtype. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




